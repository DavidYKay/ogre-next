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

common_deps = [
  OgreMainDep,
  HlmsUnlitComponentDep,
  freetypeDep,
]

if host_machine.system() == 'windows'
  deps = common_deps
else
  #deps = common_deps + dependency('freetype2')
  deps = common_deps
endif

OverlayComponent  = static_library('OverlayComponent', lib_src,
  link_with: [
  ],
  dependencies: deps,
  include_directories : incdir)

OverlayComponentDep = declare_dependency(link_with : OverlayComponent,
  include_directories : incdir)
