SUBDIRS = bash_completion.d dracut initramfs pyzfs zcp
DIST_SUBDIRS = bash_completion.d dracut initramfs pyzfs zcp

install-exec-local:
	make -C zfs-auto-snapshot DESTDIR=$(DESTDIR) PREFIX=$(prefix) install
	rm -fv $(DESTDIR)/etc/cron.*/zfs-auto-snapshot
	rmdir -v $(DESTDIR)/etc/cron.* || echo whatever
