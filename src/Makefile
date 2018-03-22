
.include <bsd.own.mk>

LIB=	sbuf
SRCS=	sbuf.c
HDRS=	sbuf.h 
MAN=	sbuf.3 

includes:
	@cd ${.CURDIR}; for i in ${HDRS}; do \
	  cmp -s $$i ${DESTDIR}/usr/include/$$i || \
	  ${INSTALL} ${INSTALL_COPY} -m 444 -o $(BINOWN) -g $(BINGRP) $$i \
	  ${DESTDIR}/usr/include; done

.include <bsd.lib.mk>
