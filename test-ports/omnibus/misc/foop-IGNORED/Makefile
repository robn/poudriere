# $FreeBSD: head/misc/freebsd-release-manifests/Makefile 429892 2016-12-29 12:41:04Z mat $

PORTNAME=	foop
DISTVERSION=	20161010
PORTREVISION=	0
PKGNAMESUFFIX=	-IGNORED
IGNORE=		ignored
CATEGORIES=	misc
MASTER_SITES=	#
DISTFILES=	#

MAINTAINER=	bdrewery@FreeBSD.org
COMMENT=	FreeBSD release manifests

LICENSE=	BSD2CLAUSE

NO_BUILD=	yes
NO_ARCH=	yes

DATADIR=	${PREFIX}/share/freebsd

do-install:
	@${MKDIR} ${STAGEDIR}${DATADIR}/MANIFESTS
	${INSTALL_DATA} ${FILESDIR}/MANIFESTS/* \
	    ${STAGEDIR}${DATADIR}/MANIFESTS/

.include <bsd.port.mk>
