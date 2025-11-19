vapis = [
  'ainakan-gum-@0@.vapi'.format(api_version),
  'ainakan-gum-heap-@0@.vapi'.format(api_version),
]

if host_os_family == 'windows'
  vapis += ['ainakan-gum-windows-@0@.vapi'.format(api_version)]
endif

if host_os_family == 'darwin'
  vapis += ['ainakan-gum-darwin-@0@.vapi'.format(api_version)]
endif

if host_os_family == 'linux'
  vapis += ['ainakan-gum-linux-@0@.vapi'.format(api_version)]
endif

if host_os_family == 'freebsd'
  vapis += ['ainakan-gum-freebsd-@0@.vapi'.format(api_version)]
endif

if have_gumjs
  vapis += [
    'ainakan-gumjs-@0@.vapi'.format(api_version),
    'ainakan-gumjs-inspector-@0@.vapi'.format(api_version),
  ]
endif

install_data(vapis, install_dir: get_option('prefix') / get_option('datadir') / 'vala' / 'vapi')
