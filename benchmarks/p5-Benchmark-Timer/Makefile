# $NetBSD: Makefile,v 1.13 2021/05/24 19:49:09 wiz Exp $

DISTNAME=	Benchmark-Timer-0.7112
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	5
CATEGORIES=	devel perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Benchmark/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://metacpan.org/release/Benchmark-Timer
COMMENT=	Benchmarking with statistical confidence
LICENSE=	gnu-gpl-v2

#DEPENDS+=	p5-Time-HiRes-[0-9]*:../../time/p5-Time-HiRes
# for make test
BUILD_DEPENDS+=	p5-URI-Escape-XS-[0-9]*:../../www/p5-URI-Escape-XS

PERL5_PACKLIST=		auto/Benchmark/Timer/.packlist
REPLACE_PERL=		delta.pl

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
