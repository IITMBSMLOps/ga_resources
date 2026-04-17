# 🎥 OBS Recording Profiles

This repository provides **two optimized OBS Studio profiles** (`Quality-720p.ini` and `Quality-1080p.ini`) designed for — compact file sizes with clear voice and screen quality.
Both use **MKV** for crash-safe recording and efficient compression with **H.264 (x264)** codec.

---

## 📦 Profiles Overview

| Profile File        | Resolution | FPS | Avg. Size (1 hr) | Use Case                                  |
| ------------------- | ---------- | --- | ---------------- | ----------------------------------------- |
| `Quality-720p.ini`  | 1280×720   | 25  | ~250–300 MB      | Meetings, lectures, screen shares         |
| `Quality-1080p.ini` | 1920×1080  | 30  | ~450–550 MB      | Tutorials, YouTube, high-clarity captures |

Both profiles share:

* 💾 **MKV recording** (safer than MP4 — no corruption if crash)
* 🎞 **H.264 (x264)** codec, tuned for compact size, use H.265 for better compression if your system supports it
* 🔉 **Mono audio (64 kbps AAC)** — ideal for voice
* ⚡ **Veryfast preset + Baseline profile + Zerolatency tune**

---

## ⚙️ Installation Guide

### 1️⃣ Locate Your OBS Profiles Folder

| OS          | Path                                                       |
| ----------- | ---------------------------------------------------------- |
| **Windows** | `%AppData%\obs-studio\basic\profiles\`                     |
| **macOS**   | `~/Library/Application Support/obs-studio/basic/profiles/` |
| **Linux**   | `~/.config/obs-studio/basic/profiles/`                     |

---

### 2️⃣ Create Folders and Copy Files

Inside your `profiles` folder, create:

```
720p-Balanced-MKV/
1080p-HQ-MKV/
```

Then copy the downloaded `.ini` files:

```
Quality-720p.ini  →  720p-Balanced-MKV/basic.ini
Quality-1080p.ini →  1080p-HQ-MKV/basic.ini
```

Your directory should look like this:

```
obs-studio/
└── basic/
    └── profiles/
        ├── 720p-Balanced-MKV/
        │   └── basic.ini
        └── 1080p-HQ-MKV/
            └── basic.ini
```

---

### 3️⃣ Load the Profile in OBS

1. Open **OBS Studio**
2. Go to **Profile → Select Profile**
3. Choose:

   * `720p-Balanced-MKV` for lighter recording
   * `1080p-HQ-MKV` for higher clarity

That’s it — you’re ready to record!

---

## 💡 Output Configuration Details

| Setting | 720p Profile       | 1080p Profile      |
| ------- | ------------------ | ------------------ |
| Format  | MKV                | MKV                |
| Codec   | x264 (H.264)       | x264 (H.264)       |
| Bitrate | 600 kbps           | 1200 kbps          |
| FPS     | 25                 | 30                 |
| Audio   | AAC, Mono, 64 kbps | AAC, Mono, 64 kbps |
| Preset  | Veryfast           | Veryfast           |
| Profile | Baseline           | Baseline           |
| Tune    | Zerolatency        | Zerolatency        |

---

## 🪴 Converting MKV → MP4 (Instant, No Quality Loss)

OBS records to MKV by default for safety.
To convert (remux) recordings for easy sharing or editing:

1. In OBS, go to **File → Remux Recordings**
2. Select your `.mkv` file
3. Click **Remux**

✅ OBS creates an `.mp4` instantly — **no re-encoding, no quality loss.**

---

## 🧠 Tips

* MKV is **crash-safe** — even if your laptop crashes or OBS stops, your recording is saved.
* You can safely edit these `.ini` profiles to adjust bitrate, resolution, or frame rate.
* For laptops with **NVIDIA GPUs**, switch encoder to **NVENC (H.264)** to reduce CPU load.
* These profiles are optimized for **voice, webcam, and screen share content**, not high-motion gaming.

