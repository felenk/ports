# $OpenBSD: Makefile,v 1.17 2021/05/22 05:11:50 rsadowski Exp $

COMMENT =		library set for simulations, games and visualizations

DISTNAME =		simgear-2016.3.1
REVISION =		3

SHARED_LIBS +=  SimGearCore               4.0 # 2.10
SHARED_LIBS +=  SimGearScene              4.0 # 2.10

CATEGORIES =		graphics

MAINTAINER =		Pascal Stumpf <pascal@stumpf.co>

HOMEPAGE =		http://www.flightgear.org

# LGPLv2
PERMIT_PACKAGE =	Yes

MASTER_SITES =		${MASTER_SITE_SOURCEFORGE:=flightgear/}
EXTRACT_SUFX =		.tar.bz2

WANTLIB += GL GLU OpenThreads curl expat m openal osg osgDB osgGA osgParticle
WANTLIB += osgSim osgText osgUtil osgViewer pthread z ${COMPILER_LIBCXX}

MODULES =		devel/cmake
COMPILER =		base-clang ports-gcc
BUILD_DEPENDS =		devel/boost
LIB_DEPENDS =		graphics/openscenegraph \
			audio/openal

CONFIGURE_ARGS +=	-DSYSTEM_EXPAT=ON

CFLAGS +=		-I${X11BASE}/include -pthread
CXXFLAGS +=		-I${X11BASE}/include -pthread

NO_TEST =		Yes

# Keep C++ #include <version> from picking up this unrelated file
post-extract:
	mv ${WRKSRC}/version ${WRKSRC}/version.txt

.include <bsd.port.mk>
