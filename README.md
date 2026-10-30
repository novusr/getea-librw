librw
=====

This library is supposed to be a re-implementation of RenderWare graphics,
or a good part of it anyway.

It is intended to be cross-platform in two senses:
support rendering on different platforms similar to RW;
supporting all file formats for all platforms at all times and provide
way to convert to all other platforms.

Supported file formats are DFF and TXD for PS2, D3D8, D3D9 and Xbox.
Not all pre-instanced PS2 DFFs are supported.
BSP is not supported at all.

For rendering we have D3D9 and OpenGL (>=2.1, ES >= 2.0) backends.
Rendering some things on the PS2 is working as a test only.

# Uses

librw can be used for rendering [GTA](https://github.com/gtamodding/re3) and is used as the core graphics backend for [GETEA-MP](https://github.com/novusr/GETEA-MP).

# GETEA Integration

This repository is a dedicated public fork of [librw](https://github.com/aap/librw) for the **GETEA** project (a 1:1 clean-room reimplementation of the GTA San Andreas base game using modern C++20, SDL3, and OpenGL 3.3 Core Profile).

It serves as the runtime rendering backend and hosts custom rendering pipelines tailored for San Andreas (such as building dual-pass day/night vertex coloring, vehicle reflection environment mapping, and hardware skeletal skinning shaders).

- **Main Project:** [GETEA-MP](https://github.com/novusr/GETEA-MP)
- **Target Backend:** OpenGL 3.3 Core Profile (`GL3`) + `SDL3`

# Building

Get premake5. Generate a config, e.g. with ``premake5 gmake``,
and look in the build directory. Or build with CMake directly as embedded in GETEA.
