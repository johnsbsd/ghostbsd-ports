# $FreeBSD$

PORTNAME=	trueos-server
PORTVERSION=	201807060938
CATEGORIES=	misc
MASTER_SITES=
DISTFILES=

MAINTAINER=	jmaloney@ixsystems.com
COMMENT=	TrueOS Server

RUN_DEPENDS=	trueos-core>=0:misc/trueos-core \
		${LOCALBASE}/bin/sudo:security/sudo \
		${LOCALBASE}/bin/zsh:shells/zsh \
		${LOCALBASE}/bin/rsync:net/rsync \
		${LOCALBASE}/bin/screen:sysutils/screen \
		${LOCALBASE}/bin/tmux:sysutils/tmux \
		${LOCALBASE}/bin/nano:editors/nano

CONFLICTS=	pcbsd-utils-[0-9]* trueos-desktop-[0-9]*
WRKSRC_SUBDIR=	package-files
MAKE_ARGS=	STAGEDIR=${STAGEDIR}  TYPE=server

USE_GITHUB=     yes
GH_ACCOUNT=     trueos
GH_PROJECT=     trueos-core
GH_TAGNAME=     91f61348b8ee29fc4cc688eca4d56b669867ebf6

.include <bsd.port.mk>
