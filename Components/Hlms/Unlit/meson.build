cc = meson.get_compiler('cpp')

lib_src = [
  # 'src/OgreHlmsUnlitDatablock.cpp.inc',
  'src/OgreHlmsUnlit.cpp',
  'src/OgreUnlitProperty.cpp',
  'src/OgreHlmsUnlitDatablock.cpp',
  'src/OgreTextureAnimationController.cpp',
  'src/OgreHlmsJsonUnlit.cpp',
]

incdir = include_directories(
  'include',
)

HlmsUnlitComponent  = static_library('HlmsUnlitComponent', lib_src,
  link_with: [
    ],
  dependencies: [
    OgreMainDep,
    HlmsCommonDep,
  ],
  include_directories : incdir)

HlmsUnlitComponentDep = declare_dependency(
  link_with : HlmsUnlitComponent,
  dependencies: HlmsCommonDep,
  include_directories : incdir)
