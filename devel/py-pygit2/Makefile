# Created by: William Grzybowski <wg@FreeBSD.org>
# $FreeBSD: head/devel/py-pygit2/Makefile 442373 2017-06-02 11:03:31Z araujo $

# Also update devel/libgit2, devel/libgit2-glib, devel/rubygem-rugged

PORTNAME=	pygit2
PORTVERSION=	1.2.0
CATEGORIES=	devel python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	mfechner@FreeBSD.org
COMMENT=	Python bindings for libgit2

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

MY_DEPENDS=	${PYTHON_PKGNAMEPREFIX}cffi>1.0:devel/py-cffi@${PY_FLAVOR}
BUILD_DEPENDS=	${MY_DEPENDS}
LIB_DEPENDS=	libgit2.so:devel/libgit2
RUN_DEPENDS=	${MY_DEPENDS} \
		${PYTHON_PKGNAMEPREFIX}six>0:devel/py-six@${PY_FLAVOR}

USES=		python:3.5+
USE_PYTHON=	autoplist distutils
MAKE_ENV=	LIBGIT2=${LOCALBASE}
PYDISTUTILS_TEST_TARGET?=	test

do-test:
	@(cd ${BUILD_WRKSRC}; ${SETENV} ${MAKE_ENV} ${PYTHON_CMD} ${PYDISTUTILS_SETUP} ${PYDISTUTILS_TEST_TARGET} ${PYDISTUTILS_TESTARGS})

post-install:
	${STRIP_CMD} ${STAGEDIR}${PYTHON_SITELIBDIR}/pygit2/_*git2*.so \

.include <bsd.port.mk>
