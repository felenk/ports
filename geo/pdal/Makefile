# $OpenBSD: Makefile,v 1.17 2020/11/05 16:43:29 jasper Exp $

COMMENT =	translator library for point cloud formats

DISTNAME =	PDAL-2.2.0-src
PKGNAME =	${DISTNAME:L:C/-src//}

SHARED_LIBS =	pdal_base 3.0 # 6.1
SHARED_LIBS +=  pdal_util 0.2 # 6.1

CATEGORIES =	geo devel textproc

HOMEPAGE =	https://pdal.io/
MASTER_SITES =	https://github.com/PDAL/PDAL/releases/download/2.2.0/

MAINTAINER =	Landry Breuil <landry@openbsd.org>

# BSD
PERMIT_PACKAGE =	Yes

MODULES =	devel/cmake

# uses std=c++0x
COMPILER =	base-clang ports-gcc

LIB_DEPENDS =	${MODPY_LIB_DEPENDS} \
		archivers/laszip \
		geo/gdal \
		databases/postgresql \
		net/curl

WANTLIB +=	c crypto curl gdal geotiff laszip m pq pthread
WANTLIB +=	ssl xml2 z zstd
WANTLIB += ${COMPILER_LIBCXX}

CONFIGURE_ARGS =	\
	-DLASZIP_INCLUDE_DIR=${LOCALBASE}/include \
	-DPDAL_PLUGIN_INSTALL_PATH=${LOCALBASE}/share/pdal/plugins \
	-DWITH_TESTS=FALSE

.include <bsd.port.mk>
