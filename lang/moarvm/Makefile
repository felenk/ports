# $OpenBSD: Makefile,v 1.26 2021/03/11 12:17:21 pascal Exp $

ONLY_FOR_ARCHS =	aarch64 amd64 arm i386 mips64 mips64el powerpc powerpc64 sparc64

COMMENT =		virtual machine for nqp/rakudo

V =			2021.02
DISTNAME =		MoarVM-$V
PKGNAME =		moarvm-$V

SHARED_LIBS =		moar	10.0

CATEGORIES =		lang

HOMEPAGE =		https://moarvm.org/

MAINTAINER =		Pascal Stumpf <pascal@stumpf.co>

# Artistic2
PERMIT_PACKAGE =	Yes

WANTLIB =		atomic_ops c ffi kvm m pthread uv zstd

MASTER_SITES =		https://moarvm.org/releases/

BUILD_DEPENDS =		math/libtommath>=1.2.0
LIB_DEPENDS =		devel/libffi \
			devel/boehm-gc,-atomic \
			devel/libuv \
			archivers/zstd

MAKE_FLAGS =		NOISY=1

CONFIGURE_STYLE =	simple
CONFIGURE_SCRIPT =	/usr/bin/perl Configure.pl
CONFIGURE_ARGS +=	--cc="${CC}" --ld="${CC}" --no-optimize \
			--prefix="${PREFIX}" \
			--has-libtommath \
			--has-libffi \
			--has-libatomic_ops \
			--has-libuv \
			--no-jit
CONFIGURE_ENV =		SO_VERSION="${LIBmoar_VERSION}" \
			CFLAGS="-std=gnu99 ${CFLAGS}"

NO_TEST =		Yes

.include <bsd.port.mk>
