# Created by: Pete French <pete@twisted.org.uk>
# $FreeBSD$

PORTNAME=	libobjc2
PORTVERSION=	1.7
PORTREVISION=	1
CATEGORIES=	lang devel gnustep
MASTER_SITES=	http://download.gna.org/gnustep/

MAINTAINER=	theraven@FreeBSD.org
COMMENT=	Replacement Objective-C runtime supporting modern Objective-C features

SSP_UNSAFE=	yes

USES=		cmake tar:bzip2
BROKEN_powerpc=		Does not compile on powerpc: Unsupported relocation type 10

.include <bsd.port.options.mk>

_CLANG!=	if [ -f /usr/bin/clang ] ; then  /usr/bin/clang --version | head -1 | \
		${SED} -e 's/.*clang version \([0-9]\)\.\([0-9]\).*/\1\2/' ; else ${ECHO} 0 ; fi

.if ${_CLANG} < 34
BUILD_DEPENDS+=	${LOCALBASE}/bin/clang34:${PORTSDIR}/lang/clang34
CC=		${LOCALBASE}/bin/clang34
CXX=	${LOCALBASE}/bin/clang++34
.else
CC=		/usr/bin/clang
CXX=	/usr/bin/clang++
.endif

SHLIB_MAJOR=	4
SHLIB_MINOR=	6

PLIST_SUB+=	SHLIB_MAJOR=${SHLIB_MAJOR} SHLIB_MINOR=${SHLIB_MINOR}

.if ${OSVERSION} < 902000
CMAKE_ARGS+=	-DFORCE_LIBOBJCXX=ON
PLIST_SUB+=	WITH_SEPARATECXX=""
.else
PLIST_SUB+=	WITH_SEPARATECXX="@comment "
.endif

CMAKE_ARGS+=	-DLIB_INSTALL_PATH=lib
CMAKE_ARGS+=	-DTESTS=OFF
# This shouldn't be needed, but our llvm port installs llvm-config with a silly
# name...
CMAKE_ARGS+=	-DLLVM_OPTS=OFF

.if ${OSVERSION} < 902000
post-install:
	${LN} -sf libobjc.so.${SHLIB_MAJOR}.${SHLIB_MINOR} ${STAGEDIR}${PREFIX}/lib/libobjc.so.${SHLIB_MAJOR}
	${LN} -sf libobjcxx.so.${SHLIB_MAJOR}.${SHLIB_MINOR} ${STAGEDIR}${PREFIX}/lib/libobjcxx.so.${SHLIB_MAJOR}
.else
post-install:
	${LN} -sf libobjc.so.${SHLIB_MAJOR}.${SHLIB_MINOR} ${STAGEDIR}${PREFIX}/lib/libobjc.so.${SHLIB_MAJOR}
.endif


.include <bsd.port.mk>
