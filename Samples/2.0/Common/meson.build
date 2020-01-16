cc = meson.get_compiler('cpp')

lib_src = [
  'src/GameEntityManager.cpp',
  'src/TutorialGameState.cpp',
  'src/Utils/MeshUtils.cpp',
  'src/Utils/ScreenSpaceReflections.cpp',
  'src/Utils/SmaaUtils.cpp',
  'src/Utils/TestUtils.cpp',
  'src/Utils/HdrUtils.cpp',
  'src/Utils/MiscUtils.cpp',
  'src/SdlInputHandler.cpp',

  #'src/System/Desktop/MainLoopMultiThreaded.cpp',
  'src/System/Desktop/MainLoopSingleThreaded.cpp',

  # 'src/System/iOS/GameViewController.mm',
  # 'src/System/iOS/Resources/Main.storyboard',
  # 'src/System/iOS/Resources/Info.plist',
  # 'src/System/iOS/iOSUtils.mm',
  # 'src/System/iOS/AppDelegate.mm',
  # 'src/System/OSX/OSXUtils.mm',
  # 'src/System/OSX/Resources/Info.plist',
  'src/System/MainEntryPoints.cpp',
  'src/System/StaticPluginLoader.cpp',
  'src/CameraController.cpp',
  'src/Threading/MessageQueueSystem.cpp',
  'src/BaseSystem.cpp',
  'src/LogicSystem.cpp',
  'src/GraphicsSystem.cpp',
]

incdir = include_directories(
  'include',
  'include/Utils',
  'include/System',
  # 'include/System/iOS',
  # 'include/System/OSX',
  'include/Threading',
)

sdlDepX86 = declare_dependency(
  dependencies : [
    cc.find_library('SDL2', dirs: [
      #'C:/Users/David/Downloads/SDL2-2.0.10-win32-x64/SDL2.dll',
      'C:/Users/David/Downloads/SDL2/i686-w64-mingw32/lib/'
#C:\Users\David\Downloads\SDL2-2.0.10-win32-x64\SDL2.dll
    ])],
  include_directories: include_directories(
      'C:/Users/David/Downloads/SDL2/i686-w64-mingw32/include'
  )
)

sdlDepX64 = declare_dependency(
  dependencies : [
    cc.find_library('SDL2', dirs: [
      'C:/Users/David/Downloads/SDL2/x86_64-w64-mingw32/lib'
    ])],
  include_directories: include_directories(
      'C:/Users/David/Downloads/SDL2/x86_64-w64-mingw32/include'
  )
)

# sdlDepVCX86 = declare_dependency(
#   dependencies : [
#     cc.find_library('SDL2', dirs: [
#       'C:\Users\David\Downloads\SDL2-devel-2.0.10-VC\SDL2-2.0.10\lib\x86'
#     ])],
#   include_directories: include_directories(
#       'C:/Users/David/Downloads/SDL2-devel-2.0.10-VC/SDL2-2.0.10/include/SDL2'
#   )
# )

sdlDepVCX64 = declare_dependency(
  dependencies : [
    cc.find_library('SDL2', dirs: [
      'C:/Users/David/Downloads/SDL2-devel-2.0.10-VC/SDL2-2.0.10/lib/x64'
    ])],
  include_directories: include_directories(
      'C:/Users/David/Downloads/SDL2-devel-2.0.10-VC/SDL2-2.0.10/include/SDL2'
  )
)

#SamplesCommon  = static_library('SamplesCommon', lib_src,
#  link_with: [
#    HlmsPbsComponent,
#    ],
#  dependencies: [
#    OgreMainDep,
#    OverlayComponentDep,
#    HlmsCommonDep,
#    HlmsPbsComponentDep,
#    HlmsUnlitComponentDep,
#    #dependency('SDL2'),
#    #sdlDepVCX64
#    #sdlDepVCX86
#    #cc.find_library('freetype2'),
#    #cc.find_library('SDL2'),
#  ],
#  include_directories : incdir)
#
#SamplesCommonDep = declare_dependency(
#  link_with : SamplesCommon,
#  dependencies: OverlayComponentDep,
#  include_directories : incdir)
