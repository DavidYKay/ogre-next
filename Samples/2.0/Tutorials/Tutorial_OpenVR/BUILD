package(default_visibility = ["//visibility:public"])

load("@rules_cc//cc:defs.bzl", "cc_binary")

cc_binary(
    name = "Tutorial_OpenVR",
    srcs = [
      'OpenVRCompositorListener.cpp',
      'Tutorial_OpenVR.cpp',
      'Tutorial_OpenVRGameState.cpp',
    ],
    includes = [
        #"subprojects/libopenvr_api/headers",
        "subprojects/ogre2/Samples/2.0/Tutorials/Tutorial_OpenVR",
    ],
    copts = [
        "-Isubprojects/ogre2/Samples/2.0/Tutorials/Tutorial_OpenVR",
        #"-Isubprojects/libopenvr_api/headers",
        #"-I.",
        #"-Isubprojects/ogre2/Samples/2.0/Tutorials/Tutorial04",
        #"-Isubprojects/ogre2/Samples/2.0/Tutorials/headers",
        #"-Isubprojects/ogre2/Samples/2.0/Common/include",
        #"-Isubprojects/ogre2/OgreMain/include",
        #"-Isubprojects/ogre2/Components/Hlms/Common/include",
        #"-Isubprojects/ogre2/Components/Hlms/Unlit/include",
        #"-Isubprojects/ogre2/Components/Hlms/Pbs/include",
        #"-isystem/usr/include/SDL2",
    ],
    # linkopts = [ ],
    deps = [
      '//subprojects/ogre2/OgreMain',
      '//subprojects/ogre2/Components/Hlms/Pbs',
      '//subprojects/ogre2/Samples/2.0/Common',
      '//subprojects/libopenvr_api',
      #dependency('SDL2'),
    ],
  )
