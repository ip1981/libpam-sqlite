AC_INIT([libpam-sqlite], [0.4], [pashev.igor@gmail.com])
AC_CONFIG_AUX_DIR([build-aux])

AM_INIT_AUTOMAKE

AC_CONFIG_HEADERS([config.h])

AC_PROG_CC_C99
LT_INIT([disable-static])

AC_CONFIG_MACRO_DIR([m4])

AC_CHECK_HEADERS(
    [sqlite3.h security/pam_appl.h],
    [],
    [AC_MSG_ERROR(Required headers not found)]
)

dnl On Illumos pam_appl.h must be included before pam_modules.h
AC_CHECK_HEADER(
    [security/pam_modules.h],
    [],
    [AC_MSG_ERROR([Required headers not found])],
    [
     #include <security/pam_appl.h>
    ]
)


AC_CHECK_LIB(
    [pam], [pam_start], 
    [],
    [AC_MSG_ERROR([PAM not found])]
)
AC_CHECK_LIB(
    [sqlite3], [sqlite3_open], 
    [],
    [AC_MSG_ERROR([SQLite3 not found])]
)

AC_SEARCH_LIBS([crypt], [crypt])

AC_CONFIG_FILES([
    Makefile
])

AC_OUTPUT

