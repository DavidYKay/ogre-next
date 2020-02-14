package(default_visibility = ["//visibility:public"])

cc_library(
    name = "Overlay",
    srcs = [
        'src/OgreTextAreaOverlayElement.cpp',
        'src/OgreBorderPanelOverlayElement.cpp',
        'src/OgreOverlayElement.cpp',
        'src/OgreOverlayContainer.cpp',
        'src/OgreOverlayElementCommands.cpp',
        'src/OgreOverlayManager.cpp',
        'src/OgreFontManager.cpp',
        'src/OgreOverlayProfileSessionListener.cpp',
        'src/OgreOverlayElementFactory.cpp',
        'src/OgreFont.cpp',
        'src/OgreOverlaySystem.cpp',
        'src/OgreOverlay.cpp',
        'src/OgrePanelOverlayElement.cpp',
    ],
    hdrs = [
        'include/OgreOverlayProfileSessionListener.h',
        'include/OgreFont.h',
        'include/OgreOverlay.h',
        'include/OgreOverlayElement.h',
        'include/OgreBorderPanelOverlayElement.h',
        'include/OgreFontManager.h',
        'include/OgreOverlaySystem.h',
        'include/OgreOverlayElementCommands.h',
        'include/OgreOverlayManager.h',
        'include/OgrePanelOverlayElement.h',
        'include/OgreTextAreaOverlayElement.h',
        'include/OgreOverlayContainer.h',
        'include/OgreOverlayElementFactory.h',
        'include/OgreOverlayPrerequisites.h',
    ],
    includes = [
        'include',
    ],
    copts = select({
        "//platforms:linux": [
            '-isystem/usr/include/freetype2',
        ],
        "//conditions:default": [],
    }),
    deps = [
        #'@freetype2',
        '//subprojects/ogre2/OgreMain',
        '//subprojects/ogre2/Components/Hlms/Unlit',
    ],
  )
