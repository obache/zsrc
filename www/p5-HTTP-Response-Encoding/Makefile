# $NetBSD: Makefile,v 1.18 2021/05/24 19:55:38 wiz Exp $
#

DISTNAME=	HTTP-Response-Encoding-0.06
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	12
CATEGORIES=	www net perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=HTTP/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://metacpan.org/release/HTTP-Response-Encoding
COMMENT=	Perl5 module to add encoding() to HTTP::Response
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-libwww>=0:../../www/p5-libwww

USE_LANGUAGES=		# empty
PERL5_PACKLIST=		auto/HTTP/Response/Encoding/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
