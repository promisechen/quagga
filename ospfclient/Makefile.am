## Automake.am for OSPF API client

AM_CPPFLAGS = -I.. -I$(top_srcdir) -I$(top_srcdir)/lib -I$(top_builddir)/lib
AM_CFLAGS = $(WERROR)

lib_LTLIBRARIES = libospfapiclient.la
libospfapiclient_la_LDFLAGS = -version-info 0:0:0
libospfapiclient_la_LIBADD = ../ospfd/libospf.la ../lib/libzebra.la

sbin_PROGRAMS = ospfclient

libospfapiclient_la_SOURCES = \
	ospf_apiclient.c

ospfapiheaderdir = $(pkgincludedir)/ospfapi

ospfapiheader_HEADERS = \
	ospf_apiclient.h

ospfclient_SOURCES = \
	ospfclient.c

ospfclient_LDADD = libospfapiclient.la \
	../ospfd/libospf.la ../lib/libzebra.la @LIBCAP@

ospfclient_CFLAGS = $(AM_CFLAGS)
ospfclient_LDFLAGS = $(AM_LDFLAGS)
