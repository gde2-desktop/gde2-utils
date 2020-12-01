AM_CPPFLAGS = \
	-I$(top_srcdir)/gsearchtool/libeggsmclient \
	-I$(top_srcdir)/gsearchtool/libgde2ui-deprecated \
	-DGDE2LOCALEDIR=\""$(prefix)/$(DATADIRNAME)/locale"\" \
	-DLOCALEDIR=\"$(datadir)/locale\" \
	-DDATADIR=\""$(datadir)"\" \
	-DGREP_COMMAND=\""$(GREP_COMMAND)"\"

libeggsmclient_LIB = $(top_builddir)/gsearchtool/libeggsmclient/libeggsmclient.la
libgde2ui_deprecated_LIB = $(top_builddir)/gsearchtool/libgde2ui-deprecated/libgde2ui-deprecated.la

bin_PROGRAMS = gde2-search-tool

gde2_search_tool_SOURCES = \
	gsearchtool-support.c \
	gsearchtool-support.h \
	gsearchtool-callbacks.c \
	gsearchtool-callbacks.h \
	gsearchtool.c \
	gsearchtool.h

gde2_search_tool_CFLAGS = \
	$(GLIB_CFLAGS) \
	$(GIO_CFLAGS) \
	$(GIO_UNIX_CFLAGS) \
	$(GTK_CFLAGS)

gde2_search_tool_LDADD = \
	$(GLIB_LIBS) \
	$(GIO_LIBS) \
	$(GIO_UNIX_LIBS) \
	$(GTK_LIBS) \
	$(libeggsmclient_LIB) \
	$(libgde2ui_deprecated_LIB)

