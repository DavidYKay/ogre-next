cc = meson.get_compiler('cpp')

lib_src = [
  '../../Common/src/GameEntityManager.cpp',
  '../../Common/src/TutorialGameState.cpp',
  '../../Common/src/Utils/MeshUtils.cpp',
  '../../Common/src/Utils/ScreenSpaceReflections.cpp',
  '../../Common/src/Utils/SmaaUtils.cpp',
  '../../Common/src/Utils/TestUtils.cpp',
  '../../Common/src/Utils/HdrUtils.cpp',
  '../../Common/src/Utils/MiscUtils.cpp',
  '../../Common/src/SdlInputHandler.cpp',

  #'../../Common/src/System/Desktop/MainLoopSingleThreaded.cpp',

  '../../Common/src/System/MainEntryPoints.cpp',
  '../../Common/src/System/StaticPluginLoader.cpp',
  '../../Common/src/CameraController.cpp',
  '../../Common/src/Threading/MessageQueueSystem.cpp',
  '../../Common/src/BaseSystem.cpp',
  '../../Common/src/LogicSystem.cpp',
  '../../Common/src/GraphicsSystem.cpp',
]

src = [
        'Tutorial04_InterpolationLoop.cpp',
        'GraphicsGameState.cpp',
        'LogicGameState.cpp',
]

incdir = include_directories(
  '.',
  '../../Common/include',
)

Tutorial04InterpolationLoop  = executable('Tutorial04InterpolationLoop', src + lib_src,
  link_with: [
    ],
  dependencies: [
    OgreMainDep,
    OverlayComponentDep,
    #SamplesCommonDep,
    HlmsPbsComponentDep,
    HlmsUnlitComponentDep,
    #dependency('SDL2'),
    sdlDepVCX64,
  ],
  include_directories : incdir)

