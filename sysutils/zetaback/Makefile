# Created by: Cy Schubert <cy@FreeBSD.org>
# $FreeBSD$

PORTNAME=	zetaback
PORTVERSION=	1.0.7
CATEGORIES=	sysutils
MASTER_SITES=	http://mirrors.omniti.com/zetaback/

MAINTAINER=	cy@FreeBSD.org
COMMENT=	Zetaback ZFS backup and recovery management system

USES=		perl5
USE_PERL5=	run
GNU_CONFIGURE=	yes
USE_AUTOTOOLS=	autoconf

post-install:
	@${TEST} ! -f ${PREFIX}/etc/zetaback.conf && ${CP} ${STAGEDIR}${PREFIX}/etc/zetaback.conf.sample ${STAGEDIR}${PREFIX}/etc/zetaback.conf; ${TRUE}
	@${TEST} ! -f ${PREFIX}/etc/zetaback_agent.conf && ${CP} ${STAGEDIR}${PREFIX}/etc/zetaback_agent.conf.sample ${STAGEDIR}${PREFIX}/etc/zetaback_agent.conf; ${TRUE}

.include <bsd.port.mk>
