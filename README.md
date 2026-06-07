# whisper-vulkan-win-x64

A prebuilt **Windows x64 build of [whisper.cpp](https://github.com/ggml-org/whisper.cpp)
with the Vulkan GPU backend** (`-DGGML_VULKAN=ON`). One build serves any Vulkan-capable
GPU (AMD / NVIDIA / Intel). Upstream publishes CUDA and CPU binaries but no Vulkan
binary, so this repo mirrors one for convenience.

The source is **unmodified upstream whisper.cpp**; only the build flags differ.

| | |
|---|---|
| Source | https://github.com/ggml-org/whisper.cpp (unmodified) |
| Commit | `610e664ba7cfe3af46125ed1b5a1184fccb51bcd` |
| Built | 2026-06-03 — LunarG Vulkan SDK 1.4.350.0, MSVC, Ninja, Release |
| License | MIT (see [LICENSE](LICENSE)) |

## Download

Grab `whisper-vulkan-win-x64.zip` from the [Releases](../../releases) page.

## Runtime requirements

- A Vulkan-capable GPU + driver (provides `vulkan-1.dll`)
- Microsoft Visual C++ Redistributable (x64)

## Run

```
whisper-server.exe -m ggml-large-v3-turbo.bin --host 127.0.0.1 --port 8080 -t 6 -l en
```

## Contents

`ggml-base.dll`, `ggml-cpu.dll`, `ggml-vulkan.dll`, `ggml.dll`, `whisper.dll`,
`whisper-server.exe`, plus the upstream MIT `LICENSE`.
