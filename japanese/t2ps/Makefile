# Created by: Yabu Tetsuro <yabu@uopmu.ees.osakafu-u.ac.jp>
# $FreeBSD$

PORTNAME=	t2ps
PORTVERSION=	1.6d
CATEGORIES=	japanese print
MASTER_SITES=	http://www.uopmu.ees.osakafu-u.ac.jp/~yabu/soft/original/
DISTNAME=	t2ps

MAINTAINER=	yabu@uopmu.ees.osakafu-u.ac.jp
COMMENT=	Converts text files to PostScript including Japanese

BROKEN=		unfetchable
DEPRECATED=	Broken for more than 6 months
EXPIRATION_DATE=	2020-05-05

RUN_DEPENDS=	nkf:japanese/nkf

PLIST_FILES=	bin/t2ps
WRKSRC=		${WRKDIR}/t2ps-dir

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/t2ps ${STAGEDIR}${PREFIX}/bin

.include <bsd.port.mk>
