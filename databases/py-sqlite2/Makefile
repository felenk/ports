# $OpenBSD: Makefile,v 1.33 2021/02/23 19:39:12 sthen Exp $

COMMENT =	SQLite3 adapter for Python

MODPY_EGG_VERSION =	2.8.3

DISTNAME =	pysqlite-${MODPY_EGG_VERSION}
PKGNAME =	py-sqlite2-${MODPY_EGG_VERSION}
CATEGORIES =	databases devel
REVISION =	1

HOMEPAGE =	https://github.com/ghaering/pysqlite/

MODPY_PI =	Yes

# BSD-like
PERMIT_PACKAGE =	Yes

WANTLIB += ${MODPY_WANTLIB}
WANTLIB += pthread sqlite3>=8.6

BUILD_DEPENDS =	textproc/py-sphinx,python3

MODULES =	lang/python
MODPY_VERSION =	${MODPY_DEFAULT_VERSION_2}

post-build:
	cd ${WRKSRC} && \
		${LOCALBASE}/bin/sphinx-build -N -b text doc/sphinx \
		build/doc

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/py-sqlite2
	${INSTALL_DATA} ${WRKSRC}/build/doc/sqlite3.txt \
		${PREFIX}/share/doc/py-sqlite2/

do-test: fake
	@cd ${WRKDIR} && \
		${SETENV} PYTHONPATH=${WRKINST}${MODPY_SITEPKG} \
		${MODPY_BIN} -c 'from pysqlite2 import test; test.test()'

.include <bsd.port.mk>
