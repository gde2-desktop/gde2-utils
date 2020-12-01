NULL =

AM_CPPFLAGS = \
	-DPREFIX=\""$(prefix)"\"			\
	-DSYSCONFDIR=\""$(sysconfdir)"\"		\
	-DLIBDIR=\""$(libdir)"\"			\
	-DDATADIR=\""$(datadir)"\" 			\
	-DPKGDATADIR=\""$(datadir)/gde2-dictionary"\" 	\
	-DGDE2LOCALEDIR=\""$(prefix)/$(DATADIRNAME)/locale"\" \
	$(NULL)

bin_PROGRAMS = gde2-dictionary

if BUILD_GDICT_APPLET
libexec_PROGRAMS = gde2-dictionary-applet
endif

gde2_dictionary_SOURCES = \
	gdict-about.c		\
	gdict-about.h		\
	gdict-app.c		\
	gdict-app.h		\
	gdict-common.c 		\
	gdict-common.h		\
	gdict-pref-dialog.c	\
	gdict-pref-dialog.h	\
	gdict-print.c 		\
	gdict-print.h 		\
	gdict-sidebar.c		\
	gdict-sidebar.h		\
	gdict-source-dialog.c 	\
	gdict-source-dialog.h 	\
	gdict-window.c 		\
	gdict-window.h 		\
	main.c			\
	$(NULL)

gde2_dictionary_CFLAGS = \
	-I$(top_builddir)/gde2-dictionary \
	-I$(top_srcdir)/gde2-dictionary \
	$(GLIB_CFLAGS) \
	$(GIO_CFLAGS) \
	$(GTK_CFLAGS) \
	$(NULL)

gde2_dictionary_LDADD = \
	-lm			\
	$(top_builddir)/gde2-dictionary/libgdict/libgde2dict.la \
	$(GLIB_LIBS) \
	$(GIO_LIBS) \
	$(GTK_LIBS) \
	$(NULL)

if BUILD_GDICT_APPLET

gde2_dictionary_applet_SOURCES = \
	gdict-about.c 		\
	gdict-about.h		\
	gdict-aligned-window.c	\
	gdict-aligned-window.h	\
	gdict-applet.c		\
	gdict-applet.h		\
	gdict-common.c		\
	gdict-common.h		\
	gdict-pref-dialog.c	\
	gdict-pref-dialog.h	\
	gdict-print.c 		\
	gdict-print.h 		\
	gdict-sidebar.c		\
	gdict-sidebar.h		\
	gdict-source-dialog.c 	\
	gdict-source-dialog.h 	\
	$(NULL)

gde2_dictionary_applet_CFLAGS = \
	-I$(top_builddir)/gde2-dictionary \
	-I$(top_srcdir)/gde2-dictionary \
	$(APPLET_CFLAGS) \
	$(GLIB_CFLAGS) \
	$(GIO_CFLAGS) \
	$(GTK_CFLAGS) \
	$(NULL)

gde2_dictionary_applet_LDADD = \
	-lm			\
	$(top_builddir)/gde2-dictionary/libgdict/libgde2dict.la \
	$(APPLET_LIBS) \
	$(GLIB_LIBS) \
	$(GIO_LIBS) \
	$(GTK_LIBS) \
	$(NULL)

endif # BUILD_GDICT_APPLET
