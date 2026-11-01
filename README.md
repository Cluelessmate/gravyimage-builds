# gravyimage builds

Portable Windows builds of **gravyimage**, a local AI image studio. It runs entirely on your own PC through your existing ComfyUI install:

- **Generate** images and logos with Z-Image Turbo
- **Edit** images with Qwen-Image-Edit 2511 (outfits, backgrounds, lighting) while keeping the person the same
- **Text and logo overlays** for things like YouTube thumbnails, plus background cut-outs
- **Restore resolution** back to the original size after an edit
- Before/after slider, prompt presets, several results per run, your own LoRAs, progress and cancel

This repository only holds the downloadable builds. The source code is private.

## Install

1. Download the latest `gravyimage-portable.zip` from [Releases](../../releases) and unzip it anywhere.
2. Run `gravyimage.exe`.
3. Choose your ComfyUI folder when asked (see [ComfyUI](#comfyui) below if you don't have it yet).
4. In **Settings > Models**, pick sizes that fit your graphics card and download what you need. Downloads can be paused and resumed. If asked, click the button to install the GGUF loader.

Images are saved to `Pictures\gravyimages` unless you change it in Settings. The app keeps its settings in a `data` folder next to the exe and runs its own private ComfyUI on port 8190, which stops when you close the app. It never touches another ComfyUI you have running.

## ComfyUI

gravyimage runs its models through ComfyUI. It was built and tested with **ComfyUI 0.43.0** (released 27 Oct 2026, Python 3.13, PyTorch 2.14 with CUDA 13). Newer versions should work; older ones may be missing nodes the app needs.

- NVIDIA, pinned to 0.43.0 (1.9 GB): <https://github.com/comfyanonymous/ComfyUI/releases/download/v0.43.0/ComfyUI_windows_portable_nvidia.7z>
- NVIDIA, always the newest: <https://github.com/comfyanonymous/ComfyUI/releases/latest/download/ComfyUI_windows_portable_nvidia.7z>
- Release page, with the other variants: <https://github.com/comfyanonymous/ComfyUI/releases/tag/v0.43.0>

Extract it with [7-Zip](https://www.7-zip.org/), then choose the extracted folder (the one containing `ComfyUI` and `python_embeded`) in gravyimage. You don't need to start ComfyUI yourself. If you already have a ComfyUI install, point the app at that instead; it is not modified apart from the GGUF loader add-on, which the app installs from Settings on request.

## Requirements

- Windows 10 or 11 with the WebView2 runtime (included with Windows 11)
- An NVIDIA graphics card (the model sizes are chosen by your VRAM; 16 GB suits the recommended edit model)
- ComfyUI 0.43.0 or newer, the Windows portable version (it includes its own Python)
- Disk space for the models you download (Edit alone is about 13 GB)

## Status

Early builds, tested on one machine so far. Models are downloaded from Hugging Face under their own licences.
