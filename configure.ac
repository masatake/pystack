AC_PREREQ([2.69])
AC_INIT([pystack], [1.0], [evan@eklitzke.org])
AC_CONFIG_AUX_DIR([build-aux])
AC_CONFIG_HEADERS([src/config.h])
AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_SRCDIR([src/pystack.cc])

AM_INIT_AUTOMAKE([dist-bzip2 foreign subdir-objects -Wall -Werror])

# Checks for programs.
AC_PROG_CXX
AC_PROG_CC
AC_PROG_INSTALL

AX_CXX_COMPILE_STDCXX_11

# Checks for libraries.

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL

# Checks for library functions.

AC_ARG_WITH([python],
            [AS_HELP_STRING([--with-python], [specify python or python3 @<:@default=python@:>@])],
            [],
            [with_python="python"])

PKG_CHECK_MODULES([PYTHON], ["$with_python"])
AC_SUBST([PYTHON])

AC_CONFIG_FILES([Makefile
                 src/Makefile])
AC_REVISION([m4_esyscmd_s([git describe --always])])
AC_OUTPUT
