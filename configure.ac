#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.67])
AC_INIT([ndnping], [1.1], [yic@email.arizona.edu], [ndnping], [https://github.com/NDN-Routing/ndnping])
AC_CONFIG_AUX_DIR([build-aux])
AM_INIT_AUTOMAKE([foreign -Wall -Werror])
AC_CONFIG_SRCDIR([ndnping.c])

# Checks for programs.
AC_PROG_CC
AM_PROG_CC_C_O

# Checks for libraries.
# FIXME: Replace `main' with a function in `-lm':
AC_CHECK_LIB([m], [main], [], [AC_MSG_ERROR([library math not found.])])

# Checks for libraries.
AX_CHECK_NDN([], AC_MSG_ERROR([NDNx is required to compile PyNDN]))

# Checks for header files.
AC_CHECK_HEADERS([limits.h stdlib.h string.h sys/time.h unistd.h], [], [AC_MSG_ERROR([header file not found.])])
# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_PID_T

# Checks for library functions.
AC_FUNC_FORK
AC_CHECK_FUNCS([gettimeofday memset sqrt strtol])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
