# $NetBSD: Makefile,v 1.13 2021/05/24 19:50:26 wiz Exp $

DISTNAME=	Data-ObjectDriver-0.20
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	1
CATEGORIES=	devel perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Data/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://metacpan.org/release/Data-ObjectDriver
COMMENT=	Simple and generic abstraction to databases
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-Class-Accessor>=0.34:../../devel/p5-Class-Accessor
DEPENDS+=	p5-Class-Data-Inheritable>=0.08:../../devel/p5-Class-Data-Inheritable
DEPENDS+=	p5-Class-Trigger>=0.14:../../devel/p5-Class-Trigger
DEPENDS+=	p5-Text-SimpleTable>=2.0:../../textproc/p5-Text-SimpleTable

# for mke test
BUILD_DEPENDS+=	p5-Test-Exception-[0-9]*:../../devel/p5-Test-Exception

USE_LANGUAGES=		# empty
PERL5_PACKLIST=		auto/Data/ObjectDriver/.packlist
PERL5_MODULE_TYPE=	Module::Build::Tiny

.include "../../databases/p5-DBI/buildlink3.mk"
.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
