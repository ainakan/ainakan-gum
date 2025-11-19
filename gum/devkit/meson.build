devkit_outputs = [
  'ainakan-gum.h',
  static_lib_prefix + 'ainakan-gum' + static_lib_suffix,
  'ainakan-gum-example.c',
]

if cc.get_argument_syntax() == 'msvc'
  devkit_outputs += [
    'ainakan-gum-example.sln',
    'ainakan-gum-example.vcxproj',
    'ainakan-gum-example.vcxproj.filters',
  ]
endif

custom_target('gum-devkit',
  input: gum,
  output: devkit_outputs,
  command: [
    mkdevkit,
    'ainakan-gum',
    f'@host_os@-@host_arch@',
    meson.current_build_dir(),
  ] + devkit_options,
  install: true,
  install_dir: get_option('libdir') / 'ainakan' / 'devkits' / 'gum'
)
