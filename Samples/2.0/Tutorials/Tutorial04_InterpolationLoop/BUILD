package(default_visibility = ["//visibility:public"])

load("@rules_cc//cc:defs.bzl", "cc_binary")

cc_library(
    name = "lib",
    srcs = [
        'GraphicsGameState.cpp',
        'LogicGameState.cpp',
    ],
    hdrs = [
        'GraphicsGameState.h',
        'LogicGameState.h',
    ],
    copts = [
        "-Isubprojects/ogre2/OgreMain/include",
        "-Isubprojects/ogre2/Samples/2.0/Common/include",
        "-Isubprojects/ogre2/Components/Overlay/include",
        "-isystemsubprojects/ogredeps/src/SDL2/include",
    ],
    deps = [
      '//subprojects/ogre2/OgreMain',
      '//subprojects/ogre2/Samples/2.0/Common',
      '//subprojects/ogre2/Components/Overlay',
    ],
)

cc_binary(
    name = "Tutorial04_InterpolationLoop",
    srcs = [
        'Tutorial04_InterpolationLoop.cpp',
    ],
    copts = [
        #"-I.",
        #"-I/home/dk/workspace/current/mccarthy",
        "-Isubprojects/ogre2/Samples/2.0/Tutorials/Tutorial04_InterpolationLoop",
        "-Isubprojects/ogre2/Samples/2.0/Common/include",
        "-Isubprojects/ogre2/OgreMain/include",
        "-Isubprojects/ogre2/Components/Overlay/include",
        #"-Isubprojects/ogre2/Components/Hlms/Common/include",
        #"-Isubprojects/ogre2/Components/Hlms/Unlit/include",
        #"-Isubprojects/ogre2/Components/Hlms/Pbs/include",
        "-isystemsubprojects/ogredeps/src/SDL2/include",
    ],
    linkopts = [
        "-lSDL2",
        "-lfreetype",
    ],
    deps = [
      ':lib',
      '//subprojects/ogre2/OgreMain',
      '//subprojects/ogre2/Components/Hlms/Unlit',
      '//subprojects/ogre2/Components/Hlms/Pbs',
      '//subprojects/ogre2/Components/Overlay',
      #dependency('SDL2'),
    ],
)

# -Isubprojects/ogre2/Samples/2.0/Tutorials/Tutorial04_InterpolationLoop
# -Isubprojects/ogre2/Samples/2.0/Common/include
# -Isubprojects/ogre2/OgreMain/include
