# $FreeBSD$

PORTNAME=	signon-kwallet-extension
DISTVERSION=	${KDE_APPLICATIONS_VERSION}
CATEGORIES=	sysutils kde kde-applications

MAINTAINER=	kde@FreeBSD.org
COMMENT=	KWallet integration for signon framework

LIB_DEPENDS=	libsignon-qt5.so:sysutils/signon-qt5

USES=		cmake:outsource kde:5 pkgconfig tar:xz
USE_KDE=	ecm wallet
USE_QT5=	core dbus gui \
		buildtools_build qmake_build
USE_LDCONFIG=	${KDE_PREFIX}/${SE_DIR}
PLIST_FILES=	${SE_DIR}/libkeyring-kwallet.so
SE_DIR=		lib/signon/extensions

.include <bsd.port.mk>
