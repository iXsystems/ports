# $FreeBSD$

PORTNAME=	zope.app.folder
PORTVERSION=	3.5.2
PORTREVISION=	1
CATEGORIES=	devel python zope
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}
DIST_SUBDIR=	zope

MAINTAINER=	zope@FreeBSD.org
COMMENT=	Folder Content Type for Zope 3

LICENSE=	ZPL21

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}zope.container>=0:devel/py-zope.container@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}zope.site>=0:devel/py-zope.site@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}zope.app.content>=0:devel/py-zope.app.content@${FLAVOR}

USES=		python:2.7
USE_PYTHON=	distutils autoplist

.include <bsd.port.mk>
