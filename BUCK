def merge_dicts(x, y):
  z = x.copy()
  z.update(y)
  return z

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

cxx_library(
  name = 'fltk',
  header_namespace = '',
  compiler_flags = ["-I/usr/include/freetype2"],
  preprocessor_flags = ["-DFL_LIBRARY","-D_FILE_OFFSET_BITS=64","-D_LARGEFILE64_SOURCE","-D_LARGEFILE_SOURCE","-D_THREAD_SAFE","-D_REENTRANT"],
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
  ], excludes = glob([
    'src/**/*_mac.cxx', 
    'src/**/*_win32.c', 
    'src/**/*_win32.cxx', 
    'src/**/*_WIN32.cxx', 
    "src/drivers/Xlib/Fl_Xlib_Graphics_Driver_font_x.cxx", 
    "src/cmap.cxx","src/dump_compose.c",
    "src/Fl_BMP_Image.cxx", 
    "src/fl_call_main.c",
    "src/Fl_File_Icon2.cxx", 
    "src/Fl_GIF_Image.cxx", 
    "src/Fl_Gl_Choice.cxx", 
    "src/Fl_Gl_Device_Plugin.cxx", 
    "src/Fl_Gl_Overlay.cxx", 
    "src/Fl_Gl_Window.cxx", 
    "src/Fl_Help_Dialog.cxx", 
    "src/fl_images_core.cxx", 
    "src/Fl_JPEG_Image.cxx", 
    "src/Fl_PNG_Image.cxx", 
    "src/Fl_PNM_Image.cxx", 
    "src/Fl_SVG_Image.cxx", 
    "src/forms_bitmap.cxx", 
    "src/forms_compatibility.cxx", 
    "src/forms_free.cxx", 
    "src/forms_fselect.cxx", 
    "src/forms_pixmap.cxx", 
    "src/forms_timer.cxx", 
    "src/freeglut_geometry.cxx",
    "src/freeglut_stroke_mono_roman.cxx", 
    "src/freeglut_stroke_roman.cxx", 
    "src/freeglut_teapot.cxx", 
    "src/gl_draw.cxx", 
    "src/gl_start.cxx", 
    "src/glut_compatibility.cxx",
    "src/glut_font.cxx", 
    "src/print_panel.cxx", 
    'src/fl_font_x.cxx', 
    'src/fl_set_fonts_x.cxx', 
    'src/fl_font_xft.cxx', 
    'src/Fl_Native_File_Chooser_GTK.cxx', 
    'src/fl_set_fonts_xft.cxx', 
  ])), 
  deps = [
    ':generated', 
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
    ':fltk_images', 
    ':fltk_forms', 
  ], 
  visibility = [
    'PUBLIC', 
  ], 
)

cxx_library(
  name = 'fltk_images',
  header_namespace = '',
  preprocessor_flags = [
    "-DFL_LIBRARY", 
    "-D_FILE_OFFSET_BITS=64", 
    "-D_LARGEFILE64_SOURCE", 
    "-D_LARGEFILE_SOURCE", 
    "-D_THREAD_SAFE", 
    "-D_REENTRANT", 
  ], 
  headers = subdir_glob([
    ("", "FL/**/*.H"),
    ("", "FL/**/*.h"),
    ("src", "**/*.h"), 
  ]), 
  platform_headers = [
    ('linux.*', subdir_glob([
      ('generated/linux-x86_64', '**/*.h'), 
    ])), 
  ], 
  srcs = glob([
    "src/fl_images_core.cxx", 
    "src/Fl_BMP_Image.cxx", 
    "src/Fl_File_Icon2.cxx", 
    "src/Fl_GIF_Image.cxx", 
    "src/Fl_Help_Dialog.cxx", 
    "src/Fl_JPEG_Image.cxx", 
    "src/Fl_PNG_Image.cxx", 
    "src/Fl_PNM_Image.cxx", 
    "src/Fl_SVG_Image.cxx", 
  ]), 
  deps = [
    ':generated', 
    ':freetype', 
    '//jpeg:jpeg', 
    '//png:png', 
    ':fltk_forms', 
  ], 
  visibility = [
    'PUBLIC', 
  ], 
)

