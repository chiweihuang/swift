add_swift_library(swiftGLKit ${SWIFT_SDK_OVERLAY_LIBRARY_BUILD_TYPES} IS_SDK_OVERLAY
  GLKMath.swift.gyb

  SWIFT_COMPILE_FLAGS "${SWIFT_RUNTIME_SWIFT_COMPILE_FLAGS}"
  LINK_FLAGS "${SWIFT_RUNTIME_SWIFT_LINK_FLAGS}"
  TARGET_SDKS OSX IOS IOS_SIMULATOR TVOS TVOS_SIMULATOR
  SWIFT_MODULE_DEPENDS_OSX Darwin AppKit CoreData CoreGraphics CoreImage Dispatch Foundation IOKit ObjectiveC QuartzCore simd XPC # auto-updated
  SWIFT_MODULE_DEPENDS_IOS Darwin CoreGraphics CoreImage Dispatch Foundation ObjectiveC QuartzCore simd UIKit # auto-updated
  SWIFT_MODULE_DEPENDS_TVOS Darwin CoreGraphics CoreImage Dispatch Foundation ObjectiveC QuartzCore simd UIKit # auto-updated
  FRAMEWORK_DEPENDS GLKit
)
