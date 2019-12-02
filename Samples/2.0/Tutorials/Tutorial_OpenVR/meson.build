cc = meson.get_compiler('cpp')

src = [
  'OpenVRCompositorListener.cpp',
  'Tutorial_OpenVR.cpp',
  'Tutorial_OpenVRGameState.cpp',
]

incdir = include_directories(
  '.',
)

binopenvr_api_dep = declare_dependency(
  dependencies : [
    cc.find_library('libopenvr_api', dirs: ['/home/dk/workspace/current/mccarthy/subprojects/libopenvr_api/bin/linux64'])],
  include_directories: include_directories(
    #'/home/dk/workspace/current/mccarthy/subprojects/libopenvr_api/headers',
    '../../../../../libopenvr_api/headers',
    )
)

Tutorial_OpenVR  = executable('Tutorial_OpenVR', src,
  link_with: [
    ],
  dependencies: [
    OgreMainDep,
    SamplesCommonDep,
    dependency('SDL2'),
    HlmsPbsComponentDep,
    binopenvr_api_dep,
    #HlmsUnlitComponentDep,
  ],
  include_directories : incdir)

