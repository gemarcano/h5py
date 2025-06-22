project('lzf_filter', 'c',
    default_options: [
    'b_lto=true',
    'c_std=c23',
    'warning_level=3',
  ],
  license: ['BSD-3'],
  version: '0.0.1')

src = files([
  'lzf/lzf_c.c',
  'lzf/lzf_d.c',
  'lzf_filter.c',
])

inc = include_directories('lzf')

hdf5 = dependency('hdf5')

lib = library(meson.project_name(), src, dependencies: hdf5,  include_directories: inc, install: true, install_dir: get_option('libdir') / 'hdf5/lib/plugin/')
