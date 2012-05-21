AC_INIT([playback-test],[0.0.1])

AC_CONFIG_SRCDIR([src/playback-test.c])

AC_PREREQ(2.60)

AC_CANONICAL_TARGET

AM_INIT_AUTOMAKE([-Wall -Werror foreign subdir-objects])
AM_MAINTAINER_MODE

AC_CONFIG_HEADERS([config.h])

m4_ifdef([AM_SILENT_RULES],[AM_SILENT_RULES([yes])],
  [AM_DEFAULT_VERBOSITY=1
   AC_SUBST(AM_DEFAULT_VERBOSITY)])

AC_PROG_CC
AC_PROG_CC_STDC
AC_PROG_CC_C_O
AC_PROG_LIBTOOL
AC_PROG_GREP

AC_C_CONST

AC_HEADER_STDC

AC_CHECK_PROG(HAVE_PKG_CONFIG,pkg-config,yes)

PKG_CHECK_MODULES([GLIB], [glib-2.0 gobject-2.0 gthread-2.0])
PKG_CHECK_MODULES([GST], [gstreamer-0.10 gstreamer-plugins-base-0.10 gstreamer-interfaces-0.10])
PKG_CHECK_MODULES([GTK], [gtk+-2.0])

case "$host" in
  *-*-darwin*)
    use_quartz=yes
    ;;
esac
AM_CONDITIONAL(USE_QUARTZ, test "x$use_quartz" = "xyes")

AC_CONFIG_FILES(
  [Makefile]
  [src/Makefile]
)

AC_OUTPUT

