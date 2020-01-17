cc = meson.get_compiler('cpp')

lib_src = [
  'src/OgreHlmsJsonPbs.cpp',
  'src/InstantRadiosity/OgreInstantRadiosity.cpp',
  'src/Cubemaps/OgreParallaxCorrectedCubemapBase.cpp',
  'src/Cubemaps/OgreParallaxCorrectedCubemap.cpp',
  'src/Cubemaps/OgreCubemapProbe.cpp',
  'src/Cubemaps/OgreParallaxCorrectedCubemapAuto.cpp',
  # 'src/OgreHlmsPbsDatablock.cpp.inc',
  'src/OgreHlmsPbsDatablock.cpp',
  'src/OgreIrradianceVolume.cpp',
  'src/Vct/OgreVctMaterial.cpp',
  'src/Vct/OgreVctVoxelizer.cpp',
  'src/Vct/OgreVoxelVisualizer.cpp',
  'src/Vct/OgreVctLighting.cpp',
  'src/OgreHlmsPbs.cpp',
]

incdir = include_directories(
  'include',
  'include/InstantRadiosity',
  'include/Cubemaps',
  'include/Vct',
)

HlmsPbsComponent  = static_library('HlmsPbsComponent', lib_src,
  link_with: [
    ],
  dependencies: [
    OgreMainDep,
    HlmsCommonDep,
    RapidJsonDep,
  ],
  include_directories : incdir)

HlmsPbsComponentDep = declare_dependency(
  link_with : HlmsPbsComponent,
  dependencies: HlmsCommonDep,
  include_directories : incdir)
