# Created by: aturetta@commit.it
# $FreeBSD$

PORTNAME=	Test-WWW-Mechanize
PORTVERSION=	1.48
CATEGORIES=	devel perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Testing-specific WWW::Mechanize subclass

LICENSE=	ART20

BUILD_DEPENDS=	p5-Carp-Assert-More>=0:devel/p5-Carp-Assert-More \
		p5-HTML-Tree>0:www/p5-HTML-Tree \
		p5-HTTP-Server-Simple>=0.42:www/p5-HTTP-Server-Simple \
		p5-Test-LongString>=0.15:devel/p5-Test-LongString \
		p5-URI>=0:net/p5-URI \
		p5-WWW-Mechanize>=1.68:www/p5-WWW-Mechanize \
		p5-libwww>=6.02:www/p5-libwww
RUN_DEPENDS:=	${BUILD_DEPENDS}

PORTSCOUT=	limit:^[0-9\.]*$$

NO_ARCH=	yes
USES=		perl5
USE_PERL5=	configure

.include <bsd.port.mk>
