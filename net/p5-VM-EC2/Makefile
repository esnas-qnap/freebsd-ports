# Created by: Sunpoet Po-Chuan Hsieh <sunpoet@FreeBSD.org>
# $FreeBSD$

PORTNAME=	VM-EC2
PORTVERSION=	1.28
CATEGORIES=	net perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Perl interface to Amazon EC2 services

LICENSE=	ART10 GPLv1
LICENSE_COMB=	dual

BUILD_DEPENDS=	p5-AnyEvent-CacheDNS>=0.08:${PORTSDIR}/dns/p5-AnyEvent-CacheDNS \
		p5-AnyEvent-HTTP>=2.15:${PORTSDIR}/www/p5-AnyEvent-HTTP \
		p5-AnyEvent>=7.04:${PORTSDIR}/devel/p5-AnyEvent \
		p5-JSON>=0:${PORTSDIR}/converters/p5-JSON \
		p5-String-Approx>=3.26:${PORTSDIR}/devel/p5-String-Approx \
		p5-URI>=1.40:${PORTSDIR}/net/p5-URI \
		p5-XML-Simple>=2.18:${PORTSDIR}/textproc/p5-XML-Simple \
		p5-libwww>=5.835:${PORTSDIR}/www/p5-libwww
RUN_DEPENDS:=	${BUILD_DEPENDS}

USE_PERL5=	modbuild
USES=		perl5

.include <bsd.port.mk>
