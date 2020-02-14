package(default_visibility = ['//visibility:public'])

cc_library(
    name = 'lib',
    srcs = [
        'GraphicsGameState.cpp',
        'LogicGameState.cpp',
    ],
    hdrs = [
        'GraphicsGameState.h',
        'LogicGameState.h',
    ],
    includes = [
        '.',
    ],
    deps = [
      '//subprojects/ogre2/Samples/2.0/Common',
    ],
)

cc_binary(
    name = 'Tutorial04_InterpolationLoop',
    srcs = [
        'Tutorial04_InterpolationLoop.cpp',
    ],
    copts = select({
        "//platforms:linux": [
            '-isystem/usr/include/freetype2',
        ],
        "//conditions:default": [],
    }),
    linkopts = select({
        "//platforms:linux": [
            '-lSDL2',
            '-lfreetype',
        ],
        "//conditions:default": [],
    }),
    deps = [
      ':lib',
      #'@freetype2',
      '//subprojects/ogredeps/src/SDL2',
      '//subprojects/ogre2/OgreMain',
      '//subprojects/ogre2/Samples/2.0/Common',
      '//subprojects/ogre2/Components/Hlms/Unlit',
      '//subprojects/ogre2/Components/Hlms/Pbs',
      '//subprojects/ogre2/Components/Overlay',
    ],
)
