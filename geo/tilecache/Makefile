# $OpenBSD: Makefile,v 1.19 2021/05/21 19:50:32 kmos Exp $

COMMENT =	tile caching frontend for WMS/TMS services

MODPY_EGG_VERSION =	2.11
DISTNAME =	tilecache-${MODPY_EGG_VERSION}
REVISION =	5

CATEGORIES =	geo graphics

HOMEPAGE =	http://tilecache.org/
MAINTAINER =	Landry Breuil <landry@openbsd.org>

# BSD
PERMIT_PACKAGE =	Yes

MASTER_SITES =	${HOMEPAGE}

MODULES =	lang/python
MODPY_VERSION =	${MODPY_DEFAULT_VERSION_2}

MODPY_SETUPTOOLS =	Yes
RUN_DEPENDS =		graphics/py2-Pillow \
			www/py-paste

post-configure:
	${SUBST_CMD} ${WRKSRC}/setup.py

post-install:
	${INSTALL_SCRIPT_DIR} ${PREFIX}/libexec/tilecache/
	mv ${PREFIX}/bin/tilecache.{f,}cgi ${PREFIX}/libexec/tilecache/

.include <bsd.port.mk>
