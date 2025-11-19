devkit_outputs = [
  'ainakan-gumjs.h',
  static_lib_prefix + 'ainakan-gumjs' + static_lib_suffix,
  'ainakan-gumjs-example.c',
]

if cc.get_argument_syntax() == 'msvc'
  devkit_outputs += [
    'ainakan-gumjs-example.sln',
    'ainakan-gumjs-example.vcxproj',
    'ainakan-gumjs-example.vcxproj.filters',
  ]
endif

custom_target('gumjs-devkit',
  input: [gum, gum_heap, gum_prof, gumjs],
  output: devkit_outputs,
  command: [
    mkdevkit,
    'ainakan-gumjs',
    f'@host_os@-@host_arch@',
    meson.current_build_dir(),
  ] + devkit_options,
  install: true,
  install_dir: get_option('libdir') / 'ainakan' / 'devkits' / 'gumjs'
)
