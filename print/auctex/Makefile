# Created by: Martin Kammerhofer
# $FreeBSD$

PORTNAME=	auctex
PORTVERSION=	11.90
PORTREVISION=	3
CATEGORIES=	print elisp
MASTER_SITES=	GNU
PKGNAMESUFFIX=	${EMACS_PKGNAMESUFFIX}

MAINTAINER=	hrs@FreeBSD.org
COMMENT=	Integrated environment for writing LaTeX using GNU Emacs

LICENSE=	GPLv3

USES=		emacs ghostscript gmake
USE_TEX=	latex texhash
TEXHASHDIRS=	${TEXMFDIR}

GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--with-lispdir=${PREFIX}/${EMACS_VERSION_SITE_LISPDIR} \
	--with-auto-dir=${PREFIX}/${EMACS_VERSION_SITE_LISPDIR}/auctex/auto \
	--with-texmf-dir=${PREFIX}/${TEXMFDIR}
PORTDOCS=	tex-ref.pdf
INFO=		auctex preview-latex
PLIST_SUB=	TEXMFDIR=${TEXMFDIR}
SUB_FILES=	pkg-message
PKGMESSAGE=	${WRKDIR}/pkg-message

OPTIONS_DEFINE=	DOCS
DOCS_CONFIGURE_ON=	--docdir=${DOCSDIR}
DOCS_CONFIGURE_OFF=	WITHOUT_AUCTEX_DOCSDIR=yes

.include <bsd.port.mk>
