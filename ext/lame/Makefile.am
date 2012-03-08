plugin_LTLIBRARIES = libgstlame.la

libgstlame_la_SOURCES = gstlame.c gstlamemp3enc.c plugin.c
libgstlame_la_CFLAGS = -DGST_USE_UNSTABLE_API \
        $(GST_PLUGINS_BASE_CFLAGS) $(GST_BASE_CFLAGS) $(GST_CFLAGS) $(LAME_CFLAGS)
libgstlame_la_LIBADD = $(GST_PLUGINS_BASE_LIBS) -lgstaudio-$(GST_MAJORMINOR) \
	$(GST_BASE_LIBS) $(GST_LIBS) $(LAME_LIBS)
libgstlame_la_LDFLAGS = $(GST_PLUGIN_LDFLAGS)
if !GST_PLUGIN_BUILD_STATIC
libgstlame_la_LIBTOOLFLAGS = --tag=disable-static
endif

noinst_HEADERS = gstlame.h gstlamemp3enc.h
