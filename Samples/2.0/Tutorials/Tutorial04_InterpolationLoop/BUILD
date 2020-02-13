package(default_visibility = ['//visibility:public'])

load('@rules_cc//cc:defs.bzl', 'cc_binary')

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
    copts = [
        #'-Isubprojects/ogre2/OgreMain/include',
        #'-Isubprojects/ogre2/Samples/2.0/Common/include',
        #'-Isubprojects/ogre2/Components/Overlay/include',
        #'-isystemsubprojects/ogredeps/src/SDL2/include',
    ],
    deps = [
      '//subprojects/ogre2/OgreMain',
      '//subprojects/ogre2/Samples/2.0/Common',
      #'//subprojects/ogre2/Samples/2.0/Common',
      #'//subprojects/ogre2/Components/Overlay',
    ],
)

cc_binary(
    name = 'Tutorial04_InterpolationLoop',
    srcs = [
        'Tutorial04_InterpolationLoop.cpp',
        'GraphicsGameState.cpp',
        'LogicGameState.cpp',
    ],
    #includes = [ '.', ],
    copts = [
        # '-isystemsubprojects/ogredeps/src/SDL2/include',
        # '-isystem/usr/include/SDL2',
        # '-I/usr/include/SDL2',
        #"-isystemsubprojects/ogredeps/src/freetype/include",
        #"-isystem/usr/include/freetype2",
    ],
    linkopts = [
        '-lSDL2',
        '-lfreetype',
    ],
    deps = [
      ':lib',
      '//subprojects/ogredeps/src/SDL2',
      '//subprojects/ogre2/OgreMain',
      '//subprojects/ogre2/Samples/2.0/Common',
      '//subprojects/ogre2/Components/Hlms/Unlit',
      '//subprojects/ogre2/Components/Hlms/Pbs',
      '//subprojects/ogre2/Components/Overlay',
    ],
)
