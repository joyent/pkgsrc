# $NetBSD: Makefile,v 1.9 2021/06/14 15:42:33 taca Exp $

DISTNAME=	kramdown-rfc2629-1.4.15
CATEGORIES=	textproc

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/cabo/kramdown-rfc2629
COMMENT=	IETF RFC 2629 back end for kramdown
LICENSE=	mit

USE_LANGUAGES=	# none

RUBYGEM_OPTIONS+=	--format-executable

#DEPENDS+=	${RUBY_PKGPREFIX}-json_pure>=2.0:../../textproc/ruby-json
DEPENDS+=	${RUBY_PKGPREFIX}-kramdown>=2.3.0<2.4:../../textproc/ruby-kramdown
DEPENDS+=	${RUBY_PKGPREFIX}-certified>=1.0<2:../../security/ruby-certified

.include "../../lang/ruby/gem.mk"
.include "../../mk/bsd.pkg.mk"
