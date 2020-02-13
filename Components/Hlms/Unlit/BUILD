package(default_visibility = ['//visibility:public'])

cc_library(
    name = 'Unlit',
    srcs = [
        'src/OgreHlmsUnlit.cpp',
        'src/OgreUnlitProperty.cpp',
        'src/OgreHlmsUnlitDatablock.cpp',
        'src/OgreTextureAnimationController.cpp',
        'src/OgreHlmsJsonUnlit.cpp',
        ],
    hdrs = [
        'src/OgreHlmsUnlitDatablock.cpp.inc',
        'include/OgreHlmsJsonUnlit.h',
        'include/OgreHlmsUnlitDatablock.h',
        'include/OgreHlmsUnlit.h',
        'include/OgreHlmsUnlitPrerequisites.h',
        'include/OgreTextureAnimationController.h',
        'include/OgreUnlitProperty.h',
        ],
    includes = [
        'include',
        ],
    deps = [
        '//subprojects/ogre2/Components/Hlms/Common',
        '//subprojects/ogre2/OgreMain',
        '//subprojects/ogredeps/src/rapidjson',
        ],
    )
