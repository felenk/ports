# $OpenBSD: Makefile,v 1.12 2021/05/22 21:54:07 sebastia Exp $

COMMENT =	convert pcap dumps to hashcat or John the Ripper input

GH_ACCOUNT =	ZerBea
GH_PROJECT =	hcxtools
GH_TAGNAME =	6.2.0
DISTNAME =	hcxtools-${GH_TAGNAME}

CATEGORIES =	security

MAINTAINER =	Sebastian Reitenbach <sebastia@openbsd.org>

# MIT
PERMIT_PACKAGE=	Yes

WANTLIB += c crypto ssl pthread curl z
LIB_DEPENDS +=	net/curl

USE_GMAKE =	Yes
ALL_TARGET =

MAKE_ENV+=	CPPFLAGS="-I${LOCALBASE}/include"
MAKE_ENV+=	LDFLAGS="-L${LOCALBASE}/lib"
#MAKE_ENV+=	CPPFLAGS="-I${LOCALBASE}/include/eopenssl11 -I${LOCALBASE}/include"
#MAKE_ENV+=	LDFLAGS="${LDFLAGS}"
MAKE_FLAGS =	PREFIX='${LOCALBASE}'
FAKE_FLAGS =	MANDIR=${DESTDIR}${PREFIX}/man

pre-install:
	${INSTALL_PROGRAM_DIR} ${PREFIX}/bin

.include <bsd.port.mk>
