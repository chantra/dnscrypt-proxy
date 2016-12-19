
sbin_PROGRAMS = \
	dnscrypt-wrapper

dnscrypt_wrapper_SOURCES = \
	cert.c \
	cert.h \
	argparse/argparse.c \
	argparse/argparse.h \
	debug.c \
	debug.h \
	dns-protocol.h \
	dnscrypt.c \
	dnscrypt.h \
	edns.c \
	edns.h \
	logger.c \
	logger.h \
	main.c \
	pidfile.c \
	pidfile.h \
	rfc1035.c \
	rfc1035.h \
	safe_rw.c \
	safe_rw.h \
	tcp_request.c \
	tcp_request.h \
	tree.h \
	udp_request.c \
	udp_request.h

AM_CFLAGS = @CWFLAGS@

AM_CPPFLAGS = \
	-I../ext \
	-I../libevent-modified/include \
	-DPKGDATADIR='"${pkgdatadir}"'

dnscrypt_wrapper_LDADD = \
	../libevent-modified/libevent_extra.la \
	../libevent-modified/libevent_core.la

dnscrypt_wrapper_DEPENDENCIES = \
	../libevent-modified/libevent_extra.la \
	../libevent-modified/libevent_core.la

BUILT_SOURCES = \
	version.h

version.h:
	@./gen-version.sh

CLEANFILES = \
   version.h.in
