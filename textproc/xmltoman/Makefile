# $NetBSD: Makefile,v 1.14 2021/05/24 19:55:01 wiz Exp $
#

DISTNAME=	xmltoman_0.4.orig
PKGNAME=	${DISTNAME:S/_/-/:R}
PKGREVISION=	9
CATEGORIES=	textproc
MASTER_SITES=	${MASTER_SITE_DEBIAN:=pool/main/x/xmltoman/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	# none
COMMENT=	XML to manual page converter

DEPENDS+=	p5-XML-Parser-[0-9]*:../../textproc/p5-XML-Parser

WRKSRC=		${WRKDIR}/${PKGNAME_NOREV}
USE_TOOLS+=	perl:run
USE_LANGUAGES=	# none

AUTO_MKDIRS=		yes
MAKE_ENV+=		PKGBASE=${PKGBASE:Q}
REPLACE_PERL=		xmltoman xmlmantohtml
USE_BSD_MAKEFILE=	yes

post-extract:
	cp ${FILESDIR}/Makefile ${WRKSRC}

.include "../../mk/bsd.pkg.mk"
