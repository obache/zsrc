# $NetBSD: Makefile,v 1.10 2020/01/18 23:36:00 rillig Exp $

DISTNAME=	xdriinfo-1.0.6
CATEGORIES=	x11
MASTER_SITES=	${MASTER_SITE_XORG:=app/}
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://xorg.freedesktop.org/
COMMENT=	X.org DRI information utility

###
### XXX	Prior to this revision, the r300 driver did not export a symbol
###	xdriinfo needs to access its configuration data.  To override
###	this check, you may set USE_ABI_DEPENDS=no.
###
ABI_DEPENDS+=	MesaLib>=7.0.4.1nb3:../../graphics/MesaLib

GNU_CONFIGURE=	yes
USE_TOOLS+=	pkg-config
###
### XXX Should we have a check for DRI drivers in
###	graphics/MesaLib/builtin.mk?
###
.include "../../graphics/MesaLib/buildlink3.mk"
.include "../../x11/xorgproto/buildlink3.mk"
.include "../../x11/libX11/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
