package(default_visibility = ["//visibility:public"])

cc_library(
    name = "Unlit",
    srcs = [
      'src/OgreHlmsUnlit.cpp',
      'src/OgreUnlitProperty.cpp',
      'src/OgreHlmsUnlitDatablock.cpp',
      'src/OgreTextureAnimationController.cpp',
      'src/OgreHlmsJsonUnlit.cpp',
    ],
    hdrs = [
      #'../Common/include/OgreHlmsTextureBaseClass.h',
      'src/OgreHlmsUnlitDatablock.cpp.inc',
      'include/OgreHlmsJsonUnlit.h',
      'include/OgreHlmsUnlitDatablock.h',
      'include/OgreHlmsUnlit.h',
      'include/OgreHlmsUnlitPrerequisites.h',
      'include/OgreTextureAnimationController.h',
      'include/OgreUnlitProperty.h',
    ],
    copts = [
        "-Isubprojects/ogre2/Components/Hlms/Unlit/include",
        "-Isubprojects/ogre2/Components/Hlms/Common/include",
        "-Isubprojects/ogre2/Components/Hlms/Common",
        "-Isubprojects/ogre2/OgreMain/include",
        "-Isubprojects/ogredeps/src/rapidjson",
    ],
  deps = [
    '//subprojects/ogre2/Components/Hlms/Common',
    '//subprojects/ogre2/OgreMain',
    "//subprojects/ogredeps/src/rapidjson",
    # OgreMainDep,
    # HlmsCommonDep,
  ],
  )
