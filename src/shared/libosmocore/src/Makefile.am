SUBDIRS=. vty

# This is _NOT_ the library release version, it's an API version.
# Please read Chapter 6 "Library interface versions" of the libtool documentation before making any modification
LIBVERSION=0:0:0

INCLUDES = $(all_includes) -I$(top_srcdir)/include
AM_CFLAGS = -fPIC -Wall

lib_LTLIBRARIES = libosmocore.la

libosmocore_la_SOURCES = timer.c select.c signal.c msgb.c rxlev_stat.c \
			 tlv_parser.c bitvec.c comp128.c gsm_utils.c statistics.c \
			 write_queue.c utils.c rsl.c gsm48.c gsm48_ie.c \
			 logging.c gsm0808.c rate_ctr.c gsmtap_util.c \
			 gprs_cipher_core.c crc16.c panic.c process.c

if ENABLE_PLUGIN
libosmocore_la_SOURCES += plugin.c
libosmocore_la_LDFLAGS = -ldl
endif

if ENABLE_TALLOC
libosmocore_la_SOURCES += talloc.c
endif
