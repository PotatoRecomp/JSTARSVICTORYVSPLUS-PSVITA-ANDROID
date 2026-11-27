# J-Stars Victory VS+ — PS Vita Android Port

An unofficial native **Android (arm64)** static recompilation port of the PlayStation Vita version of **J-Stars Victory VS+** (`PCSE00595`, version `1.02`), powered by a Vulkan 1.1 renderer with profile-guided optimisation for mobile GPUs.

Download the latest APK from the [Releases](https://github.com/PotatoRecomp/JSTARSVICTORYVSPLUS-PSVITA-ANDROID/releases) page.

> [!NOTE]
> This repository and its releases do **not** include any game assets, game code, or encryption keys. You must provide your own legally acquired PS Vita dump of **J-Stars Victory VS+** (`PCSE00595`, base game + `1.02` update) along with `work.bin`.

## Features

- **Smooth 30 FPS gameplay** on arm64 Android devices with full 3D rendering, audio, and Vulkan 1.1 presentation (FIFO + single in-flight fence pacing for responsive touch and UI on both Mali and Adreno GPUs).
- **True Hor+ Widescreen**: expands horizontal field of view to fill wide phone screens without stretching or vertical cropping (**Aspect ratio**: `Full` or `Original`).
- **Built-in on-device Vita dump importer**: automatically decrypts and merges your Vita base game and `1.02` patch directly on your phone.
- **Controls**:
  - Customizable on-screen touch controls with per-button layout editor and FPS-style swipe camera look.
  - Physical USB/Bluetooth gamepad support with automatic touch-overlay hide/show (press **Select + Start** or **Guide** to open the menu).
- **In-game Android settings menu** (**☰** button):
  - **Display**: Render resolution (`0.5×`–`4×`), **Aspect ratio** (`Full` true Hor+ widescreen / `Original` 16:9), Anti-aliasing (`Off` / `FXAA` / `SSAA 2X–4X`), Upscaling (`Bilinear` / `FSR 1.0`), Texture filtering (`Off` / `2×`–`16×`).
  - **Performance**: V-Sync, Frameskip (`Off` / `1`–`3` / `Auto`), Shadows (`On` / `Half` / `Off`), Effects (`Full` / `Reduced` / `Off`), Custom GPU driver loader (e.g. Turnip), Adreno GPU clocks (`Normal` / `Max`), Shader cache export/clear, and top-center performance HUD (`FPS`, `Frame time`, `CPU`, `RAM`, `Temperature`, `Battery`).
  - **Game**: Volume, Capture frame, Quit.
  - **Controls**: Camera control (`Swipe` / `Right stick`), Camera sensitivity, Invert Y, Button size, Touch layout editor, Stick deadzone, Gyroscope.
  - **Cheats**: Unlock all characters, Infinite HP, Infinite stamina, Infinite Victory Burst.
- **Shader prewarm & persistent cache**: precompiles shader pipelines on startup to minimize in-battle stutter.

## Requirements

- **Architecture**: `arm64-v8a` (64-bit ARM)
- **OS**: Android 10 (API 29) or newer
- **Graphics**: Vulkan 1.1 capable GPU (Mali or Adreno)
- **Storage**: ~2 GB of free internal storage for the prepared game files
- **Game Dump**: Legally acquired PS Vita dump of `PCSE00595` (base + `1.02` update) with `work.bin`

## Installation

1. Download and install the latest APK from [Releases](https://github.com/PotatoRecomp/JSTARSVICTORYVSPLUS-PSVITA-ANDROID/releases).
2. Copy your legally acquired `PCSE00595` Vita dump into `/sdcard/JStars` on internal storage with both folders inside:
   ```text
   /sdcard/JStars/
   ├── app/PCSE00595/      (base game, including sce_sys/package/work.bin and sce_pfs/)
   └── patch/PCSE00595/    (version 1.02 update, including sce_pfs/)
   ```
3. Launch **J-Stars** and grant storage permission when prompted (**All files access** under *Special app access* if asked).
4. On first launch, the app will automatically decrypt and prepare the game files and precompile shaders.

## Disclaimer

No copyrighted game code, assets, or proprietary files are distributed here. **J-Stars Victory VS+** and its characters, assets, and trademarks belong to Bandai Namco Entertainment, Shueisha, and their respective creators. PlayStation Vita is a trademark of Sony Interactive Entertainment. This unofficial fan port is not affiliated with or endorsed by any of them.
