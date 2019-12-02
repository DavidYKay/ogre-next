cc = meson.get_compiler('cpp')

src = [
  'Tutorial00_Basic.cpp'
]

incdir = include_directories(
  '.',
)

Tutorial00Basic  = executable('Tutorial00Basic', src,
  link_with: [
    ],
  dependencies: [
    OgreMainDep,
    HlmsPbsComponentDep,
    HlmsUnlitComponentDep,
  ],
  include_directories : incdir)

