example_programs =  \
  client_test       \
  stats_counters    \
  dump_torrent      \
  make_torrent      \
  simple_client     \
  upnp_test         \
  bt_get            \
  bt_get2           \
  connection_tester

if ENABLE_EXAMPLES
bin_PROGRAMS = $(example_programs)
endif

EXTRA_PROGRAMS = $(example_programs)
EXTRA_DIST = Jamfile CMakeLists.txt session_view.hpp torrent_view.hpp print.hpp cmake/FindLibtorrentRasterbar.cmake

client_test_SOURCES = client_test.cpp print.cpp session_view.cpp torrent_view.cpp
stats_counters_SOURCES = stats_counters.cpp
bt_get_SOURCES = bt-get.cpp
bt_get2_SOURCES = bt-get2.cpp
bt_get_CXXFLAGS = -std=c++11
bt_get2_CXXFLAGS = -std=c++11
dump_torrent_SOURCES = dump_torrent.cpp
make_torrent_SOURCES = make_torrent.cpp
simple_client_SOURCES = simple_client.cpp
connection_tester_SOURCES = connection_tester.cpp
upnp_test_SOURCES = upnp_test.cpp

LDADD = $(top_builddir)/src/libtorrent-rasterbar.la

AM_CPPFLAGS = -ftemplate-depth-50 -I$(top_srcdir)/include @DEBUGFLAGS@ @OPENSSL_INCLUDES@

AM_LDFLAGS = @BOOST_SYSTEM_LIB@ @OPENSSL_LDFLAGS@ @OPENSSL_LIBS@

