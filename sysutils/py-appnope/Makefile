# $NetBSD: Makefile,v 1.4 2020/12/02 20:00:42 adam Exp $

DISTNAME=	appnope-0.1.2
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	sysutils python
MASTER_SITES=	${MASTER_SITE_PYPI:=a/appnope/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/minrk/appnope
COMMENT=	Disable App Nap on macOS
LICENSE=	modified-bsd

ONLY_FOR_PLATFORM=	Darwin-*-*

# setup.py uses platform, which in turn uses pyexpat in parsing
# SystemVersion.plist on Darwin.
BUILD_DEPENDS+=	${PYPKGPREFIX}-expat-[0-9]*:../../textproc/py-expat

USE_LANGUAGES=	# none

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
