# $FreeBSD: head/misc/freebsd-release-manifests/Makefile 429892 2016-12-29 12:41:04Z mat $

PORTNAME=	foo-dep-FLAVORS-unsorted
DISTVERSION=	20161010
PORTREVISION=	0
FLAVORS=	FLAV DEFAULT IGNORED DEPIGNORED
CATEGORIES=	misc
MASTER_SITES=	#
DISTFILES=	#

MAINTAINER=	bdrewery@FreeBSD.org
COMMENT=	FreeBSD release manifests

LICENSE=	BSD2CLAUSE

NO_BUILD=	yes
NO_ARCH=	yes

DATADIR=	${PREFIX}/share/freebsd

.include <bsd.port.options.mk>

.if empty(FLAVOR)
FLAVOR=	DEFAULT
.endif

.if ${FLAVOR} != DEFAULT && !empty(FLAVORS:M${FLAVOR})
PKGNAMESUFFIX=	-${FLAVOR}
.endif
.if ${FLAVOR} == IGNORED
IGNORE=		ignored
.elif ${FLAVOR} == DEPIGNORED
IGNORE=		dep ignored
.endif

do-install:
	@${MKDIR} ${STAGEDIR}${DATADIR}/MANIFESTS
	${INSTALL_DATA} ${FILESDIR}/MANIFESTS/* \
	    ${STAGEDIR}${DATADIR}/MANIFESTS/

.include <bsd.port.mk>
