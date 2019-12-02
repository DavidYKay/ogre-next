cc = meson.get_compiler('cpp')

lib_src = [
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
]

incdir = include_directories(
  'include',
)

OverlayComponent  = library('OverlayComponent', lib_src,
  link_with: [
    ],
  dependencies: [
    OgreMainDep,
    HlmsUnlitComponentDep,
    dependency('freetype2'),
  ],
  include_directories : incdir)

OverlayComponentDep = declare_dependency(link_with : OverlayComponent,
  include_directories : incdir)
