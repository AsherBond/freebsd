# $FreeBSD$

# Vendor sources and generated files
LDNSDIR= ${.CURDIR}/../../../contrib/ldns
UNBOUNDDIR= ${.CURDIR}/../../../contrib/unbound

.PATH: ${UNBOUNDDIR} ${UNBOUNDDIR}/smallapp ${UNBOUNDDIR}/doc

PROG=	unbound-control
SCRIPTS=	unbound-control-setup.sh
SRCS=	unbound-control.c worker_cb.c
CFLAGS=	-I${UNBOUNDDIR} -I${LDNSDIR}
DPADD=	${LIBUNBOUND} ${LIBLDNS} ${LIBUTIL} ${LIBSSL} ${LIBCRYPTO} ${LIBPTHREAD}
LDADD=	${LDUNBOUND} ${LDLDNS} -lutil -lssl -lcrypto -lpthread
USEPRIVATELIB=	ldns
MAN=	unbound-control.8

.include <bsd.prog.mk>
