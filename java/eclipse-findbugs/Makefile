# Created by: Mario Sergio Fujikawa Ferreira <lioux@FreeBSD.org>
# $FreeBSD$

PORTNAME=	findbugs
DISTVERSION=	3.0.0.20140706-2cfb468
CATEGORIES=	java devel
MASTER_SITES=	SF/${PORTNAME}/${PORTNAME}%20eclipse%20plugin/3.0.0
PKGNAMEPREFIX=	eclipse-
DISTNAME=	edu.umd.cs.findbugs.plugin.eclipse_${DISTVERSION}
DIST_SUBDIR=	eclipse

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Eclipse plug-in that provides FindBugs support

RUN_DEPENDS=	eclipse:${PORTSDIR}/java/eclipse

USES=		zip
NO_BUILD=	yes
USE_JAVA=	yes
JAVA_VERSION=	1.6+
JAVA_OS=	native

PLIST_SUB=	\
	ECLIPSE_PLUGINS="lib/eclipse/plugins" \
	DISTNAME="${DISTNAME}"

post-extract:
	@${RM} -Rf ${WRKSRC}/src

do-install:
	@(cd ${WRKSRC} && ${COPYTREE_SHARE} . ${STAGEDIR}${PREFIX}/lib/eclipse/plugins/${DISTNAME})

.include <bsd.port.mk>
