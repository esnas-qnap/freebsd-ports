# Created by: TAKATSU Tomonari <tota@rtfm.jp>
# $FreeBSD$

PORTNAME=	jpmobile
PORTVERSION=	4.2.0
CATEGORIES=	japanese www rubygems
MASTER_SITES=	RG
PKGNAMESUFFIX=	4

MAINTAINER=	tota@FreeBSD.org
COMMENT=	Rails plugin for Japanese mobile-phones

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/MIT-LICENSE

RUN_DEPENDS=	rubygem-rails4>0:${PORTSDIR}/www/rubygem-rails4

USE_RUBY=	yes
USE_RUBYGEMS=	yes
RUBYGEM_AUTOPLIST=	yes

OPTIONS_DEFINE=		GEOKIT IPADDRESSES TERMINFO
GEOKIT_DESC=		Run with geokit
IPADDRESSES_DESC=	IP address validation support
TERMINFO_DESC=		terminal information support

OPTIONS_DEFAULT=	IPADDRESSES TERMINFO

.include <bsd.port.pre.mk>

PKGNAMEPREFIX:=	${PKGNAMEPREFIX}rubygem-

GEOKIT_RUN_DEPENDS=	rubygem-geokit>=1.5.0:${PORTSDIR}/graphics/rubygem-geokit
IPADDRESSES_RUN_DEPENDS=	ja-rubygem-jpmobile-ipaddresses>=0.0.1:${PORTSDIR}/japanese/rubygem-jpmobile-ipaddresses
TERMINFO_RUN_DEPENDS+=	ja-rubygem-jpmobile-terminfo>=0.0.2:${PORTSDIR}/japanese/rubygem-jpmobile-terminfo

.include <bsd.port.post.mk>
