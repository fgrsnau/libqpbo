project('libqpbo', 'cpp', version: '1.4.0')

sources = ['qpbo.cpp',
           'qpbo_extra.cpp',
           'qpbo_maxflow.cpp',
           'qpbo_postprocessing.cpp']

headers = ['qpbo.h', 'block.h']

both_libraries('qpbo', sources, install: true, version: meson.project_version())
install_headers(headers, subdir: 'qpbo')

configuration = configuration_data()
configuration.set('prefix', get_option('prefix'))
configuration.set('libdir', get_option('libdir'))
configuration.set('includedir', get_option('includedir'))
configuration.set('version', meson.project_version())

configure_file(input: 'libqpbo.pc.in',
               output: 'libqpbo.pc',
               configuration: configuration,
               install: true,
               install_dir: get_option('libdir') / 'pkgconfig')


# vim: set ts=8 sts=2 sw=2 et:
