cc = meson.get_compiler('cpp')

lib_src = [
  'src/OgreHlmsBufferManager.cpp',
]

incdir = include_directories(
  'include',
)

HlmsCommon = static_library('HlmsPbsComponent', lib_src,
  link_with: [
    ],
  dependencies: [
    OgreMainDep
  ],
  include_directories : incdir)


HlmsCommonDep = declare_dependency(link_with : HlmsCommon,
  include_directories : incdir)
