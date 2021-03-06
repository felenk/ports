# $OpenBSD: Makefile,v 1.17 2021/04/29 04:25:14 rsadowski Exp $

COMMENT =		library supporting Blu-ray playback

V =			1.3.0
DISTNAME =		libbluray-${V}
CATEGORIES =		multimedia

HOMEPAGE =		https://www.videolan.org/developers/libbluray.html

MASTER_SITES =		https://download.videolan.org/pub/videolan/libbluray/${V}/ \
			ftp://ftp.videolan.org/pub/videolan/libbluray/${V}/
EXTRACT_SUFX =		.tar.bz2

# LGPL v2.1
PERMIT_PACKAGE =	Yes

WANTLIB +=		c expat fontconfig freetype iconv lzma m pthread
WANTLIB +=		xml2 z

SHARED_LIBS +=		bluray		3.2	# 11.0

LIB_DEPENDS =		converters/libiconv \
			textproc/libxml
BUILD_DEPENDS =		devel/bison

AUTOCONF_VERSION =	2.69
AUTOMAKE_VERSION =	1.16

SEPARATE_BUILD =	Yes
CONFIGURE_STYLE =	autoreconf
YACC =			${LOCALBASE}/bin/bison -y
CONFIGURE_ARGS +=	--disable-bdjava-jar \
			--disable-doxygen-doc \
			--disable-optimizations

.include <bsd.port.mk>
