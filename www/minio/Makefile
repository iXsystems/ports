# $FreeBSD: head/www/minio/Makefile 465252 2018-03-22 00:14:04Z swills $

PORTNAME=	minio
PORTVERSION=	${GH_TAGNAME:S/RELEASE.//:S/Z//:S/T/-/:S/-/./g}
CATEGORIES=	www

MAINTAINER=	swills@FreeBSD.org
COMMENT=	Amazon S3 compatible object storage server

LICENSE=	APACHE20

BUILD_DEPENDS=	go>=1.7:lang/go

USES=		compiler

USE_GITHUB=	yes
GH_TAGNAME=	RELEASE.2018-04-04T05-20-54Z
GH_SUBDIR=	src/github.com/${PORTNAME}/${PORTNAME}
COMMIT_ID=	85a57d20210eb867b1c023e024cc4391d5ac5685

PLIST_FILES=	bin/minio

USE_RC_SUBR=	minio

USERS=		minio
GROUPS=		minio

SUB_LIST=	USER="${USERS}" \
		GROUP="${GROUPS}"

do-build:
	@cd ${WRKSRC}/${GH_SUBDIR} ; \
	${SETENV} ${MAKE_ENV} GOPATH=${WRKSRC} CGO_ENABLED=0 go build \
		--ldflags '-X github.com/minio/minio/cmd.Version=${GH_TAGNAME:C/RELEASE\.//:C|(..)-(..)-(..)Z|\1:\2:\3Z|} -X github.com/minio/minio/cmd.ReleaseTag=${GH_TAGNAME} -X github.com/minio/minio/cmd.CommitID=${COMMIT_ID} -X github.com/minio/minio/cmd.GOPATH=${WRKSRC} -s -w' -o ${WRKSRC}/bin/minio

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/bin/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
