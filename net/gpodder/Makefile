# $OpenBSD: Makefile,v 1.28 2021/02/23 19:39:32 sthen Exp $

COMMENT=		media aggregator and podcast client

MODPY_EGG_VERSION=	3.10.17

GH_ACCOUNT=		gpodder
GH_PROJECT=		gpodder
GH_TAGNAME=		${MODPY_EGG_VERSION}

CATEGORIES=		net www

HOMEPAGE=		https://gpodder.github.io/

MAINTAINER=		Tim Meunier <trondd@kagu-tsuchi.com>

# GPLv3+
PERMIT_PACKAGE=		Yes

MODULES=		lang/python \
			textproc/intltool

# XXX Causes python crash
#MODPY_PYTEST=		Yes

RUN_DEPENDS=		devel/desktop-file-utils \
			devel/gettext,-runtime \
			devel/py-html5lib${MODPY_FLAVOR} \
			devel/py-gobject3${MODPY_FLAVOR} \
			net/mygpoclient \
			textproc/py-podcastparser${MODPY_FLAVOR} \
			www/youtube-dl \
			www/webkitgtk4 \
			x11/dbus-python${MODPY_FLAVOR} \
			x11/gtk+3,-guic
TEST_DEPENDS=		devel/py-coverage${MODPY_FLAVOR} \
			devel/py-minimock${MODPY_FLAVOR} \
			devel/py-test${MODPY_FLAVOR} \
			devel/py-test-cov${MODPY_FLAVOR}

USE_GMAKE=		Yes
MAKE_FILE=		makefile
MAKE_ENV=		LC_CTYPE=en_US.UTF-8 \
			PYTHON=${MODPY_BIN} \
			GPODDER_MANPATH_NO_SHARE="yes"

ALL_TARGET=		messages

TEST_TARGET=		unittest

do-install:
	cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} DESTDIR=/ ${MAKE_PROGRAM} \
		-f ${MAKE_FILE} install
	${MODPY_BIN} ${MODPY_LIBDIR}/compileall.py \
		${PREFIX}/share/gpodder/extensions/

.include <bsd.port.mk>
