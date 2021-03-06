# $OpenBSD: Makefile,v 1.109 2021/05/14 09:40:36 ajacoutot Exp $

COMMENT=		IDE for GNOME

GNOME_PROJECT=		gnome-builder
GNOME_VERSION=		3.40.2

CATEGORIES=		devel

# GPLv3
PERMIT_PACKAGE=		Yes

WANTLIB += c cairo cairo-gobject clang dazzle-1.0 devhelp-3 enchant-2
WANTLIB += fontconfig gdk-3 gio-2.0 girepository-1.0 gladeui-2
WANTLIB += glib-2.0 gobject-2.0 gspell-1 gtk-3 gtksourceview-4
WANTLIB += intl json-glib-1.0 jsonrpc-glib-1.0 pango-1.0 pangocairo-1.0
WANTLIB += pangoft2-1.0 pcre peas-1.0 template_glib-1.0 vte-2.91
WANTLIB += webkit2gtk-4.0 xml2

MODULES=		devel/dconf \
			devel/meson \
			lang/python \
			x11/gnome

MODGNOME_TOOLS=		desktop-file-utils gtk-update-icon-cache \
			gobject-introspection yelp

# needs support for variadic macros (__VA_OPT__)
# https://bugs.llvm.org/show_bug.cgi?id=40665
COMPILER=		ports-gcc
COMPILER_LANGS=		c

BUILD_DEPENDS=		devel/ectags \
			devel/libexecinfo \
			textproc/py-sphinx${MODPY_FLAVOR}

RUN_DEPENDS=		devel/ectags

# python auto-completion
RUN_DEPENDS +=		devel/py-jedi${MODPY_FLAVOR}

# python documentation auto-completion
RUN_DEPENDS +=		textproc/py-lxml${MODPY_FLAVOR}

# see patch-src_plugins_todo_gbp-todo-model_c
RUN_DEPENDS +=		sysutils/ggrep

LIB_DEPENDS=		devel/glade \
			devel/jsonrpc-glib \
			devel/libpeas \
			devel/llvm \
			devel/template-glib \
			devel/vte3 \
			textproc/gspell \
			x11/gnome/devhelp \
			x11/gnome/libdazzle \
			x11/gtksourceview4

.include <bsd.port.arch.mk>
.if ${ARCH:Mi386}
# Doesn't build with lld: non-ABS relocation R_386_GOTOFF against symbol '.LC74'
USE_LLD =		No
.endif

CONFIGURE_ARGS=		-Dplugin_valgrind=false \
			-Dplugin_flatpak=false \
			-Dplugin_sysprof=false \
			-Dplugin_update_manager=false \
			-Dchannel=other

# requires libportal
CONFIGURE_ARGS +=	-Dplugin_color_picker=false

# XXX prctl(2) or procctl(2)
# error: #error "Please submit a patch to support parent-death signal on your OS"
CONFIGURE_ARGS +=	-Dplugin_git=false

MODGNOME_LDFLAGS +=	-L${X11BASE}/lib

DEBUG_PACKAGES=		${BUILD_PACKAGES}

# disable meson's default of using "-Wl,--as-needed" with ld.bfd;
# build failures due to undefined references are often seen.
.include <bsd.port.arch.mk>
.if !${PROPERTIES:Mlld} || ${ARCH:Mi386}
CONFIGURE_ARGS +=	-Db_asneeded=false
.endif

# don't pick up llvm-config(1) from base
pre-configure:
	ln -sf ${LOCALBASE}/bin/llvm-config ${WRKDIR}/bin/llvm-config

.include <bsd.port.mk>
