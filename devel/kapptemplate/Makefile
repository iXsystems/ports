# $FreeBSD$

PORTNAME=	kapptemplate
DISTVERSION=	${KDE_APPLICATIONS_VERSION}
CATEGORIES=	devel kde kde-applications

MAINTAINER=	kde@FreeBSD.org
COMMENT=	KDE template generator

BUILD_DEPENDS=	${LOCALBASE}/share/xsl/docbook/html/docbook.xsl:textproc/docbook-xsl \
		docbook-xml>0:textproc/docbook-xml

USES=		cmake:outsource gettext kde:5 tar:xz
USE_KDE=	auth archive codecs completion config configwidgets coreaddons \
		doctools ecm i18n jobwidgets kio newstuff service widgetsaddons
USE_QT5=	core gui network testlib widgets xml \
		buildtools_build qmake_build

.include <bsd.port.mk>
