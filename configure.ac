AC_PREREQ(2.63)
AC_INIT([gnome-weather],[0.2],
	[https://bugzilla.gnome.org/enter_bug.cgi?product=gnome-weather],
	[gnome-weather],
	[https://live.gnome.org/Design/Apps/Weather])

AC_CONFIG_HEADERS([config.h])
AC_CONFIG_MACRO_DIR([m4])

AM_INIT_AUTOMAKE([1.11 dist-xz foreign tar-ustar -Wno-portability])

m4_ifdef([AM_SILENT_RULES],[AM_SILENT_RULES([yes])])

GETTEXT_PACKAGE=gnome-weather
AC_SUBST(GETTEXT_PACKAGE)
AC_DEFINE_UNQUOTED(GETTEXT_PACKAGE, "$GETTEXT_PACKAGE",
                   [The prefix for our gettext translation domains.])
IT_PROG_INTLTOOL(0.26)

AC_PROG_CC
AM_PROG_CC_C_O
LT_INIT([disable-static])

LIBGD_INIT([header-bar main-toolbar main-view stack revealer gir])

PKG_PROG_PKG_CONFIG([0.22])

GLIB_GSETTINGS
GOBJECT_INTROSPECTION_REQUIRE([1.30.0])

AC_PATH_PROG([GJS],[gjs])

AC_CONFIG_FILES([
  Makefile
  data/Makefile
  libgd/Makefile
  src/Makefile
  po/Makefile.in
])
AC_OUTPUT
