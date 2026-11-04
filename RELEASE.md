# 26.11.1

**Project:** Ember  
**Release week:** 2026-11-02 – 2026-11-08

## Highlights

Updated Ember's native graphics integrations and added support for drawing a render pass into a defined area of its color attachment.

## Added

- `RenderPassDescriptor.drawArea`, which offsets and clips a pass's viewport and scissors inside a color attachment; the attachment clear still covers its full area.
- `NativeLibs/Vulkan/vulkan.klffi` bindings for the Vulkan backend.

## Changed

- Updated Vulkan, Dawn, and Metal backend paths and their interop definitions to use the current native interfaces.

## Known limitations

- No new cross-platform graphics build or rendering test results are recorded for this release preparation; these changes are not claimed as validated across all backends.
