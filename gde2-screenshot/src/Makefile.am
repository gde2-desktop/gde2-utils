AM_CPPFLAGS =							\
	-I.							\
	-I$(srcdir)						\
	-DGDE2LOCALEDIR=\""$(prefix)/$(DATADIRNAME)/locale"\"	\
	-DUIDIR=\""$(datadir)/gde2-screenshot"\"

bin_PROGRAMS = gde2-screenshot

gde2_screenshot_SOURCES = \
	gde2-screenshot.c		\
	screenshot-dialog.c		\
	screenshot-dialog.h		\
	screenshot-shadow.c		\
	screenshot-shadow.h		\
	screenshot-utils.c		\
	screenshot-utils.h		\
	screenshot-save.c		\
	screenshot-save.h		\
	screenshot-xfer.c		\
	screenshot-xfer.h

gde2_screenshot_CFLAGS =		\
	$(GLIB_CFLAGS)			\
	$(GIO_CFLAGS)			\
	$(LIBCANBERRA_GTK_CFLAGS)	\
	$(GTHREAD_CFLAGS)		\
	$(GTK_CFLAGS)

gde2_screenshot_LDFLAGS = -export-dynamic

gde2_screenshot_LDADD =		\
	$(XSHAPE_LIBS)			\
	$(GLIB_LIBS)			\
	$(GIO_LIBS)			\
	$(LIBCANBERRA_GTK_LIBS)		\
	$(GTHREAD_LIBS)			\
	$(GTK_LIBS)			\
	-lm

install-exec-local:
	rm -f $(DESTDIR)$(bindir)/gde2-panel-screenshot
	ln -s gde2-screenshot $(DESTDIR)$(bindir)/gde2-panel-screenshot