cxx_library(
  name = "fltk_forms",
  header_namespace = '',
  preprocessor_flags = [
    "-DFL_LIBRARY", 
    "-D_FILE_OFFSET_BITS=64", 
    "-D_LARGEFILE64_SOURCE", 
    "-D_LARGEFILE_SOURCE", 
    "-D_THREAD_SAFE", 
    "-D_REENTRANT", 
  ],
  headers = subdir_glob([
    ("", "FL/**/*.H"),
    ("", "FL/**/*.h"),
    ("", "src/**/*.h"),
  ]), 
  platform_headers = [
    ('linux.*', subdir_glob([
      ('generated/linux-x86_64', '**/*.h'), 
    ])), 
  ], 
  srcs = glob([
    "src/forms_compatibility.cxx", 
    "src/forms_bitmap.cxx", 
    "src/forms_free.cxx", 
    "src/forms_fselect.cxx", 
    "src/forms_pixmap.cxx", 
    "src/forms_timer.cxx", 
  ]), 
  deps = [
    ':generated', 
    ':freetype', 
  ],
  visibility = [
    'PUBLIC', 
  ], 
)

cxx_library(
  name = 'fltk_gl',
  header_namespace = '',
  preprocessor_flags = [
    "-DFL_LIBRARY", 
    "-D_FILE_OFFSET_BITS=64", 
    "-D_LARGEFILE64_SOURCE", 
    "-D_LARGEFILE_SOURCE", 
    "-D_THREAD_SAFE", 
    "-D_REENTRANT", 
  ],
  headers = subdir_glob([
    ("build", "**/*.H"),
  ]), 
  srcs = glob(
    ["src/drivers/OpenGL/*.cxx","src/Fl_Gl_Choice.cxx","src/Fl_Gl_Device_Plugin.cxx","src/Fl_Gl_Overlay.cxx","src/Fl_Gl_Window.cxx","src/freeglut_geometry.cxx","src/freeglut_stroke_mono_roman.cxx","src/freeglut_stroke_roman.cxx","src/freeglut_teapot.cxx","src/gl_draw.cxx","src/gl_start.cxx","src/glut_compatibility.cxx","src/glut_font.cxx"],
    excludes = ["src/drivers/OpenGL/Fl_OpenGL_Graphics_Driver.cxx"],
    include_dotfiles=False
  ) + [
    
  ],
  linker_flags = [],
  exported_linker_flags = [],
  deps = [
    ':freetype', 
  ],
  visibility = [
    'PUBLIC', 
  ], 
)


genrule(
  name = 'gen-build-test-keyboard_ui-cxx', 
  out = 'keyboard_ui.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-79607aa99ba92939226d8e980fa71fa04a059912)/build/test/keyboard_ui.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-keyboard_ui-h', 
  out = 'keyboard_ui.H', 
  cmd = 'cd $TMP && cp $(location :gen-79607aa99ba92939226d8e980fa71fa04a059912)/build/test/keyboard_ui.H $OUT', 
)

genrule(
  name = 'gen-6d1a40675dded6fd047f0f622e3e606eb27d0c9e', 
  out = 'out', 
  srcs = glob(
    ["test/inactive.fl"],
    excludes = [],
    include_dotfiles=False
  ),
  cmd = 'mkdir -p $OUT && cp -r $SRCDIR/. $TMP && cd $TMP && mkdir -p $TMP/build/test && cd build && cd $TMP/build/test && ../bin/fluid -c $TMP/test/inactive.fl && mkdir -p $OUT/build/test && cp $TMP/build/test/inactive.cxx $OUT/build/test/inactive.cxx && cp $TMP/build/test/inactive.H $OUT/build/test/inactive.H', 
)

genrule(
  name = 'gen-build-test-inactive-cxx', 
  out = 'inactive.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-6d1a40675dded6fd047f0f622e3e606eb27d0c9e)/build/test/inactive.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-inactive-h', 
  out = 'inactive.H', 
  cmd = 'cd $TMP && cp $(location :gen-6d1a40675dded6fd047f0f622e3e606eb27d0c9e)/build/test/inactive.H $OUT', 
)

genrule(
  name = 'gen-51caacd8ccbfeddb215d55b0f3de7db606444c51', 
  out = 'out', 
  srcs = glob(
    ["test/fast_slow.fl"],
    excludes = [],
    include_dotfiles=False
  ),
  cmd = 'mkdir -p $OUT && cp -r $SRCDIR/. $TMP && cd $TMP && mkdir -p $TMP/build/test && cd build && cd $TMP/build/test && ../bin/fluid -c $TMP/test/fast_slow.fl && mkdir -p $OUT/build/test && cp $TMP/build/test/fast_slow.cxx $OUT/build/test/fast_slow.cxx && cp $TMP/build/test/fast_slow.H $OUT/build/test/fast_slow.H', 
)

genrule(
  name = 'gen-build-test-fast_slow-cxx', 
  out = 'fast_slow.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-51caacd8ccbfeddb215d55b0f3de7db606444c51)/build/test/fast_slow.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-fast_slow-h', 
  out = 'fast_slow.H', 
  cmd = 'cd $TMP && cp $(location :gen-51caacd8ccbfeddb215d55b0f3de7db606444c51)/build/test/fast_slow.H $OUT', 
)

