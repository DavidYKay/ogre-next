cc = meson.get_compiler('cpp')

common_src = [
  'src/GLSL/OgreGLSLExtSupport.cpp',
  'src/GLSL/OgreGLSLMonolithicProgram.cpp',
  'src/GLSL/OgreGLSLMonolithicProgramManager.cpp',
  'src/GLSL/OgreGLSLPreprocessor.cpp',
  'src/GLSL/OgreGLSLProgram.cpp',
  'src/GLSL/OgreGLSLProgramManager.cpp',
  'src/GLSL/OgreGLSLSeparableProgram.cpp',
  'src/GLSL/OgreGLSLSeparableProgramManager.cpp',
  'src/GLSL/OgreGLSLShader.cpp',
  'src/GLSL/OgreGLSLShaderFactory.cpp',
  'src/GLSL/OgreGLSLShaderManager.cpp',
  'src/OgreGL3PlusAsyncTextureTicket.cpp',
  'src/OgreGL3PlusContext.cpp',
  'src/OgreGL3PlusDefaultHardwareBufferManager.cpp',
  'src/OgreGL3PlusEngineDll.cpp',
  'src/OgreGL3PlusHardwareBufferManager.cpp',
  'src/OgreGL3PlusHardwareCounterBuffer.cpp',
  'src/OgreGL3PlusHardwareIndexBuffer.cpp',
  'src/OgreGL3PlusHardwareOcclusionQuery.cpp',
  'src/OgreGL3PlusHardwareShaderStorageBuffer.cpp',
  'src/OgreGL3PlusHardwareUniformBuffer.cpp',
  'src/OgreGL3PlusHardwareVertexBuffer.cpp',
  'src/OgreGL3PlusMappings.cpp',
  'src/OgreGL3PlusPixelFormatToShaderType.cpp',
  'src/OgreGL3PlusPlugin.cpp',
  'src/OgreGL3PlusRenderPassDescriptor.cpp',
  'src/OgreGL3PlusRenderSystem.cpp',
  'src/OgreGL3PlusStagingTexture.cpp',
  'src/OgreGL3PlusSupport.cpp',
  'src/OgreGL3PlusTextureGpu.cpp',
  'src/OgreGL3PlusTextureGpuManager.cpp',
  'src/OgreGL3PlusTextureGpuWindow.cpp',
  'src/OgreGL3PlusVertexArrayObject.cpp',
  'src/Vao/OgreGL3PlusAsyncTicket.cpp',
  'src/Vao/OgreGL3PlusBufferInterface.cpp',
  'src/Vao/OgreGL3PlusConstBufferPacked.cpp',
  'src/Vao/OgreGL3PlusDynamicBuffer.cpp',
  'src/Vao/OgreGL3PlusMultiSourceVertexBufferPool.cpp',
  'src/Vao/OgreGL3PlusStagingBuffer.cpp',
  'src/Vao/OgreGL3PlusTexBufferEmulatedPacked.cpp',
  'src/Vao/OgreGL3PlusTexBufferPacked.cpp',
  'src/Vao/OgreGL3PlusUavBufferPacked.cpp',
  'src/Vao/OgreGL3PlusVaoManager.cpp',
  'src/gl3w.cpp',
]
#'src/windowing/OSX/OgreGL3PlusUtil.h',
#'src/windowing/OSX/OgreOSXCocoaContext.mm',
#'src/windowing/OSX/OgreOSXCocoaView.mm',
#'src/windowing/OSX/OgreOSXCocoaWindow.mm',
#'src/windowing/OSX/OgreOSXCocoaWindowDelegate.mm',
#'src/windowing/OSX/OgreOSXGL3PlusSupport.mm',
#'src/windowing/SDL/OgreGL3PlusUtil.h',
#'src/windowing/SDL/OgreSDLGLSupport.cpp',
#'src/windowing/SDL/OgreSDLWindow.cpp',
#'src/windowing/gtk/OgreGL3PlusUtil.h',
#'src/windowing/gtk/OgreGTKGLSupport.cpp',
#'src/windowing/gtk/OgreGTKWindow.cpp',

common_inc = [
  'include',
  'include/windowing',
  'include/Vao',
  'include/GLSL',
  'include/GL',

]

common_deps = [
    OgreMainDep
]


if host_machine.system() == 'windows'
  lib_src = common_src + [
    'src/windowing/win32/OgreGL3PlusUtil.h',
    'src/windowing/win32/OgreWin32Context.cpp',
    'src/windowing/win32/OgreWin32GLSupport.cpp',
    'src/windowing/win32/OgreWin32Window.cpp',
  ]
  inc = include_directories(common_inc + [
    'include/windowing/win32',
    'src/windowing/win32',
  ])
  #deps = common_deps + cc.find_library('opengl32')
  deps = [
      OgreMainDep,
      cc.find_library('opengl32'),
  ]
else
  lib_src = [
    'src/windowing/GLX/OgreGL3PlusUtil.h',
    'src/windowing/GLX/OgreGLXContext.cpp',
    'src/windowing/GLX/OgreGLXGLSupport.cpp',
    'src/windowing/GLX/OgreGLXWindow.cpp',
  ]
  inc = include_directories(common_inc + [
    'include/windowing/GLX',
    'src/windowing/GLX',
  ])
  deps = common_deps + [
    dependency('xrandr'),
    cc.find_library('X11'),
    cc.find_library('dl'),
    cc.find_library('GL'),
  ]
endif

#'include/windowing/SDL',
#'include/windowing/OSX',
#'include/windowing/gtk',

# gtkdep = dependency('gtk+-3.0')

RenderSystemGL3Plus  = shared_library('RenderSystemGL3Plus', lib_src,
  link_with: [
  ],
  dependencies: deps,
  include_directories : inc)

