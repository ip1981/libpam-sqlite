AC_INIT([libpam-sqlite], [0.4], [pashev.igor@gmail.com])
AC_CONFIG_AUX_DIR([build-aux])

AM_INIT_AUTOMAKE

AC_CONFIG_HEADERS([config.h])

AC_PROG_CC
LT_INIT([disable-static])
AC_PROG_LIBTOOL

AC_CONFIG_MACRO_DIR([m4])

AC_CHECK_HEADERS([sqlite.h security/pam_modules.h])
AC_CHECK_LIB([pam], [pam_start], 
     [],
     [AC_MSG_ERROR([PAM not found])]
)
AC_CHECK_LIB([sqlite], [sqlite_open], 
     [],
     [AC_MSG_ERROR([SQLite2 not found])]
)

AC_CONFIG_FILES([
    Makefile
])

AC_OUTPUT

