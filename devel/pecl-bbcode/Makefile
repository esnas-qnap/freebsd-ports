# Created by: Ditesh Shashikant Gathani <ditesh@gathani.org>
# $FreeBSD$

PORTNAME=	bbcode
PORTVERSION=	1.0.2
CATEGORIES=	devel pear
MASTER_SITES=	http://pecl.php.net/get/
PKGNAMEPREFIX=	pecl-
DIST_SUBDIR=	PECL

MAINTAINER=	ports@FreeBSD.org
COMMENT=	PECL extension which allows quick and efficient BBCode Parsing

LICENSE=	PHP301 BSD3CLAUSE
LICENSE_COMB=	multi

USES=		tar:tgz
USE_PHP=	yes
USE_PHP_BUILD=	yes
USE_PHPEXT=	yes
IGNORE_WITH_PHP=5 56

CONFIGURE_ARGS=	--enable-bbcode

post-patch:
	@${REINPLACE_CMD} -e 's/#include <malloc.h>/\/\/#include <malloc.h>/g' ${WRKSRC}/lib/bbcode2.c

.include <bsd.port.mk>
