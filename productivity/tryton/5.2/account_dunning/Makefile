# $OpenBSD: Makefile,v 1.3 2020/07/03 21:12:29 sthen Exp $

MODPY_EGG_VERSION =	5.2.1
TRYTON_MODULE =		account_dunning
REVISION =		0

TRYTON_DEPENDS += 	account \
			company \
			party

RUN_DEPENDS +=		databases/py-sql${MODPY_FLAVOR}

.include <bsd.port.mk>
