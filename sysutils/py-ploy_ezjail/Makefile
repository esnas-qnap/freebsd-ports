# Created by: Kubilay Kocak <koobs@FreeBSD.org>
# $FreeBSD$

PORTNAME=	ploy_ezjail
PORTVERSION=	1.2.0
CATEGORIES=	sysutils python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	koobs@FreeBSD.org
COMMENT=	Ploy plugin for managing FreeBSD Jails

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}ploy>=1.2.0:${PORTSDIR}/sysutils/py-ploy \
		${PYTHON_PKGNAMEPREFIX}lazy>0:${PORTSDIR}/devel/py-lazy

USES=		python
USE_PYTHON=	autoplist distutils

.include <bsd.port.mk>
