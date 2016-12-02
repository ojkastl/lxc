EXTRA_DIST = lxc

if INIT_SCRIPT_SYSV
install-sysvinit: lxc
	$(MKDIR_P) $(DESTDIR)$(sysconfdir)/init.d
	$(INSTALL_SCRIPT) lxc $(DESTDIR)$(sysconfdir)/init.d/lxc

uninstall-sysvinit:
	rm -f $(DESTDIR)$(sysconfdir)/init.d/lxc
	rmdir $(DESTDIR)$(sysconfdir)/init.d || :

install-data-local: install-sysvinit
uninstall-local: uninstall-sysvinit
endif
