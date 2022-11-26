This repository contains CI jobs for building Magnum and its dependencies.

[![Join the chat at https://gitter.im/mosra/magnum](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mosra/magnum?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Magnum Tools
============

`magnum-imageconverter`, `magnum-sceneconverter`, `magnum-shaderconverter`,
`magnum-gl-info`, `magnum-vk-info`, `magnum-player`, importer and
image/scene/shader converter plugins; Python 3.8, ~~3.9,~~ and 3.10 bindings.

-   **Build file:** [`magnum-tools.yml`](https://github.com/mosra/magnum-ci/blob/magnum-tools/.github/workflows/magnum-tools.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions/workflows/magnum-tools.yml), automatically built every Monday and Thursday
    -   Ubuntu 18.04+

Dependencies
============

As the intent is to link these to self-contained plugin modules in most cases,
all libraries are built as static. Stripped `Release` binaries unless said
otherwise.

ANGLE
-----

https://github.com/google/angle — OpenGL ES implemented using D3D on Windows
and Metal on Mac.

-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/angle/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3ASwiftShader)
-   **Latest known-good build**: [v4134](https://github.com/mosra/magnum-ci/actions/runs/252324081) (2020-09-13)
    -   Windows
    -   Windows UWP
    -   macOS

Assimp
------

https://www.assimp.org — Asset import library.

-   **Used by:** [AssimpImporter](https://doc.magnum.graphics/magnum/classMagnum_1_1Trade_1_1AssimpImporter.html)
-   **Build file:** [`assimp.yml`](https://github.com/mosra/magnum-ci/blob/assimp/.github/workflows/assimp.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions/workflows/assimp.yml)
    -   Windows MSVC2019+
    -   Windows MSVC2019+ Debug
    -   ~~Windows MSVC2017~~
    -   ~~Windows MSVC2017 Debug~~
    -   Windows MinGW
    -   Ubuntu 18.04+

FreeType
--------

https://www.freetype.org — Font rendering library.

-   **Used by:** [FreeTypeFont](https://doc.magnum.graphics/magnum/classMagnum_1_1Text_1_1FreeTypeFont.html)
-   **Build file:** [`build.yml`](https://github.com/mosra/magnum-ci/blob/freetype/.github/workflows/build.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions?query=workflow%3AFreeType)
-   **Latest known-good build**: [2.10.4](https://github.com/mosra/magnum-ci/actions/runs/454639188) (2020-12-31)
    -   Windows MSVC2019
    -   Windows MSVC2017

Glslang
-------

https://github.com/KhronosGroup/glslang — GLSL validator and GLSL-to-SPIR-V
compiler.

-   **Used by:** [GlslangShaderConverter](https://doc.magnum.graphics/magnum/classMagnum_1_1ShaderTools_1_1GlslangConverter.html)
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
-------------

https://github.com/libjpeg-turbo/libjpeg-turbo — libjpeg with SIMD
acceleration.

-   **Used by:** [JpegImporter](https://doc.magnum.graphics/magnum/classMagnum_1_1Trade_1_1JpegImporter.html), [JpegImageConverter](https://doc.magnum.graphics/magnum/classMagnum_1_1Trade_1_1JpegImageConverter.html)
-   **Build file:** [`libjpeg-turbo.yml`](https://github.com/mosra/magnum-ci/blob/libjpeg-turbo/.github/workflows/libjpeg-turbo.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions/workflows/libjpeg-turbo.yml)
    -   Windows MSVC2019+
    -   ~~Windows MSVC2017~~
    -   No MinGW build due to ABI issues
        (`undefined reference to '__imp___acrt_iob_func'`) when used on
        AppVeyor with GCC 7.2
    -   Ubuntu 18.04+

libpng
------

https://github.com/glennrp/libpng — Portable Network Graphics.

-   **Used by:** [PngImporter](https://doc.magnum.graphics/magnum/classMagnum_1_1Trade_1_1PngImporter.html), [PngImageConverter](https://doc.magnum.graphics/magnum/classMagnum_1_1Trade_1_1PngImageConverter.html)
-   **Depends on**: [zlib](#zlib)
-   **Build file:** [`libpng.yml`](https://github.com/mosra/magnum-ci/blob/libpng/.github/workflows/libpng.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions/workflows/libpng.yml)
    -   Windows MSVC2019+
    -   No MinGW build due to ABI issues
        (`undefined reference to '__security_cookie'`) when used on
        AppVeyor with GCC 7.2
    -   Ubuntu 18.04+

libwebp
-------

https://github.com/webmproject/libwebp — a library to encode and decode images
in WebP format.

-   **Used by:** [WebPImporter](https://doc.magnum.graphics/magnum/classMagnum_1_1Trade_1_1WebPImporter.html)
-   **Build file:** [`libwebp.yml`](https://github.com/mosra/magnum-ci/blob/libwebp/.github/workflows/libwebp.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions/workflows/libwebp.yml)
    -   Ubuntu 18.04+

MeshOptimizer
-------------

https://github.com/zeux/meshoptimizer — mesh optimization library that makes
meshes smaller and faster to render.

-   **Used by:** [MeshOptimizerSceneConverter](https://doc.magnum.graphics/magnum/classMagnum_1_1Trade_1_1MeshOptimizerSceneConverter.html)
-   **Build file:** [`meshoptimizer.yml`](https://github.com/mosra/magnum-ci/blob/meshoptimizer/.github/workflows/meshoptimizer.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions/workflows/meshoptimizer.yml)
    -   Windows MSVC2019+
    -   Windows MSVC2019+ Debug
    -   Windows MinGW
    -   Ubuntu 18.04+

OpenEXR
-------

https://github.com/AcademySoftwareFoundation/openexr — reference implementation
of the OpenEXR format.

-   **Used by:** [OpenExrImporter](https://doc.magnum.graphics/magnum/classMagnum_1_1Trade_1_1OpenExrImporter.html), [OpenExrImageConverter](https://doc.magnum.graphics/magnum/classMagnum_1_1Trade_1_1OpenExrImageConverter.html)
-   **Depends on**: [zlib](#zlib)
-   **Build file:** [`openexr.yml`](https://github.com/mosra/magnum-ci/blob/openexr/.github/workflows/openexr.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions/workflows/openexr.yml)
    -   Windows MSVC2019+
    -   Windows MSVC2019+ Debug
    -   ~~Windows MSVC2017~~
    -   ~~Windows MSVC2017 Debug~~
    -   Windows MinGW
    -   Ubuntu 18.04
    -   Ubuntu 18.04, version 2.5 with a system zlib dependency
    -   Ubuntu 18.04, version 2.5 with a system zlib dependency, GCC 4.8

SDL
---

https://libsdl.org — Cross-platform windowing abstraction.

-   **Used by:** [Sdl2Application](https://doc.magnum.graphics/magnum/classMagnum_1_1Platform_1_1Sdl2Application.html)
-   **Build file:** [`sdl.yml`](https://github.com/mosra/magnum-ci/blob/sdl/.github/workflows/sdl.yml)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions/workflows/sdl.yml)
    -   Ubuntu 18.04

SPIRV-Tools
-----------

https://github.com/KhronosGroup/SPIRV-Tools — Tools for SPIR-V (dis)assembly,
validation and optimization.

-   **Used by:** [SpirvToolsShaderConverter](https://doc.magnum.graphics/magnum/classMagnum_1_1ShaderTools_1_1SpirvToolsConverter.html)
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
-----------

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
-------------

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
----

https://github.com/madler/zlib — data compression library.

-   **Build file:** [`zlib.yml`](https://github.com/mosra/magnum-ci/blob/zlib/.github/workflows/zlib.yml)
-   **Required by:** [libpng](#libpng), [OpenEXR](#OpenEXR)
-   **All builds**: [GitHub Actions](https://github.com/mosra/magnum-ci/actions/workflows/zlib.yml)
    -   Windows MSVC2019+
    -   ~~Windows MSVC2017~~
    -   Windows MinGW
