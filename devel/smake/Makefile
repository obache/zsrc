# $NetBSD: Makefile,v 1.16 2021/06/25 10:43:03 micha Exp $

DISTNAME=	schily-2021-06-07
PKGNAME=	smake-1.5
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_SOURCEFORGE:=schilytools/}
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	micha@NetBSD.org
HOMEPAGE=	https://sourceforge.net/projects/schilytools/
COMMENT=	Highly portable UNIX make implementation
LICENSE=	cddl-1.0

MAKE_JOBS_SAFE=	no
MAKE_FLAGS+=	GMAKE_NOWARN=true

USE_TOOLS+=	gmake
MAKE_FLAGS+=	DESTDIR=${DESTDIR} INS_BASE=${PREFIX} DEFMANBASE=. MANDIR=${PKGMANDIR}
# Honor CPPFLAGS, CFLAGS and LDFLAGS
MAKE_FLAGS+=	CPPOPTX=${CPPFLAGS:Q} COPTX=${CFLAGS:Q} LDOPTX=${LDFLAGS:Q}

.include "../../mk/bsd.prefs.mk"

# Platform specific code (for sharing with other packages based on schilytools)
.include "Makefile.common"

SUBST_CLASSES+=		man
SUBST_STAGE.man=	pre-configure
SUBST_FILES.man=	smake/smake.1
SUBST_SED.man=		-e "s,/opt/schily/share/lib/smake/defaults.smk,${PREFIX}/share/lib/smake/defaults.smk,g"
SUBST_MESSAGE.man=	Fix path for default rules in manpage.

do-configure:
	cd ${WRKSRC}/inc && ${MAKE_PROGRAM} ${MAKE_FLAGS}

do-build:
	cd ${WRKSRC}/libschily && ${MAKE_PROGRAM} ${MAKE_FLAGS}
	cd ${WRKSRC}/smake && ${MAKE_PROGRAM} ${MAKE_FLAGS}

# Documentation is in ${WRKSRC}/README.compile
do-install:
	cd ${WRKSRC}/smake && ${MAKE_PROGRAM} ${MAKE_FLAGS} install

.include "../../mk/bsd.pkg.mk"
