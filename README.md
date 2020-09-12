This repository contains CI jobs for building Magnum and its dependencies.

[![Join the chat at https://gitter.im/mosra/magnum](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mosra/magnum?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

ANGLE
=====

https://github.com/google/angle — OpenGL ES implemented using D3D on Windows
and Metal on Mac.

-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3ASwiftShader)
-   **Latest known-good build**: [v4134](https://github.com/mosra/magnum-ci/actions/runs/165671594)
    -   Windows
    -   Windows UWP
    -   macOS

SwiftShader
===========

https://github.com/google/swiftshader — Software implementation of OpenGL ES
and Vulkan.

-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3ASwiftShader)
-   **Latest known-good build**: [r5464.a6940c8e6e](https://github.com/mosra/magnum-ci/actions/runs/246178301), [upstream commit](https://github.com/google/swiftshader/commit/a6940c8e6e)
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

-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3A"Vulkan+Loader")
-   **Latest known-good build**: [1.2.153](https://github.com/mosra/magnum-ci/actions/runs/246455131)
    -   macOS 10.15
