# $NetBSD: Makefile,v 1.25 2021/05/24 19:49:02 wiz Exp $

DISTNAME=	fastjar-0.98
PKGREVISION=	2
CATEGORIES=	archivers
MASTER_SITES=	http://download.savannah.gnu.org/releases/fastjar/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://savannah.nongnu.org/projects/fastjar
COMMENT=	C language version of the 'jar' archiver normally used by Java
LICENSE=	gnu-gpl-v2

GNU_CONFIGURE=	YES
TOOLS_BROKEN=	perl

INFO_FILES=		YES
INSTALLATION_DIRS=	${PKGMANDIR}/man1

post-install:
	${INSTALL_MAN} ${WRKSRC}/fastjar.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1
	${INSTALL_MAN} ${WRKSRC}/grepjar.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1

.include "../../devel/zlib/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
