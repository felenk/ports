# $OpenBSD: Makefile,v 1.23 2021/01/04 14:06:39 sthen Exp $

COMMENT=	YAML parser and emitter in Python

MODPY_EGG_VERSION=5.3.1
DISTNAME=	PyYAML-${MODPY_EGG_VERSION}
PKGNAME=	py-yaml-${MODPY_EGG_VERSION}
CATEGORIES=	textproc
REVISION=	1

HOMEPAGE=	https://pyyaml.org/wiki/PyYAML

MAINTAINER=	Pierre-Emmanuel Andre <pea@openbsd.org>

# BSD
PERMIT_PACKAGE=	Yes

WANTLIB+=	pthread yaml-0 ${MODPY_WANTLIB}

MODULES=	lang/python
MODPY_PI=	Yes

FLAVORS =	python3
FLAVOR ?=

LIB_DEPENDS=	devel/libyaml

pre-configure:
	${SUBST_CMD} ${WRKSRC}/setup.cfg

do-test:
	@cd ${WRKSRC} && ${MODPY_BIN} ${MODPY_SETUP} test

.include <bsd.port.mk>
