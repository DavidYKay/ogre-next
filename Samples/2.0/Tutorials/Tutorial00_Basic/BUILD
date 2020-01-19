package(default_visibility = ["//visibility:public"])

load("@rules_cc//cc:defs.bzl", "cc_binary")

cc_binary(
    name = "Tutorial00_Basic",
    srcs = [
        'Tutorial00_Basic.cpp'
    ],
    copts = [
        #"-Isubprojects/ogre2/Samples/2.0/Common/include",
        "-Isubprojects/ogre2/OgreMain/include",
        "-Isubprojects/ogre2/Components/Hlms/Common/include",
        "-Isubprojects/ogre2/Components/Hlms/Unlit/include",
        "-Isubprojects/ogre2/Components/Hlms/Pbs/include",
        #"-isystem/usr/include/freetype2",
        "-isystem/usr/include/SDL2",
    ],
    linkopts = [
        #"-L/usr/lib64",
        "-lX11",
        "-lXt",
        "-lXaw",
        "-lpthread",
        "-lzzip",
        "-ldl",
        #"-L"
        "-lXrandr",
        #"-lxrandr",
    ],
    deps = [
      '//subprojects/ogre2/OgreMain',
      '//subprojects/ogre2/Components/Hlms/Unlit',
      '//subprojects/ogre2/Components/Hlms/Pbs',
    ],
  )
