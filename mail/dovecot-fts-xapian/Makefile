# $FreeBSD$

PORTNAME=	fts-xapian
PORTVERSION=	1.3
CATEGORIES=	mail
PKGNAMEPREFIX=	dovecot-

MAINTAINER=	bapt@FreeBSD.org
COMMENT=	Dovecot FTS plugin based on Xapian

LICENSE=	LGPL21

BUILD_DEPENDS=	dovecot>=2.3.7:mail/dovecot
LIB_DEPENDS=	libxapian.so:databases/xapian-core \
		libicuuc.so:devel/icu \
		libsqlite3.so:databases/sqlite3
RUN_DEPENDS=	dovecot>=2.3.7:mail/dovecot

USES=		autoreconf compiler:c++11-lang libtool pkgconfig

USE_LDCONFIG=	yes

USE_GITHUB=yes
GH_ACCOUNT=	grosjo

GNU_CONFIGURE=	yes

PLIST_FILES=	lib/dovecot/lib21_fts_xapian_plugin.a \
		lib/dovecot/lib21_fts_xapian_plugin.so

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/dovecot/lib21_fts_xapian_plugin.so

.include <bsd.port.mk>
