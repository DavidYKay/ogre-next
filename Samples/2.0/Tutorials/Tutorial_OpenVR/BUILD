package(default_visibility = ["//visibility:public"])

load("@rules_cc//cc:defs.bzl", "cc_binary")

cc_library(
    name = "lib",
    srcs = [
      'Tutorial_OpenVRGameState.cpp',
      'OpenVRCompositorListener.cpp',
    ],
    hdrs = [
      'OpenVRCompositorListener.h',
      'Tutorial_OpenVRGameState.h',
      'Tutorial_OpenVR.h',
    ],
    copts = [
        "-Isubprojects/libopenvr_api/headers",
        "-Isubprojects/ogre2/OgreMain/include",
        "-Isubprojects/ogre2/Samples/2.0/Common/include",
        "-Isubprojects/ogre2/Components/Overlay/include",
        "-isystem/usr/include/SDL2",
        "-Isubprojects/ogre2/Components/Hlms/Pbs/include",
        "-Isubprojects/ogre2/Components/Hlms/Common/include",
    ],

    deps = [
      '//subprojects/ogre2/Components/Hlms/Pbs',
      '//subprojects/ogre2/OgreMain',
      '//subprojects/ogre2/Samples/2.0/Common',
      '//subprojects/ogre2/Components/Overlay',
      '//subprojects/libopenvr_api',
    ],
)

cc_binary(
    name = "Tutorial_OpenVR",
    srcs = [
      'Tutorial_OpenVR.cpp',
    ],
    includes = [
        #"subprojects/libopenvr_api/headers",
        #"subprojects/ogre2/Samples/2.0/Tutorials/Tutorial_OpenVR",
    ],
    copts = [
        "-Isubprojects/ogre2/Samples/2.0/Tutorials/Tutorial_OpenVR",
        "-Isubprojects/libopenvr_api/headers",
        #"-Isubprojects/ogre2/Samples/2.0/Tutorials/Tutorial04",
        #"-Isubprojects/ogre2/Samples/2.0/Tutorials/headers",
        "-Isubprojects/ogre2/Samples/2.0/Common/include",
        "-Isubprojects/ogre2/OgreMain/include",
        "-Isubprojects/ogre2/Components/Overlay/include",
        #"-Isubprojects/ogre2/Components/Hlms/Common/include",
        #"-Isubprojects/ogre2/Components/Hlms/Unlit/include",
        "-isystem/usr/include/SDL2",
    ],
    linkopts = [ 
        "-lSDL2",
        "-lfreetype",
    ],
    deps = [
      ':lib',
      '//subprojects/ogre2/OgreMain',
      '//subprojects/ogre2/Samples/2.0/Common',
      '//subprojects/ogre2/Components/Overlay',
      #'//subprojects/libopenvr_api',
      #dependency('SDL2'),
    ],
  )
