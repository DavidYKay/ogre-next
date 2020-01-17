package(default_visibility = ["//visibility:public"])

cc_library(
    name = "Common",
    srcs = [
      'src/OgreHlmsBufferManager.cpp',
    ],
    hdrs = [
      'include/OgreHlmsBufferManager.h',
      'include/OgreHlmsTextureBaseClass.h',
      'include/OgreHlmsTextureBaseClass.inl',
    ],
    copts = [
        "-Isubprojects/ogre2/Components/Hlms/Common/include",
        "-Isubprojects/ogre2/OgreMain/include",
    ],
  deps = [
    '//subprojects/ogre2/OgreMain'
  ],
)
