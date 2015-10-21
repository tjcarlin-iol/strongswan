AUTOMAKE_OPTIONS = foreign

SUBDIRS = properties auth-dialog po

nmvpnservicedir = $(sysconfdir)/NetworkManager/VPN
nmvpnservice_DATA = nm-strongswan-service.name

@INTLTOOL_DESKTOP_RULE@

nm-strongswan-service.name: $(srcdir)/nm-strongswan-service.name.in
	$(AM_V_GEN) \
	sed -e 's|[@]LIBEXECDIR[@]|$(libexecdir)|' \
	    -e 's|[@]CHARON[@]|$(charon)|' $< >$@

EXTRA_DIST = \
    nm-strongswan-service.name.in  \
    intltool-extract.in  \
    intltool-merge.in    \
    intltool-update.in

DISTCLEANFILES = intltool-extract intltool-merge intltool-update

ACLOCAL_AMFLAGS = -I m4
