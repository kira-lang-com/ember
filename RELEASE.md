# 26.10.4

The first source release of Ember includes:

- A graphics application lifecycle and APIs for buffers, textures, pipelines, render passes, and draw encoding.
- Metal on Apple platforms and Vulkan on Windows and Linux, with Dawn available for WebGPU and compatibility runs.
- Exportable render targets using Linux Vulkan dma-buf or Metal IOSurface; Dawn reports them as unexportable.

The current compiler requires local aliases when capturing state members in a trailing render-pass block.
