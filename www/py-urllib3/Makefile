# $OpenBSD: Makefile,v 1.22 2021/05/21 19:50:39 kmos Exp $

COMMENT=	HTTP library for Python

MODPY_EGG_VERSION=1.26.4
DISTNAME=	urllib3-${MODPY_EGG_VERSION}
PKGNAME=	py-urllib3-${MODPY_EGG_VERSION}
REVISION=	0

CATEGORIES=	www


# MIT
PERMIT_PACKAGE=	Yes

MODULES=	lang/python

FLAVORS =		python3
FLAVOR ?=

MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes
MODPY_PYTEST =		Yes

.if ${FLAVOR:Mpython3}
TEST_DEPENDS =		devel/py-mock${MODPY_FLAVOR} \
			net/py-socks${MODPY_FLAVOR} \
			sysutils/py-psutil${MODPY_FLAVOR} \
			security/py-trustme${MODPY_FLAVOR} \
			www/py-tornado${MODPY_FLAVOR}

TEST_ENV +=		PYTHONPATH=${WRKSRC}/src
.else
NO_TEST =		Yes
.endif

.include <bsd.port.mk>
