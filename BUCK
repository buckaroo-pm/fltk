# TODO: These libs should be ported properly! 

prebuilt_cxx_library(
  name = 'alsa', 
  header_only = True, 
  exported_linker_flags = [
    '-lasound', 
  ], 
)

prebuilt_cxx_library(
  name = 'dl', 
  header_only = True, 
  exported_linker_flags = [
    '-ldl', 
  ], 
)

prebuilt_cxx_library(
  name = 'x11', 
  header_only = True, 
  exported_linker_flags = [
    '-lX11', 
  ], 
)

prebuilt_cxx_library(
  name = 'xext', 
  header_only = True, 
  exported_linker_flags = [
    '-lXext', 
  ], 
)

prebuilt_cxx_library(
  name = 'xinerama', 
  header_only = True, 
  exported_linker_flags = [
    '-lXinerama', 
  ], 
)

prebuilt_cxx_library(
  name = 'xrender', 
  header_only = True, 
  exported_linker_flags = [
    '-lXrender', 
  ], 
)

prebuilt_cxx_library(
  name = 'xcursor', 
  header_only = True, 
  exported_linker_flags = [
    '-lXcursor', 
  ], 
)

prebuilt_cxx_library(
  name = 'xft', 
  header_only = True, 
  exported_linker_flags = [
    '-lXft', 
  ], 
)

prebuilt_cxx_library(
  name = 'xfixes', 
  header_only = True, 
  exported_linker_flags = [
    '-lXfixes', 
  ], 
)

prebuilt_cxx_library(
  name = 'freeimage', 
  header_only = True, 
  exported_linker_flags = [
    '-lfreeimage', 
  ], 
)

prebuilt_cxx_library(
  name = 'freetype', 
  header_only = True, 
  exported_preprocessor_flags = [
    '-I/usr/include/freetype2', 
  ], 
  exported_linker_flags = [
    '-lfreetype', 
  ], 
)

prebuilt_cxx_library(
  name = 'fontconfig', 
  header_only = True, 
  exported_linker_flags = [
    '-lfontconfig', 
  ], 
)

prebuilt_cxx_library(
  name = 'generated', 
  header_namespace = '', 
  header_only = True, 
  exported_platform_headers = [
    ('linux.*', subdir_glob([
      ('generated/linux-x86_64', 'FL/**/*.h'), 
    ])), 
  ], 
)

linux_srcs = glob([
  "src/drivers/Posix/*.cxx",
  "src/drivers/Posix/*.c", 
  "src/drivers/X11/*.cxx",
  "src/drivers/X11/*.c",
  "src/drivers/PostScript/*.cxx", 
  "src/drivers/PostScript/*.c",
])

macos_srcs = glob([
  'src/**/*_mac.cxx', 
])

windows_srcs = glob([
  'src/**/*_win32.c', 
  'src/**/*_win32.cxx', 
  'src/**/*_WIN32.cxx', 
])

platform_srcs = linux_srcs + macos_srcs + windows_srcs

cxx_library(
  name = 'fltk',
  header_namespace = '',
  preprocessor_flags = [
    "-DFL_LIBRARY","-D_FILE_OFFSET_BITS=64","-D_LARGEFILE64_SOURCE",
    "-D_LARGEFILE_SOURCE","-D_THREAD_SAFE","-D_REENTRANT"
  ],
  exported_headers = subdir_glob([
    ("build", "**/*.H"),
    ("build", "**/*.h"),
    ("", "FL/**/*.H"),
    ("", "FL/**/*.h"),
  ]), 
  headers = subdir_glob([
    ("", "src/print_panel.cxx"),
    ("", "src/**/*.H"),
    ("", "src/**/*.h"),
    ("", "src/**/*.c"),
    ("", "src/**/*.xpm"),
    ("", "src/Fl_Native_File_Chooser_GTK.cxx"),
    ("", "src/Fl_Native_File_Chooser_FLTK.cxx"),
    ("", "src/Fl_Native_File_Chooser_common.cxx"),
    ("", "src/fl_font_xft.cxx"),
    ("", "src/fl_set_fonts_xft.cxx"),
    ("", "src/fl_dnd_x.cxx"),
  ]), 
  platform_headers = [
    ('linux.*', subdir_glob([
      ('generated/linux-x86_64', '**/*.h'), 
    ])), 
  ], 
  srcs = glob([
    "src/drivers/Xlib/*.cxx", 
    "src/drivers/Xlib/*.c", 
    "src/drivers/PostScript/*.cxx", 
    "src/drivers/PostScript/*.c",
    "src/drivers/Posix/*.cxx",
    "src/drivers/Posix/*.c", 
    "src/drivers/X11/*.cxx",
    "src/drivers/X11/*.c",
    "src/*.cxx",
    "src/*.c", 
    "src/xutf8/is_right2left.c",
    "src/xutf8/is_spacing.c",
    "src/xutf8/case.c", 
    "src/xutf8/keysym2Ucs.c", 
  ], excludes = platform_srcs + glob([
    "src/print_panel.cxx", 
    'src/fl_font_x.cxx', 
    'src/fl_set_fonts_x.cxx', 
    'src/fl_font_xft.cxx', 
    'src/Fl_Native_File_Chooser_GTK.cxx', 
    'src/fl_set_fonts_xft.cxx', 
  ])), 
  platform_srcs = [
    ('linux.*', linux_srcs), 
    ('macos.*', macos_srcs), 
    ('windows.*', windows_srcs), 
  ], 
  deps = [
    ':generated', 
    '//jpeg:jpeg', 
    '//png:png', 
  ], 
  platform_deps = [
    ('linux.*', [ 
      ':dl', 
      ':alsa', 
      ':x11', 
      ':xinerama', 
      ':xext', 
      ':xrender', 
      ':xft', 
      ':xcursor', 
      ':xfixes', 
      ':freeimage', 
      ':freetype', 
      ':fontconfig', 
    ]), 
  ], 
  visibility = [
    'PUBLIC', 
  ], 
)
