ACLOCAL_AMFLAGS = -I m4

SUBDIRS = src

doc_DATA = README.rst LICENSE

dist_man_MANS = vmod_cookie.3
MAINTAINERCLEANFILES = $(dist_man_MANS)

%.1 %.2 %.3 %.4 %.5 %.6 %.7 %.8 %.9: README.rst
if HAVE_RST2MAN
	${RST2MAN} $< $@
else
	@echo "========================================"
	@echo "You need rst2man installed to make dist"
	@echo "========================================"
	@false
endif
