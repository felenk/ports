# $OpenBSD: Makefile,v 1.15 2021/05/21 19:50:36 kmos Exp $

COMMENT =		parse CSS3 Selectors and translates them to XPath 1.0

MODPY_EGG_VERSION =	1.0.0
PKGNAME =		py-${DISTNAME}
REVISION =		4

GH_ACCOUNT =		scrapy
GH_PROJECT =		cssselect
GH_TAGNAME =		v${MODPY_EGG_VERSION}

CATEGORIES =		textproc

# BSD
PERMIT_PACKAGE =	Yes

MODULES =		lang/python

TEST_DEPENDS =		textproc/py-lxml${MODPY_FLAVOR}

MODPY_SETUPTOOLS =	Yes
MODPY_PYTEST =		Yes

FLAVORS =		python3
FLAVOR ?=

.include <bsd.port.mk>
