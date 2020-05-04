package(default_visibility = ["//visibility:public"])

cc_library(
    name = "SceneFormat",
    srcs = [
        'src/OgreSceneFormatBase.cpp',
        'src/OgreSceneFormatExporter.cpp',
        'src/OgreSceneFormatImporter.cpp',
    ],
    hdrs = [
        'include/OgreSceneFormatBase.h',
        'include/OgreSceneFormatExporter.h',
        'include/OgreSceneFormatImporter.h',
        'include/OgreSceneFormatPrerequisites.h',
    ],
    includes = [
        'include',
    ],
    deps = [
        '//subprojects/ogre2/OgreMain',
        '//subprojects/ogre2/Components/Hlms/Pbs',
    ],
)
