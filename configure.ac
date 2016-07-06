AC_INIT(clinfo, 2.1.16.01.12)
AC_CONFIG_SRCDIR([src/clinfo.c])
AM_INIT_AUTOMAKE([foreign])

# Checks for programs.
AC_PROG_CC
AC_PROG_INSTALL
AC_PROG_MAKE_SET

# Checks for libraries.
AM_PROG_LIBTOOL

# Set shared libraries
AC_DISABLE_STATIC
AC_ENABLE_SHARED

# Checks for header files.
AC_CHECK_HEADERS([CL/cl.h],
    [has_opencl_header=yes; break;],
    [AC_MSG_ERROR([Couldn't find OpenCL header])]
)

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.
AC_SEARCH_LIBS([clGetPlatformInfo], [OpenCL],
    [echo "found"; break;],
    [AC_MSG_ERROR([Couldn't find OpenCL library])]
)

AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_FILES([Makefile src/Makefile])
AC_OUTPUT
