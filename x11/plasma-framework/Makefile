# $NetBSD: Makefile,v 1.48 2021/04/21 11:40:49 adam Exp $

DISTNAME=	plasma-framework-${KF5VER}
PKGREVISION=	1
CATEGORIES=	x11

HOMEPAGE=	https://community.kde.org/Frameworks
COMMENT=	Plasma library and runtime components based upon KF5 and Qt5
LICENSE=	gnu-gpl-v2 AND gnu-lgpl-v2.1

.include "../../meta-pkgs/kde/kf5.mk"

BUILD_DEPENDS+=	kdoctools>=${KF5VER}:../../devel/kdoctools

USE_TOOLS+=	gmake msgmerge pkg-config

SUBST_CLASSES+=		fix-moc
SUBST_STAGE.fix-moc=	post-configure
SUBST_MESSAGE.fix-moc=	Cleaning up MOC includes
SUBST_FILES.fix-moc=	_KDE_build/src/scriptengines/qml/CMakeFiles/plasma_appletscript_declarative_autogen.dir/AutogenInfo.json
SUBST_NOOP_OK.fix-moc=	yes
SUBST_SED.fix-moc=	-e 's;"${PREFIX}/include",;;g'

.include "../../devel/kdeclarative/buildlink3.mk"
.include "../../devel/kwayland/buildlink3.mk"
.include "../../x11/kactivities5/buildlink3.mk"
.include "../../x11/kirigami2/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../x11/qt5-qtquickcontrols/buildlink3.mk"
.include "../../x11/qt5-qttools/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
