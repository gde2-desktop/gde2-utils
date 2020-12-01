icondir = $(datadir)/pixmaps/gde2-search-tool
icon_DATA = thumbnail_frame.png

gsettingsschema_in_files = org.gde2.search-tool.gschema.xml.in
gsettings_SCHEMAS = $(gsettingsschema_in_files:.xml.in=.xml)
.PRECIOUS: $(gsettings_SCHEMAS)

@INTLTOOL_DESKTOP_RULE@

@GSETTINGS_RULES@

@INTLTOOL_XML_RULE@
appdatadir = $(datadir)/appdata
appdata_in_files = gde2-search-tool.appdata.xml.in
appdata_DATA = $(appdata_in_files:.xml.in=.xml)

man_MANS = gde2-search-tool.1

Utilitiesdir = $(datadir)/applications
Utilities_in_files = gde2-search-tool.desktop.in
Utilities_DATA = $(Utilities_in_files:.desktop.in=.desktop)

EXTRA_DIST = \
	$(icon_DATA) \
	$(appdata_in_files) \
	$(Utilities_in_files) \
	$(Utilities_DATA) \
	$(gsettingsschema_in_files) \
	$(man_MANS)

CLEANFILES = \
	gde2-search-tool.appdata.xml \
	gde2-search-tool.desktop \
	$(gsettings_SCHEMAS)

disthook:
	cd $(distdir) ; rm -f $(CLEANFILES)
