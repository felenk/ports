# $OpenBSD: Makefile,v 1.1.1.1 2020/02/17 14:02:22 paco Exp $

COMMENT =		transparent file encryption in Git

DISTNAME =		git-crypt-0.6.0
CATEGORIES =		devel

HOMEPAGE =		https://www.agwa.name/projects/git-crypt/
MAINTAINER =		Paco Esteban <paco@openbsd.org>

# GPL v3+
PERMIT_PACKAGE =	Yes

WANTLIB +=		${COMPILER_LIBCXX} c crypto m

MASTER_SITES =		https://www.agwa.name/projects/git-crypt/downloads/

# C++11
COMPILER =		base-clang ports-gcc

BUILD_DEPENDS =		textproc/libxslt \
			textproc/docbook-xsl

RUN_DEPENDS =		devel/git

MAKE_ENV =		ENABLE_MAN=yes \
			DOCBOOK_XSL=${PREFIX}/share/xsl/docbook/manpages/docbook.xsl \
			BINDIR=${TRUEPREFIX}/bin \
			MANDIR=${TRUEPREFIX}/man

NO_TEST =		Yes

pre-fake:
	[ -f "${WRKSRC}/git-crypt.1" ] && \
		mv "${WRKSRC}/git-crypt.1" "${WRKSRC}/man/man1/git-crypt.1"

.include <bsd.port.mk>
