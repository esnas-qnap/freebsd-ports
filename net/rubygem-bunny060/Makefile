# Created by: renchap@cocoa-x.com
# $FreeBSD$

PORTNAME=	bunny
PORTVERSION=	0.6.0
CATEGORIES=	net rubygems
MASTER_SITES=	RG

MAINTAINER=	ruby@FreeBSD.org
COMMENT=	Another synchronous Ruby AMQP client

RUN_DEPENDS=	rubygem-amq-protocol>=1.6.0:${PORTSDIR}/net/rubygem-amq-protocol

DEPRECATED=	Use net/rubygem-bunny instead
EXPIRATION_DATE=2015-06-30

USE_RUBY=	yes
USE_RUBYGEMS=	yes
RUBYGEM_AUTOPLIST=	yes

PKGNAMESUFFIX=	060

PORTSCOUT=	limit:^0\.6\.0

.include <bsd.port.mk>
