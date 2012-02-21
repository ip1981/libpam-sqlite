lib_LTLIBRARIES = pam_sqlite.la

pam_sqlite_la_SOURCES = \
	pam_get_pass.c \
	pam_get_service.c \
	pam_sqlite.c \
	pam_std_option.c \
	pam_mod_misc.h

pam_sqlite_la_LDFLAGS = -module -avoid-version -no-undefined

dist_EXTRA = test.c

