# **Super Mario Galaxy 63 – 4K Texture Pack (PNG & DDS)**

This repository contains a complete texture pack for **Super Mario Galaxy 63**, a ROM hack of *Super Mario Galaxy 2*.
The textures are available in two formats:

* **DDS Texture Pack** – Optimized for in-game use in Dolphin Emulator (fast loading, smaller file size)
* **PNG Texture Pack** – For development/editing only (do **not** use in-game)

> **Just want to play?** Download the **latest release** here instead of cloning the whole repo:
> **Releases:** [https://github.com/iZePlayzYT/SuperMarioGalaxy63-TexturePack/releases](https://github.com/iZePlayzYT/SuperMarioGalaxy63-TexturePack/releases)

---

## **Table of Contents**

1. [Texture Packs](#texture-packs)
2. [How to Install Custom Textures in Dolphin](#how-to-install-custom-textures-in-dolphin)
3. [Upscaling & Conversion Process](#upscaling--conversion-process)
4. [Unmodified Texture Dumps](#unmodified-texture-dumps)
5. [Contributing](#contributing)
6. [Credits](#credits)

---

## **Texture Packs**

The repository is organized into the following folders:

* **`DDS/`** → DDS textures (**use these in-game**)
* **`PNG/`** → PNG textures (**for development/editing only**)
* **`DUMPS/`** → Original, unmodified textures dumped from the game

---

## **How to Install Custom Textures in Dolphin**

### **1. Preparing Dolphin Emulator**

Ensure the latest version of Dolphin Emulator is installed:
[https://dolphin-emu.org/](https://dolphin-emu.org/)

### **2. Configuring Dolphin Emulator Settings**

1. Open Dolphin Emulator
2. Go to `Graphics Settings` → `Advanced` and:

   * **Enable:** Load Custom Textures
   * **Disable:** Prefetch Custom Textures

### **3. Placing the DDS Textures**

Navigate to Dolphin’s **User Directory**:

* **Windows**: `C:\Users\<YourUsername>\AppData\Roaming\Dolphin Emulator\Load\Textures\`
* **macOS**: `~/Library/Application Support/Dolphin/Load/Textures/`
* **Linux**: `~/.local/share/dolphin-emu/Load/Textures/`

You have two options:

#### **Option A – General Folder (SB4)**

If you downloaded the ZIP of a release, it contains a **folder named `SB4`** which works for **all versions** of the game.
Place the **entire `SB4` folder** from the release ZIP directly into your `Load/Textures/` directory.

**Important:** If you use the general `SB4` folder, make sure there are **no version-specific folders** (`SB4E01`, `SB4P01`, `SB4J01`, etc.) in `Load/Textures/`,
otherwise Dolphin will load textures from those instead and ignore `SB4`.

#### **Option B – Version-Specific Folder**

If you prefer, create the folder for your specific game version and place the **DDS textures** inside:

* **SB4E01** → NTSC-U (*Super Mario Galaxy 2*)
* **SB4P01** → PAL (*Super Mario Galaxy 2*)
* **SB4J01** → NTSC-J (*Super Mario Galaxy 2*)

If the folder doesn’t exist, create it manually.

**Do not** use PNG files in-game.

---

## **Upscaling & Conversion Process**

### **Upscaling with Chainner**

1. Install **Chainner**: [https://github.com/chaiNNer-org/chaiNNer/releases](https://github.com/chaiNNer-org/chaiNNer/releases)
2. In Chainner’s **Dependency Manager**, install: **PyTorch**, **NCNN**, **ONNX** (including all sub-packages).
3. Open the chain from `UPSCALING.chn`.
4. Download the 4 model files referenced by the chain from: [https://github.com/Venomalia/Hdcube](https://github.com/Venomalia/Hdcube)
5. In Chainner, set:

   * **Input folder** → the textures you want to upscale
   * **Output folder** → where processed files are written
   * Paths for all 4 model files used in the chain
6. Press **Start** to run the pipeline. *(Tip: lock the chain via the lock icon to avoid accidental edits while running.)*

---

### **Converting PNG to DDS (Recommended Method)**

DDS textures for in-game use should be created using **Custom Texture Tool PS** (CTT-PS) with the exact settings shown below.

**Download CTT-PS:**
[https://github.com/epicboy/Custom-Texture-Tool/releases](https://github.com/epicboy/Custom-Texture-Tool/releases)

**Settings:** <br><img width="563" height="785" alt="image" src="https://github.com/user-attachments/assets/71a5e7a5-bad7-4c06-91c0-04a87c731777"/>

---

## **Unmodified Texture Dumps**

Unmodified texture dumps are provided in the `DUMPS/` folder.
These are the original, raw textures before any processing—useful for reference or further editing.

---

## **Contributing**

Pull requests are welcome. To keep both packs synchronized:

* **Every change must include both PNG (development) and DDS (in-game) versions.**
* PRs that only update one format will **not** be merged.

**Steps:**

1. Fork the repository
2. Make edits in **PNG**, then convert to **DDS** using the recommended settings
3. Update both `PNG/` and `DDS/`
4. Open a pull request describing your changes

---

## **Credits**

* **iZePlayz** — Main creator, dumping, upscaling, bug fixing, DDS conversion
* **SY24 & Super Hackio** — Various textures from their SMG2 HUD Remastered Texture Pack: [https://www.youtube.com/watch?v=\_TBhu-NfrX0](https://www.youtube.com/watch?v=_TBhu-NfrX0)
* **CDAMJC** — Various textures from his SMG2 HD Texture Pack: [https://forums.dolphin-emu.org/Thread-super-mario-galaxy-2-hd-texture-mod](https://forums.dolphin-emu.org/Thread-super-mario-galaxy-2-hd-texture-mod)
* **Remaining textures** — Created or reworked by iZePlayz

---
