gde2_screenshotdir  = $(datadir)/applications
gde2_screenshot_in_files = gde2-screenshot.desktop.in
gde2_screenshot_DATA = $(gde2_screenshot_in_files:.desktop.in=.desktop)
@INTLTOOL_DESKTOP_RULE@

man_MANS = gde2-screenshot.1
uidir = $(datadir)/gde2-screenshot
ui_DATA = gde2-screenshot.ui \
	gde2-screenshot-gtk3.ui

@INTLTOOL_XML_RULE@
appdatadir = $(datadir)/appdata
appdata_in_files = gde2-screenshot.appdata.xml.in
appdata_DATA = $(appdata_in_files:.xml.in=.xml)

gsettings_SCHEMAS = org.gde2.screenshot.gschema.xml
@GSETTINGS_RULES@

EXTRA_DIST =					\
	$(appdata_in_files)			\
	$(gde2_screenshot_in_files)	\
	$(man_MANS)				\
	$(ui_DATA)

CLEANFILES = \
	$(gsettings_SCHEMAS)	\
	$(gde2_screenshot_DATA)	\
	$(appdata_DATA)

dist-hook:
	cd $(distdir) ; rm -f $(CLEANFILES)

install-exec-local:
	rm -f $(DESTDIR)$(mandir)/man1/gde2-panel-screenshot.1
	ln -s gde2-screenshot.1 $(DESTDIR)$(mandir)/man1/gde2-panel-screenshot.1

