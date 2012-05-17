bin_PROGRAMS = gst-playback-test-0.10

gst_playback_test_0_10_SOURCES = playback-test.c

if USE_QUARTZ
  AM_CPPFLAGS = '-xobjective-c'
endif

LDADD = $(GST_LIBS) $(GTK_LIBS) $(GLIB_LIBS) $(LIBM)

AM_CFLAGS = -I$(top_builddir) $(GST_CFLAGS) $(GTK_CFLAGS) $(GLIB_CFLAGS)
