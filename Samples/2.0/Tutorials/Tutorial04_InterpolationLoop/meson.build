cc = meson.get_compiler('cpp')

src = [
        'Tutorial04_InterpolationLoop.cpp',
        'GraphicsGameState.cpp',
        'LogicGameState.cpp',
]

incdir = include_directories(
  '.',
)

Tutorial04InterpolationLoop  = executable('Tutorial04InterpolationLoop', src,
  link_with: [
    ],
  dependencies: [
    OgreMainDep,
    SamplesCommonDep,
    HlmsPbsComponentDep,
    HlmsUnlitComponentDep,
    # dependency('SDL2'),
    SDL2BinDep,
  ],
  include_directories : incdir)

