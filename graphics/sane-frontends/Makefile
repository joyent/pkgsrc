# $NetBSD: Makefile,v 1.86 2021/04/21 11:41:58 adam Exp $

.include "../../graphics/sane-backends/Makefile.common"
MASTER_SITES=	https://gitlab.com/sane-project/frontends/uploads/14e5c5a9205b10bd3df04501852eab28/

DISTNAME=	sane-frontends-${SANE_VERSION}
SANE_MICRO=	14
PKGREVISION=	49

COMMENT=	Frontends for access to scanners, digital cameras, frame grabbers etc

BUILDLINK_API_DEPENDS.sane+=	sane-backends>=${SANE_VERSION}

USE_TOOLS+=	pkg-config

.include "options.mk"

.include "../../x11/gtk2/buildlink3.mk"
.include "../../graphics/sane-backends/buildlink3.mk"

.include "../../mk/bsd.pkg.mk"
