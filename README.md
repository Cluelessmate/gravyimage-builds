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
3. Choose your ComfyUI folder when asked (the portable ComfyUI, for example `ComfyUI_windows_portable`, from <https://github.com/comfyanonymous/ComfyUI/releases>).
4. In **Settings > Models**, pick sizes that fit your graphics card and download what you need. Downloads can be paused and resumed. If asked, click the button to install the GGUF loader.

Images are saved to `Pictures\gravyimages` unless you change it in Settings. The app keeps its settings in a `data` folder next to the exe and runs its own private ComfyUI on port 8190, which stops when you close the app. It never touches another ComfyUI you have running.

## Requirements

- Windows 10 or 11 with the WebView2 runtime (included with Windows 11)
- An NVIDIA graphics card (the model sizes are chosen by your VRAM; 16 GB suits the recommended edit model)
- A ComfyUI install that includes its own Python
- Disk space for the models you download (Edit alone is about 13 GB)

## Status

Early builds, tested on one machine so far. Models are downloaded from Hugging Face under their own licences.
