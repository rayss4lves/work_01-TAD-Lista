project(
  'work_01-TAD-Lista',
  'c',
  version: '0.1',
  default_options: ['warning_level=3'],
)

# Depedencia do gtk 
dep_gtk = dependency('gtk+-3.0', version: '>=3.0')

subdir('src/image')
subdir('src/ui')

includes = [includes_img_trat, includes_ui]
libs = lib_img
libs += lib_ui

configure_file(
  input: 'utils/input_image_example_Gray.txt',
  output: 'imgGray.txt',
  copy: true,
)

configure_file(
  input: 'utils/input_image_example_RGB.txt',
  output: 'imgRGB.txt',
  copy: true,
)


executable(
  'work_01-TAD-Lista',
  'src/main.c',
  include_directories: includes,
  link_with: libs,
  dependencies: dep_gtk,
  install: true,
)