# $OpenBSD: Makefile,v 1.21 2021/03/14 21:31:42 kmos Exp $

COMMENT =		helper to test wsgi applications

MODPY_EGG_VERSION =	2.0.35
DISTNAME =		WebTest-${MODPY_EGG_VERSION}
PKGNAME =		py-${DISTNAME:L}

CATEGORIES =		www devel

HOMEPAGE =		http://webtest.pythonpaste.org/

# MIT
PERMIT_PACKAGE =	Yes

MODULES =		lang/python

MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes
MODPY_PYTEST =		Yes
MODPY_PYTEST_ARGS =	tests

FLAVORS =		python3
FLAVOR =		python3

RUN_DEPENDS =		devel/py-six${MODPY_FLAVOR} \
			www/py-waitress${MODPY_FLAVOR} \
			www/py-beautifulsoup4${MODPY_FLAVOR} \
			www/py-webob${MODPY_FLAVOR}>=1.2

# also needs WSGIProxy2 and PasteDeploy
TEST_DEPENDS =		devel/py-coverage${MODPY_FLAVOR} \
			devel/py-mock${MODPY_FLAVOR} \
			www/py-query${MODPY_FLAVOR}

.include <bsd.port.mk>
