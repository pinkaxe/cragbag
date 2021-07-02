
AC_INIT([node_net], [0.0.0], [])
#AC_PREREQ([2.61])
AM_INIT_AUTOMAKE([-Wall -Werror foreign subdir-objects])
AC_PROG_CC
AC_PROG_LD
AM_PROG_AR
AC_PROG_LIBTOOL
#AC_PROG_RANLIB

AC_CONFIG_HEADERS([config.h])
AC_CONFIG_FILES([
		Makefile
        log/Makefile
		sys/Makefile
		wrap/Makefile
		db/Makefile
		file/Makefile
		que/Makefile
		ll/Makefile
        bitmap/Makefile
        dpool/Makefile
        link/Makefile
        sbuf/Makefile

        sock_serv/Makefile

		async_runner/Makefile
            ])

AC_ARG_ENABLE(debug, [  --enable-debug            enable debugging
        [[default=yes]]],, enable_debug=yes)
if test x"$enable_debug" = x"yes"; then
    CFLAGS="-O0 -g -pg -fno-inline -Wall "
else
    CFLAGS="-O2 -DNDEBUG "
fi
CFLAGS+=-I$PWD/lib

AC_OUTPUT
