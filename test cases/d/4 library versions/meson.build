project('D library versions', 'd')

if meson.get_compiler('d').get_id() == 'gcc'
  error('MESON_SKIP_TEST: GDC can not build shared libraries')
endif

shared_library('some', 'lib.d',
  version : '1.2.3',
  soversion : '0',
  install : true)

shared_library('noversion', 'lib.d',
  install : true)

shared_library('onlyversion', 'lib.d',
  version : '1.4.5',
  install : true)

shared_library('onlysoversion', 'lib.d',
  # Also test that int soversion is acceptable
  soversion : 5,
  install : true)
