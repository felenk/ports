# $OpenBSD: Makefile,v 1.11 2021/02/24 16:49:00 sthen Exp $

COMMENT=	roundcube plugin: DKIM verification status

GH_ACCOUNT=	JVEHENT
GH_PROJECT=	dkimstatus
GH_TAGNAME=	v0.9.5
PKGNAME=	rcube-${DISTNAME}
REVISION=	5

CATEGORIES=	mail www

HOMEPAGE=	https://jve.linuxwall.info/blog/index.php?pages/DKIMSTATUS-plugin-for-roundcube

# GPLv2
PERMIT_PACKAGE=	Yes

NO_BUILD=	Yes
NO_TEST=	Yes
PKG_ARCH=	*

PREFIX=		${VARBASE}/www
INSTDIR=	${PREFIX}/roundcubemail/plugins
TINSTDIR=	${TRUEPREFIX}/roundcubemail/plugins
SUBST_VARS=	INSTDIR TINSTDIR

MODULES=	lang/php

RUN_DEPENDS=	mail/roundcubemail>=1.1

do-install:
	${INSTALL_DATA_DIR} ${INSTDIR}/dkimstatus
	cp -Rp ${WRKDIST}/* ${INSTDIR}/dkimstatus
	chown -R ${SHAREOWN}:${SHAREGRP} ${INSTDIR}
	find ${INSTDIR} \( -name \*.orig -or -name \*.src \) -delete

.include <bsd.port.mk>
