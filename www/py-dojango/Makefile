# Created by: jpaetzel
# $FreeBSD$

PORTNAME=	dojango
PORTVERSION=	0.5.9
PORTREVISION=	4
CATEGORIES=	www python java
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	jpaetzel@FreeBSD.org
COMMENT=	Django application for building dojo

USES=		python
USE_PYTHON=	distutils autoplist

USE_GITHUB=	yes
GH_ACCOUNT=	william-gr
GH_PROJECT=	dojango
GH_TAGNAME=	87507e5

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}django110>=1.6:www/py-django110@${FLAVOR}

OPTIONS_DEFINE=		JAVA

.include <bsd.port.options.mk>

.if ${PORT_OPTIONS:MJAVA}
USE_JAVA=	yes
JAVA_VERSION=	1.6+
.endif

.include <bsd.port.mk>
