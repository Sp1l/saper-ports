# $FreeBSD: head/lang/neko/Makefile 430235 2017-01-01 03:45:12Z sunpoet $

PORTNAME=	neko
PORTVERSION=	2.2.0
CATEGORIES=	lang

MAINTAINER=	penzin.dev@gmail.com
COMMENT=	Neko programming languages and virtual machine

LICENSE=	MIT

BUILD_DEPENDS=	${LOCALBASE}/bin/git:devel/git ${LOCALBASE}/include/apache22/httpd.h:www/apache22
LIB_DEPENDS=	libgc-threaded.so:devel/boehm-gc-threaded \
		libapr-1.so:devel/apr1 libaprutil-1.so:devel/apr1 \
		libpcre.so:devel/pcre libpcreposix.so:devel/pcre \
		libmbedtls.so:security/mbedtls libmbedcrypto.so:security/mbedtls libmbedx509.so:security/mbedtls \
		libfontconfig.so:x11-fonts/fontconfig libfreetype.so:print/freetype2

USES=		cmake pkgconfig sqlite:3 mysql

USE_GNOME=	atk cairo gdkpixbuf2 glib20 gtk20 pango
USE_GITHUB=	yes
GH_ACCOUNT=	HaxeFoundation
# GH_PROJECT is the same as port name
GH_TAGNAME=	v${PORTVERSION:S/./-/g}

USE_LDCONFIG=	${PREFIX}/lib ${PREFIX}/lib/neko

MAKE_JOBS_UNSAFE=yes

.include <bsd.port.mk>