genrule(
  name = 'gen-7fdd4b6900f1ec8de8d6de9060e37943950036bd', 
  out = 'out', 
  srcs = glob(
    ["test/valuators.fl"],
    excludes = [],
    include_dotfiles=False
  ),
  cmd = 'mkdir -p $OUT && cp -r $SRCDIR/. $TMP && cd $TMP && mkdir -p $TMP/build/test && cd build && cd $TMP/build/test && ../bin/fluid -c $TMP/test/valuators.fl && mkdir -p $OUT/build/test && cp $TMP/build/test/valuators.cxx $OUT/build/test/valuators.cxx && cp $TMP/build/test/valuators.H $OUT/build/test/valuators.H', 
)

genrule(
  name = 'gen-build-test-valuators-cxx', 
  out = 'valuators.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-7fdd4b6900f1ec8de8d6de9060e37943950036bd)/build/test/valuators.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-valuators-h', 
  out = 'valuators.H', 
  cmd = 'cd $TMP && cp $(location :gen-7fdd4b6900f1ec8de8d6de9060e37943950036bd)/build/test/valuators.H $OUT', 
)

genrule(
  name = 'gen-70a45d7eda7b38cbb875a24455e42fc561b0d19e', 
  out = 'out', 
  srcs = glob(
    ["test/preferences.fl"],
    excludes = [],
    include_dotfiles=False
  ),
  cmd = 'mkdir -p $OUT && cp -r $SRCDIR/. $TMP && cd $TMP && mkdir -p $TMP/build/test && cd build && cd $TMP/build/test && ../bin/fluid -c $TMP/test/preferences.fl && mkdir -p $OUT/build/test && cp $TMP/build/test/preferences.cxx $OUT/build/test/preferences.cxx && cp $TMP/build/test/preferences.H $OUT/build/test/preferences.H', 
)

genrule(
  name = 'gen-build-test-preferences-cxx', 
  out = 'preferences.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-70a45d7eda7b38cbb875a24455e42fc561b0d19e)/build/test/preferences.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-preferences-h', 
  out = 'preferences.H', 
  cmd = 'cd $TMP && cp $(location :gen-70a45d7eda7b38cbb875a24455e42fc561b0d19e)/build/test/preferences.H $OUT', 
)

genrule(
  name = 'gen-ead1f1742c4c0acda872ecbb56c825751818af2b', 
  out = 'out', 
  srcs = glob(
    ["test/resize.fl"],
    excludes = [],
    include_dotfiles=False
  ),
  cmd = 'mkdir -p $OUT && cp -r $SRCDIR/. $TMP && cd $TMP && mkdir -p $TMP/build/test && cd build && cd $TMP/build/test && ../bin/fluid -c $TMP/test/resize.fl && mkdir -p $OUT/build/test && cp $TMP/build/test/resize.cxx $OUT/build/test/resize.cxx && cp $TMP/build/test/resize.H $OUT/build/test/resize.H', 
)

genrule(
  name = 'gen-build-test-resize-cxx', 
  out = 'resize.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-ead1f1742c4c0acda872ecbb56c825751818af2b)/build/test/resize.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-resize-h', 
  out = 'resize.H', 
  cmd = 'cd $TMP && cp $(location :gen-ead1f1742c4c0acda872ecbb56c825751818af2b)/build/test/resize.H $OUT', 
)

genrule(
  name = 'gen-05e100338dc46933003c97166228ae4b2da9f8fa', 
  out = 'out', 
  srcs = glob(
    ["test/mandelbrot_ui.fl"],
    excludes = [],
    include_dotfiles=False
  ),
  cmd = 'mkdir -p $OUT && cp -r $SRCDIR/. $TMP && cd $TMP && mkdir -p $TMP/build/test && cd build && cd $TMP/build/test && ../bin/fluid -c $TMP/test/mandelbrot_ui.fl && mkdir -p $OUT/build/test && cp $TMP/build/test/mandelbrot_ui.cxx $OUT/build/test/mandelbrot_ui.cxx && cp $TMP/build/test/mandelbrot_ui.H $OUT/build/test/mandelbrot_ui.H', 
)

genrule(
  name = 'gen-build-test-mandelbrot_ui-cxx', 
  out = 'mandelbrot_ui.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-05e100338dc46933003c97166228ae4b2da9f8fa)/build/test/mandelbrot_ui.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-mandelbrot_ui-h', 
  out = 'mandelbrot_ui.H', 
  cmd = 'cd $TMP && cp $(location :gen-05e100338dc46933003c97166228ae4b2da9f8fa)/build/test/mandelbrot_ui.H $OUT', 
)

