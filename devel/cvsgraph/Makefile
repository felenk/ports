# $OpenBSD: Makefile,v 1.25 2021/02/01 13:47:23 fcambus Exp $

COMMENT=		graphical representation of CVS repository

DISTNAME=		cvsgraph-1.7.1
CATEGORIES=		devel
HOMEPAGE=		https://www.vagrearg.org/content/cvsgraph
REVISION=		0

# GPLv2+
PERMIT_PACKAGE=	Yes

WANTLIB += c fontconfig freetype gd iconv jpeg m png pthread tiff webp
WANTLIB += z

# also https://gitlab.com/bertho/cvsgraph/
MASTER_SITES=		https://www.vagrearg.org/cvsgraph/release/

LIB_DEPENDS=		converters/libiconv \
			graphics/gd

ALL_TARGET=

CONFIGURE_STYLE=	gnu
CONFIGURE_ARGS=		--with-gd-inc=${LOCALBASE}/include \
			--with-gd-lib=${LOCALBASE}/lib
CFLAGS +=		-I${LOCALBASE}/include

NO_TEST=		Yes

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/cvsgraph
	${INSTALL_DATA} ${WRKSRC}/cvsgraph.conf \
			${PREFIX}/share/examples/cvsgraph

.include <bsd.port.mk>
