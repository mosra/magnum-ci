This repository contains CI jobs for building Magnum and its dependencies.

[![Join the chat at https://gitter.im/mosra/magnum](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mosra/magnum?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

ANGLE
=====

https://github.com/google/angle — OpenGL ES implemented using D3D on Windows
and Metal on Mac.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/angle/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3ASwiftShader)
-   **Latest known-good build**: [v4134](https://github.com/mosra/magnum-ci/actions/runs/252324081) (2020-09-13)
    -   Windows
    -   Windows UWP
    -   macOS

Assimp
======

https://www.assimp.org — Asset import library.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/assimp/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3AAssimp)
-   **Latest known-good build**: [5.1.2](https://github.com/mosra/magnum-ci/actions/runs/1513158340) (2021-11-28)
    -   Windows MSVC2019
    -   Windows MSVC2019 Debug
    -   Windows MSVC2017
    -   Windows MSVC2017 Debug
    -   Windows MinGW

FreeType
========

https://www.freetype.org — Font rendering library.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/freetype/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3AFreeType)
-   **Latest known-good build**: [2.10.4](https://github.com/mosra/magnum-ci/actions/runs/454639188) (2020-12-31)
    -   Windows MSVC2019
    -   Windows MSVC2017

Glslang
=======

https://github.com/KhronosGroup/glslang — GLSL validator and GLSL-to-SPIR-V
compiler.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/glslang/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3AGlslang)
-   **Latest known-good build**: [8.13.3743](https://github.com/mosra/magnum-ci/actions/runs/454616450) (2020-12-31)
    -   Windows MSVC2019
    -   Windows MSVC2019 Debug
    -   Windows MSVC2017
    -   Windows MSVC2017 Debug
    -   Ubuntu 16.04
    -   Ubuntu 16.04 GCC 4.8

libjpeg-turbo
=============

https://github.com/libjpeg-turbo/libjpeg-turbo — libjpeg with SIMD acceleration

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/libjpeg-turbo/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3Alibjpeg-turbo)
-   **Latest known-good build**: [2.0.6](https://github.com/mosra/magnum-ci/actions/runs/473943089) (2021-01-09)
    -   Windows MSVC2019
    -   Windows MSVC2017
    -   No MinGW build due to ABI issues
        (`undefined reference to '__imp___acrt_iob_func'`) when used on
        AppVeyor with GCC 7.2

Magnum Tools
============

`magnum-imageconverter`, `magnum-sceneconverter`, `magnum-gl-info`,
`magnum-vk-info`, `magnum-player`, importer and image/scene converter plugins
and Python 3.8, 3.9, and 3.10 bindings.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/magnum-tools/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3A"Magnum+Tools")
-   **Latest known-good build**: [`master`](https://github.com/mosra/magnum-ci/actions/runs/2071552983) (2022-03-31)
    -   Ubuntu 18.04

OpenEXR
=======

https://github.com/AcademySoftwareFoundation/openexr — reference implementation
of the OpenEXR format

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/openexr/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3Aopenexr)
-   **Depends on**: [zlib](#zlib)
-   **Latest known-good build**: [2.5.5](https://github.com/mosra/magnum-ci/actions/runs/726022297) (2021-04-07)
    -   Windows MSVC2019
    -   Windows MSVC2019 Debug
    -   Windows MSVC2017
    -   Windows MSVC2017 Debug
    -   Windows MinGW
    -   Ubuntu 16.04 (there's `libopenexr-dev` 2.2 in the repos, but it leaks
        like crazy, so this build is needed)
    -   Ubuntu 16.04 GCC 4.8

SDL
===

https://libsdl.org — Cross-platform windowing abstraction.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/sdl/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3ASDL)
-   **Latest known-good build**: [2.0.20](https://github.com/mosra/magnum-ci/actions/runs/2070884829) (2022-03-31)
    -   Ubuntu 18.04

SPIRV-Tools
===========

https://github.com/KhronosGroup/SPIRV-Tools — Tools for SPIR-V (dis)assembly,
validation and optimization.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/spirv-tools/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3ASPIRV-Tools)
-   **Latest known-good build**: [2020.4](https://github.com/mosra/magnum-ci/actions/runs/454588347) (2020-12-31)
    -   Windows MSVC2019
    -   Windows MSVC2019 Debug
    -   Windows MSVC2017
    -   Windows MSVC2017 Debug
    -   Ubuntu 16.04
    -   Ubuntu 16.04 GCC 4.8

SwiftShader
===========

https://github.com/google/swiftshader — Software implementation of OpenGL ES
and Vulkan.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/swiftshader/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3ASwiftShader)
-   **Latest known-good build**: [r5464.a6940c8e6e](https://github.com/mosra/magnum-ci/actions/runs/251407425), [upstream commit](https://github.com/google/swiftshader/commit/a6940c8e6e) (2020-09-09)
    -   using LLVM 7 (not 10 yet, although it's available)
    -   Windows MSVC2019 (MSVC2017 build not done because CMake 3.13
        required by SwiftShader isn't available on the image)
    -   macOS 10.15
    -   Ubuntu 16.04 (only OpenGL ES, Vulkan doesn't build on GCC 5)
    -   Ubuntu 18.04

Vulkan Loader
=============

https://github.com/KhronosGroup/Vulkan-Loader — Vulkan entry-point, providing
device enumeration and layer loading. Shipped with Vulkan SDK on Windows and
Mesa on Linux, however on macOS people usually use MoltenVK directly, which is
why we build our own (and we don't want to install the full SDK in CI builds as
it's too much).

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/vulkan-loader/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3A"Vulkan+Loader")
-   **Latest known-good build**: [1.2.153](https://github.com/mosra/magnum-ci/actions/runs/246455131) (2020-09-09)
    -   macOS 10.15

zlib
====

https://github.com/madler/zlib — data compression library

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/openexr/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3Aopenexr)
-   **Latest known-good build**: [1.2.11](https://github.com/mosra/magnum-ci/actions/runs/716471861) (2021-04-04)
    -   Windows MSVC2019
    -   Windows MSVC2017
    -   Windows MinGW
