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

Glslang
=======

https://github.com/KhronosGroup/glslang — GLSL validator and GLSL-to-SPIR-V
compiler.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/glslang/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3AGlslang)
-   **Latest known-good build**: [8.13.3743](https://github.com/mosra/magnum-ci/actions/runs/335427690) (2020-10-29)
    -   Windows MSVC2019
    -   Windows MSVC2019 Debug
    -   Ubuntu 16.04
    -   Ubuntu 16.04 GCC 4.8

SPIRV-Tools
===========

https://github.com/KhronosGroup/SPIRV-Tools — Tools for SPIR-V (dis)assembly,
validation and optimization.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/spirv-tools/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3ASPIRV-Tools)
-   **Latest known-good build**: [2020.04](https://github.com/mosra/magnum-ci/actions/runs/328842428) (2020-10-26)
    -   Windows MSVC2019
    -   Windows MSVC2019 Debug
    -   Ubuntu 16.04

SwiftShader
===========

https://github.com/google/swiftshader — Software implementation of OpenGL ES
and Vulkan.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/swiftshader/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3ASwiftShader)
-   **Latest known-good build**: [r5464.a6940c8e6e](https://github.com/mosra/magnum-ci/actions/runs/246178301), [upstream commit](https://github.com/google/swiftshader/commit/a6940c8e6e) (2020-09-09)
    -   using LLVM 7 (not 10 yet, although it's available)
    -   Windows MSVC2019
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
