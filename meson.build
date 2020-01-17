project('ogre2', 'cpp', 'c',
  default_options: [
    'warning_level=0'
  ]
)

add_project_arguments('-D_DEBUG=1', language : 'c')
add_project_arguments('-D_DEBUG=1', language : 'cpp')

# GCC
# add_project_arguments('-w', language: 'cpp')
# add_project_arguments('-w', language: 'c')
# add_project_arguments('-msse4.1', language: 'cpp')
# add_project_arguments('-fcompare-debug-second', language: 'cpp')
# add_project_arguments('-fcompare-debug-second', language: 'c')


# cmake = import('cmake')
# Subproject with the "code generator"
# ogredeps_proj = cmake.subproject('ogredeps')
# zziplibDep = ogredeps_proj.target('zziplib')

ogredeps_proj = subproject('ogredeps')
# TODO: Standardize capitalization
zziplibDep   = ogredeps_proj.get_variable('zziplibDep')
zlibDep      = ogredeps_proj.get_variable('zlibDep')
freetypeDep  = ogredeps_proj.get_variable('freetypeDep')
RapidJsonDep = ogredeps_proj.get_variable('RapidJsonDep')

subdir('OgreMain')
subdir('RenderSystems')
subdir('Components')
#subdir('Samples')
