project('ogre2', 'cpp', 'c',
  default_options: [
    'warning_level=0'
  ]
)

add_project_arguments('-D_DEBUG=1', language : 'c')
add_project_arguments('-D_DEBUG=1', language : 'cpp')
add_project_arguments('-w', language: 'cpp')
add_project_arguments('-w', language: 'c')

compiler = meson.get_compiler('cpp')
if compiler.get_id() == 'gcc'

add_project_arguments('-msse4.1', language: 'cpp')
add_project_arguments('-fcompare-debug-second', language: 'cpp')
add_project_arguments('-fcompare-debug-second', language: 'c')

else
# Non-GCC options
endif

ogredeps_proj = subproject('ogredeps')
# TODO: Standardize capitalization
zziplibDep   = ogredeps_proj.get_variable('zziplibDep')
zlibDep      = ogredeps_proj.get_variable('zlibDep')
freetypeDep  = ogredeps_proj.get_variable('freetypeDep')
RapidJsonDep = ogredeps_proj.get_variable('RapidJsonDep')

subdir('OgreMain')
subdir('RenderSystems')
subdir('Components')
subdir('Samples')
