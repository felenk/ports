# $OpenBSD: Makefile,v 1.4 2021/03/23 21:01:13 edd Exp $

COMMENT =		GitHub webhooks runner daemon

V =			0.4.2
DISTNAME =		snare-$V

CATEGORIES =		devel

HOMEPAGE =		https://tratt.net/laurie/src/snare/
MASTER_SITES =		${HOMEPAGE}releases/
EXTRACT_SUFX =		.tgz

MAINTAINER =            Laurence Tratt <laurie@tratt.net>

# Apache-2.0/MIT
PERMIT_PACKAGE =	Yes

WANTLIB +=		c c++abi m pthread

DISTFILES +=		${DISTNAME}${EXTRACT_SUFX}
MODULES =		devel/cargo

MODCARGO_CRATES +=	aho-corasick	0.7.15	# Unlicense/MIT
MODCARGO_CRATES +=	autocfg	1.0.1	# Apache-2.0 OR MIT
MODCARGO_CRATES +=	bincode	1.3.2	# MIT
MODCARGO_CRATES +=	bitflags	1.2.1	# MIT/Apache-2.0
MODCARGO_CRATES +=	block-buffer	0.9.0	# MIT OR Apache-2.0
MODCARGO_CRATES +=	bstr	0.2.15	# MIT OR Apache-2.0
MODCARGO_CRATES +=	byteorder	1.3.4	# Unlicense OR MIT
MODCARGO_CRATES +=	bytes	1.0.1	# MIT
MODCARGO_CRATES +=	cactus	1.0.6	# Apache-2.0/MIT
MODCARGO_CRATES +=	cc	1.0.67	# MIT/Apache-2.0
MODCARGO_CRATES +=	cfg-if	0.1.10	# MIT/Apache-2.0
MODCARGO_CRATES +=	cfg-if	1.0.0	# MIT/Apache-2.0
MODCARGO_CRATES +=	cfgrammar	0.9.3	# Apache-2.0/MIT
MODCARGO_CRATES +=	chrono	0.4.19	# MIT/Apache-2.0
MODCARGO_CRATES +=	cpuid-bool	0.1.2	# MIT OR Apache-2.0
MODCARGO_CRATES +=	crossbeam-utils	0.8.3	# MIT OR Apache-2.0
MODCARGO_CRATES +=	crypto-mac	0.10.0	# MIT OR Apache-2.0
MODCARGO_CRATES +=	digest	0.9.0	# MIT OR Apache-2.0
MODCARGO_CRATES +=	filetime	0.2.14	# MIT/Apache-2.0
MODCARGO_CRATES +=	fnv	1.0.7	# Apache-2.0 / MIT
MODCARGO_CRATES +=	futures-channel	0.3.13	# MIT OR Apache-2.0
MODCARGO_CRATES +=	futures-core	0.3.13	# MIT OR Apache-2.0
MODCARGO_CRATES +=	futures-task	0.3.13	# MIT OR Apache-2.0
MODCARGO_CRATES +=	futures-util	0.3.13	# MIT OR Apache-2.0
MODCARGO_CRATES +=	generic-array	0.14.4	# MIT
MODCARGO_CRATES +=	getopts	0.2.21	# MIT/Apache-2.0
MODCARGO_CRATES +=	getrandom	0.2.2	# MIT OR Apache-2.0
MODCARGO_CRATES +=	globset	0.4.6	# Unlicense/MIT
MODCARGO_CRATES +=	hashbrown	0.9.1	# Apache-2.0/MIT
MODCARGO_CRATES +=	hermit-abi	0.1.18	# MIT/Apache-2.0
MODCARGO_CRATES +=	hex	0.4.3	# MIT OR Apache-2.0
MODCARGO_CRATES +=	hmac	0.10.1	# MIT OR Apache-2.0
MODCARGO_CRATES +=	http	0.2.3	# MIT/Apache-2.0
MODCARGO_CRATES +=	http-body	0.4.0	# MIT
MODCARGO_CRATES +=	httparse	1.3.5	# MIT/Apache-2.0
MODCARGO_CRATES +=	httpdate	0.3.2	# MIT/Apache-2.0
MODCARGO_CRATES +=	hyper	0.14.4	# MIT
MODCARGO_CRATES +=	ignore	0.4.17	# Unlicense/MIT
MODCARGO_CRATES +=	indexmap	1.6.2	# Apache-2.0/MIT
MODCARGO_CRATES +=	instant	0.1.9	# BSD-3-Clause
MODCARGO_CRATES +=	itoa	0.4.7	# MIT OR Apache-2.0
MODCARGO_CRATES +=	json	0.12.4	# MIT/Apache-2.0
MODCARGO_CRATES +=	lazy_static	1.4.0	# MIT/Apache-2.0
MODCARGO_CRATES +=	libc	0.2.89	# MIT OR Apache-2.0
MODCARGO_CRATES +=	lock_api	0.4.2	# Apache-2.0/MIT
MODCARGO_CRATES +=	log	0.4.14	# MIT OR Apache-2.0
MODCARGO_CRATES +=	lrlex	0.9.3	# Apache-2.0/MIT
MODCARGO_CRATES +=	lrpar	0.9.3	# Apache-2.0/MIT
MODCARGO_CRATES +=	lrtable	0.9.3	# Apache-2.0/MIT
MODCARGO_CRATES +=	memchr	2.3.4	# Unlicense/MIT
MODCARGO_CRATES +=	mio	0.7.10	# MIT
MODCARGO_CRATES +=	miow	0.3.6	# MIT/Apache-2.0
MODCARGO_CRATES +=	nix	0.19.1	# MIT
MODCARGO_CRATES +=	ntapi	0.3.6	# Apache-2.0 OR MIT
MODCARGO_CRATES +=	num-integer	0.1.44	# MIT OR Apache-2.0
MODCARGO_CRATES +=	num-traits	0.2.14	# MIT OR Apache-2.0
MODCARGO_CRATES +=	num_cpus	1.13.0	# MIT/Apache-2.0
MODCARGO_CRATES +=	once_cell	1.7.2	# MIT OR Apache-2.0
MODCARGO_CRATES +=	opaque-debug	0.3.0	# MIT OR Apache-2.0
MODCARGO_CRATES +=	packedvec	1.2.3	# Apache-2.0/MIT
MODCARGO_CRATES +=	parking_lot	0.11.1	# Apache-2.0/MIT
MODCARGO_CRATES +=	parking_lot_core	0.8.3	# Apache-2.0/MIT
MODCARGO_CRATES +=	percent-encoding	2.1.0	# MIT/Apache-2.0
MODCARGO_CRATES +=	pest	2.1.3	# MIT/Apache-2.0
MODCARGO_CRATES +=	pin-project	1.0.5	# Apache-2.0 OR MIT
MODCARGO_CRATES +=	pin-project-internal	1.0.5	# Apache-2.0 OR MIT
MODCARGO_CRATES +=	pin-project-lite	0.2.6	# Apache-2.0 OR MIT
MODCARGO_CRATES +=	pin-utils	0.1.0	# MIT OR Apache-2.0
MODCARGO_CRATES +=	ppv-lite86	0.2.10	# MIT/Apache-2.0
MODCARGO_CRATES +=	proc-macro2	1.0.24	# MIT OR Apache-2.0
MODCARGO_CRATES +=	quote	1.0.9	# MIT OR Apache-2.0
MODCARGO_CRATES +=	rand	0.8.3	# MIT OR Apache-2.0
MODCARGO_CRATES +=	rand_chacha	0.3.0	# MIT OR Apache-2.0
MODCARGO_CRATES +=	rand_core	0.6.2	# MIT OR Apache-2.0
MODCARGO_CRATES +=	rand_hc	0.3.0	# MIT OR Apache-2.0
MODCARGO_CRATES +=	redox_syscall	0.2.5	# MIT
MODCARGO_CRATES +=	regex	1.4.5	# MIT OR Apache-2.0
MODCARGO_CRATES +=	regex-syntax	0.6.23	# MIT/Apache-2.0
MODCARGO_CRATES +=	remove_dir_all	0.5.3	# MIT/Apache-2.0
MODCARGO_CRATES +=	rerun_except	0.1.2	# Apache-2.0/MIT
MODCARGO_CRATES +=	rustc_version	0.3.3	# MIT/Apache-2.0
MODCARGO_CRATES +=	same-file	1.0.6	# Unlicense/MIT
MODCARGO_CRATES +=	scopeguard	1.1.0	# MIT/Apache-2.0
MODCARGO_CRATES +=	secstr	0.4.0	# Unlicense
MODCARGO_CRATES +=	semver	0.11.0	# MIT/Apache-2.0
MODCARGO_CRATES +=	semver-parser	0.10.2	# MIT/Apache-2.0
MODCARGO_CRATES +=	serde	1.0.124	# MIT OR Apache-2.0
MODCARGO_CRATES +=	serde_derive	1.0.124	# MIT OR Apache-2.0
MODCARGO_CRATES +=	sha-1	0.9.4	# MIT OR Apache-2.0
MODCARGO_CRATES +=	signal-hook	0.2.3	# Apache-2.0/MIT
MODCARGO_CRATES +=	signal-hook-registry	1.3.0	# Apache-2.0/MIT
MODCARGO_CRATES +=	smallvec	1.6.1	# MIT/Apache-2.0
MODCARGO_CRATES +=	socket2	0.3.19	# MIT/Apache-2.0
MODCARGO_CRATES +=	sparsevec	0.1.3	# Apache-2.0/MIT
MODCARGO_CRATES +=	static_assertions	1.1.0	# MIT OR Apache-2.0
MODCARGO_CRATES +=	subtle	2.4.0	# BSD-3-Clause
MODCARGO_CRATES +=	syn	1.0.64	# MIT OR Apache-2.0
MODCARGO_CRATES +=	tempfile	3.2.0	# MIT OR Apache-2.0
MODCARGO_CRATES +=	thread_local	1.1.3	# Apache-2.0/MIT
MODCARGO_CRATES +=	time	0.1.43	# MIT/Apache-2.0
MODCARGO_CRATES +=	tokio	1.3.0	# MIT
MODCARGO_CRATES +=	tokio-macros	1.1.0	# MIT
MODCARGO_CRATES +=	tower-service	0.3.1	# MIT
MODCARGO_CRATES +=	tracing	0.1.25	# MIT
MODCARGO_CRATES +=	tracing-core	0.1.17	# MIT
MODCARGO_CRATES +=	try-lock	0.2.3	# MIT
MODCARGO_CRATES +=	try_from	0.3.2	# MIT
MODCARGO_CRATES +=	typenum	1.13.0	# MIT OR Apache-2.0
MODCARGO_CRATES +=	ucd-trie	0.1.3	# MIT/Apache-2.0
MODCARGO_CRATES +=	unicode-width	0.1.8	# MIT/Apache-2.0
MODCARGO_CRATES +=	unicode-xid	0.2.1	# MIT OR Apache-2.0
MODCARGO_CRATES +=	users	0.11.0	# MIT
MODCARGO_CRATES +=	vergen	3.2.0	# MIT/Apache-2.0
MODCARGO_CRATES +=	version_check	0.9.3	# MIT/Apache-2.0
MODCARGO_CRATES +=	vob	2.0.6	# Apache-2.0/MIT
MODCARGO_CRATES +=	walkdir	2.3.1	# Unlicense/MIT
MODCARGO_CRATES +=	want	0.3.0	# MIT
MODCARGO_CRATES +=	wasi	0.10.2+wasi-snapshot-preview1	# Apache-2.0 WITH LLVM-exception OR Apache-2.0 OR MIT
MODCARGO_CRATES +=	winapi	0.3.9	# MIT/Apache-2.0
MODCARGO_CRATES +=	winapi-i686-pc-windows-gnu	0.4.0	# MIT/Apache-2.0
MODCARGO_CRATES +=	winapi-util	0.1.5	# Unlicense/MIT
MODCARGO_CRATES +=	winapi-x86_64-pc-windows-gnu	0.4.0	# MIT/Apache-2.0

CONFIGURE_STYLE =	cargo

SEPARATE_BUILD =	Yes

MODCARGO_RUSTFLAGS =	-C debuginfo=0

do-install:
	${INSTALL_PROGRAM} ${MODCARGO_TARGET_DIR}/release/snare ${PREFIX}/bin/
	${INSTALL_MAN} ${WRKSRC}/snare.1 ${PREFIX}/man/man1/
	${INSTALL_MAN} ${WRKSRC}/snare.conf.5 ${PREFIX}/man/man5/
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/snare
	${INSTALL_DATA} ${WRKSRC}/snare.conf.example ${PREFIX}/share/examples/snare/snare.conf

.include <bsd.port.mk>
