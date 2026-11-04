# 26.10.4

**Project:** Ember  
**Release week:** 2026-10-26 – 2026-11-01

## Highlights

The first source release of Ember includes:

- A graphics application lifecycle and APIs for buffers, textures, pipelines, render passes, and draw encoding.
- Metal on Apple platforms and Vulkan on Windows and Linux, with Dawn available for WebGPU and compatibility runs.
- Exportable render targets using Linux Vulkan dma-buf or Metal IOSurface; Dawn reports them as unexportable.


## Changed

- Added `RenderPassDescriptor.drawArea`: a pass can draw into part of its color attachment. The viewport and every scissor are placed inside the area on Vulkan, Dawn and Metal, and a clear still covers the whole attachment. A compositor uses it to draw a smaller output at an offset.
- Made low-level graphics backend, native callback state, and foreign memory operations explicit inside `unsafe` regions across Metal, Vulkan, and Dawn code paths.

## Breaking changes

- Source now requires Kira unsafe-block support for affected native graphics integration paths.

## Known limitations

- Render-pass closures currently require local aliases for captured state members, pending compiler improvements.
- Modern KLF-hosted Kira frontend parity for `unsafe` remains pending.