genrule(
  name = 'gen-c07ad90f80cac7e406e92b7d070ae81362eaf25d', 
  out = 'out', 
  srcs = glob(
    ["test/tabs.fl"],
    excludes = [],
    include_dotfiles=False
  ),
  cmd = 'mkdir -p $OUT && cp -r $SRCDIR/. $TMP && cd $TMP && mkdir -p $TMP/build/test && cd build && cd $TMP/build/test && ../bin/fluid -c $TMP/test/tabs.fl && mkdir -p $OUT/build/test && cp $TMP/build/test/tabs.cxx $OUT/build/test/tabs.cxx && cp $TMP/build/test/tabs.H $OUT/build/test/tabs.H', 
)

genrule(
  name = 'gen-build-test-tabs-cxx', 
  out = 'tabs.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-c07ad90f80cac7e406e92b7d070ae81362eaf25d)/build/test/tabs.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-tabs-h', 
  out = 'tabs.H', 
  cmd = 'cd $TMP && cp $(location :gen-c07ad90f80cac7e406e92b7d070ae81362eaf25d)/build/test/tabs.H $OUT', 
)

genrule(
  name = 'gen-3e9fee784c9ecbe5272e2106796fd379e1fa9ef5', 
  out = 'out', 
  srcs = glob(
    ["test/tree.fl"],
    excludes = [],
    include_dotfiles=False
  ),
  cmd = 'mkdir -p $OUT && cp -r $SRCDIR/. $TMP && cd $TMP && mkdir -p $TMP/build/test && cd build && cd $TMP/build/test && ../bin/fluid -c $TMP/test/tree.fl && mkdir -p $OUT/build/test && cp $TMP/build/test/tree.cxx $OUT/build/test/tree.cxx && cp $TMP/build/test/tree.H $OUT/build/test/tree.H', 
)

genrule(
  name = 'gen-build-test-tree-cxx', 
  out = 'tree.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-3e9fee784c9ecbe5272e2106796fd379e1fa9ef5)/build/test/tree.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-tree-h', 
  out = 'tree.H', 
  cmd = 'cd $TMP && cp $(location :gen-3e9fee784c9ecbe5272e2106796fd379e1fa9ef5)/build/test/tree.H $OUT', 
)

genrule(
  name = 'gen-f84ffcd3e3dd639ecc0a6a74ecdce88c15bd708e', 
  out = 'out', 
  srcs = glob(
    ["test/CubeViewUI.fl"],
    excludes = [],
    include_dotfiles=False
  ),
  cmd = 'mkdir -p $OUT && cp -r $SRCDIR/. $TMP && cd $TMP && mkdir -p $TMP/build/test && cd build && cd $TMP/build/test && ../bin/fluid -c $TMP/test/CubeViewUI.fl && mkdir -p $OUT/build/test && cp $TMP/build/test/CubeViewUI.cxx $OUT/build/test/CubeViewUI.cxx && cp $TMP/build/test/CubeViewUI.H $OUT/build/test/CubeViewUI.H', 
)

genrule(
  name = 'gen-build-test-cubeviewui-cxx', 
  out = 'CubeViewUI.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-f84ffcd3e3dd639ecc0a6a74ecdce88c15bd708e)/build/test/CubeViewUI.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-cubeviewui-h', 
  out = 'CubeViewUI.H', 
  cmd = 'cd $TMP && cp $(location :gen-f84ffcd3e3dd639ecc0a6a74ecdce88c15bd708e)/build/test/CubeViewUI.H $OUT', 
)

genrule(
  name = 'gen-c727f5da2a04ca03e4c7e0c8103f2ac6e1adfaea', 
  out = 'out', 
  srcs = glob(
    ["test/radio.fl"],
    excludes = [],
    include_dotfiles=False
  ),
  cmd = 'mkdir -p $OUT && cp -r $SRCDIR/. $TMP && cd $TMP && mkdir -p $TMP/build/test && cd build && cd $TMP/build/test && ../bin/fluid -c $TMP/test/radio.fl && mkdir -p $OUT/build/test && cp $TMP/build/test/radio.cxx $OUT/build/test/radio.cxx && cp $TMP/build/test/radio.H $OUT/build/test/radio.H', 
)

genrule(
  name = 'gen-build-test-radio-cxx', 
  out = 'radio.cxx', 
  cmd = 'cd $TMP && cp $(location :gen-c727f5da2a04ca03e4c7e0c8103f2ac6e1adfaea)/build/test/radio.cxx $OUT', 
)

genrule(
  name = 'gen-build-test-radio-h', 
  out = 'radio.H', 
  cmd = 'cd $TMP && cp $(location :gen-c727f5da2a04ca03e4c7e0c8103f2ac6e1adfaea)/build/test/radio.H $OUT', 
)
