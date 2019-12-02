project('ogre2', 'cpp', 'c',
  default_options: [
    'warning_level=0'
  ]
)

add_project_arguments('-D_DEBUG=1', language : 'c')
add_project_arguments('-D_DEBUG=1', language : 'cpp')
add_project_arguments('-w', language: 'cpp')
add_project_arguments('-w', language: 'c')
add_project_arguments('-fcompare-debug-second', language: 'cpp')
add_project_arguments('-fcompare-debug-second', language: 'c')

subdir('OgreMain')
subdir('RenderSystems')
subdir('Components')
subdir('Samples')
