package(default_visibility = ["//visibility:public"])

load("@rules_cc//cc:defs.bzl", "cc_binary")

cc_binary(
    name = "Tutorial04_InterpolationLoop",
    srcs = [
        'Tutorial04_InterpolationLoop.cpp',
        'GraphicsGameState.cpp',
        'LogicGameState.cpp',
    ],
    copts = [
        #"-I.",
        "-Isubprojects/ogre2/Samples/2.0/Tutorials/Tutorial04_InterpolationLoop",

        "-Isubprojects/ogre2/Samples/2.0/Common/include",
        "-Isubprojects/ogre2/OgreMain/include",
        #"-Isubprojects/ogre2/Components/Hlms/Common/include",
        #"-Isubprojects/ogre2/Components/Hlms/Unlit/include",
        #"-Isubprojects/ogre2/Components/Hlms/Pbs/include",
        #"-isystem/usr/include/SDL2",
    ],
    # linkopts = [ ],
    deps = [
      '//subprojects/ogre2/OgreMain',
      '//subprojects/ogre2/Components/Hlms/Unlit',
      '//subprojects/ogre2/Components/Hlms/Pbs',
      '//subprojects/ogre2/Samples/2.0/Common',
      #dependency('SDL2'),
    ],
  )

# -Isubprojects/ogre2/Samples/2.0/Tutorials/Tutorial04_InterpolationLoop 
# -Isubprojects/ogre2/Samples/2.0/Common/include 
# -Isubprojects/ogre2/OgreMain/include 

