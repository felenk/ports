# $OpenBSD: Makefile,v 1.27 2021/02/19 23:13:03 sthen Exp $

COMMENT =	Python module for creating Excel XLSX files

MODPY_EGG_VERSION = 1.2.9
DISTNAME =	XlsxWriter-${MODPY_EGG_VERSION}
PKGNAME =	py-${DISTNAME:L}
REVISION =	1

CATEGORIES =	devel

HOMEPAGE =	https://xlsxwriter.readthedocs.io/

MAINTAINER =	Remi Pointel <rpointel@openbsd.org>

# BSD
PERMIT_PACKAGE =	Yes

MODULES =	lang/python
MODPY_PI =	Yes

FLAVORS =	python3
FLAVOR ?=

NO_TEST =	Yes

post-install:
	mv ${PREFIX}/bin/vba_extract.py \
		${PREFIX}/bin/vba_extract.py${MODPY_BIN_SUFFIX}

.include <bsd.port.mk>
