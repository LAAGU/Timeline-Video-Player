<div align="center">

<img src="assets/icon.png" width="96" alt="Timeline logo" />

# Timeline

**A fast, free media player and screen recorder for Windows.**<br/>
Seek previews, frame-accurate trimming, one-key clips, and watching together in sync.<br/>
<sub>New in 2.0: rebuilt to be tiny (a 5 MB download) and light, using 2-3x less memory.</sub>

[![Latest release](https://img.shields.io/github/v/release/LAAGU/Timeline-Video-Player?label=latest&color=0099ff&style=flat-square)](../../releases/latest)
[![Installer downloads](https://img.shields.io/endpoint?url=https%3A%2F%2Ftimeline.softwaretrinkets.com%2Fapi%2Fbadge%2Fdownloads&style=flat-square)](../../releases)
![Windows 10 | 11](https://img.shields.io/badge/Windows-10%20%7C%2011-2b2b33?style=flat-square)
![Free](https://img.shields.io/badge/price-free-30d158?style=flat-square)

<a href="../../releases/latest"><img src="https://img.shields.io/badge/Download_for_Windows-0099ff?style=for-the-badge" alt="Download for Windows" height="36" /></a>
&nbsp;
<a href="https://timeline.softwaretrinkets.com"><img src="https://img.shields.io/badge/Website-17171f?style=for-the-badge" alt="Website" height="36" /></a>

<br/>

<picture>
  <source media="(prefers-color-scheme: light)" srcset="assets/screenshots/player-light.webp" />
  <img src="assets/screenshots/player-dark.webp" alt="Timeline playing a video, with the file list on the right" width="100%" />
</picture>

[Lighter in 2.0](#-lighter-in-20) · [Player](#-player) · [Recorder](#-recorder) · [Watch together](#-watch-together) · [Shortcuts](#-keyboard-shortcuts) · [Privacy](#-privacy) · [FAQ](#-faq)

</div>

---

## ✨ Highlights

|  |  |  |
|---|---|---|
| 🖼️ **Seek previews**<br/><sub>Hover the timeline to see that moment before you jump.</sub> | ✂️ **Frame-accurate trimming**<br/><sub>Cut the start and end, save a new file. No editor needed.</sub> | ⚡ **One-key clips**<br/><sub>Always keeps the last seconds ready. <kbd>Alt</kbd>+<kbd>F10</kbd> saves them.</sub> |
| 🔴 **GPU screen recording**<br/><sub>NVIDIA, AMD and Intel encoders: H.264, H.265 and AV1.</sub> | 👥 **Watch together**<br/><sub>A 6-digit code, synced playback and chat. No upload.</sub> | 🪶 **Tiny and light**<br/><sub>A 5 MB download. 2-3x less memory than 1.x.</sub> |
| 📊 **Best settings for my PC**<br/><sub>Recorder settings picked for your graphics card and screen.</sub> | 🎮 **Game benchmark**<br/><sub>Your game's exact FPS, what Timeline costs it, and why frames drop.</sub> | 🆓 **Free**<br/><sub>No account, no ads, nothing else to install.</sub> |
| 📺 **Streams and free TV**<br/><sub>Any video or stream link, or thousands of free channels.</sub> | 💬 **Captions online**<br/><sub>Find captions for the video you're watching. No account needed.</sub> | 🎨 **Caption style**<br/><sub>Your colour, size, font, outline and background.</sub> |

---

## 🪶 Lighter in 2.0

Timeline 2.0 is rebuilt on a much lighter base (Tauri and Rust instead of Electron and ffmpeg). Everything is still here; it just takes far less from your PC. Updating from 1.x is automatic and keeps your settings.

|  | 1.4.4 (Electron + ffmpeg) | **2.0 (Tauri)** |
|---|---|---|
| Download | about 260 MB | **about 5 MB** |
| Installed size | almost 1 GB | **about 14 MB** |
| Memory, idle | 179 MB | **108 MB** |
| Memory while recording | 499 MB | **162 MB** |
| CPU while recording | 1.1 % | **0.2 %** |
| Trim 60 s of video | **8.8 s** (16.5 % CPU) | 11.2 s (1.4 % CPU) |
| Compress to 50 MB | 11.1 s | 11.4 s |

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/perf/memory-dark.png" />
  <img src="assets/perf/memory-light.png" alt="Memory used per task: 1.4.4 versus 2.0" width="100%" />
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/perf/cpu-dark.png" />
  <img src="assets/perf/cpu-light.png" alt="CPU used per task: 1.4.4 versus 2.0" width="100%" />
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/perf/time-dark.png" />
  <img src="assets/perf/time-light.png" alt="Time taken per task: 1.4.4 versus 2.0" width="100%" />
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/perf/data-moved-dark.png" />
  <img src="assets/perf/data-moved-light.png" alt="Data moved per second while capturing: 1.4.4 versus 2.0" width="100%" />
</picture>

<details>
<summary><b>More charts: GPU, and memory / CPU over each task</b></summary>
<br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/perf/gpu-dark.png" />
  <img src="assets/perf/gpu-light.png" alt="GPU used per task: 1.4.4 versus 2.0" width="100%" />
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/perf/memory-over-time-dark.png" />
  <img src="assets/perf/memory-over-time-light.png" alt="Memory over each task: 1.4.4 versus 2.0" width="100%" />
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/perf/cpu-over-time-dark.png" />
  <img src="assets/perf/cpu-over-time-light.png" alt="CPU over each task: 1.4.4 versus 2.0" width="100%" />
</picture>
</details>

<details>
<summary><b>How it was measured</b></summary>
<br/>

- **PC:** Ryzen 7 7800X3D (16 threads), RTX 5070, 32 GB, Windows 11. Both versions built for release and run one after the other with fresh settings, 3 runs each (the charts show the middle one; the "over each task" charts show a single run).
- **Same settings in both:** H.264 on the RTX 5070, 60 fps, 15 Mb/s. Test video: 2 minutes, 1920x1080, 60 fps.
- **Tasks:** idle; trim 60 s of the video (frame-exact in both); compress the video to 50 MB ("Medium" preset in both); record a window playing the video for 60 s; clipping for 60 s, then save a 30 s clip.
- **What counts:** every process each version runs (1.4.4: its window and helper processes, recorder service and ffmpeg; 2.0: the app and its window). Memory = private memory, as Task Manager shows it. CPU = share of all 16 threads. GPU = the busiest engine. "Data moved" = what the processes read and write, including the pipes between them: 1.4.4 passes every raw frame from its capture helper to ffmpeg, while 2.0 keeps frames on the graphics card. It is not disk load: the disk stayed 1-2 % busy in both.
</details>

---

## 🎬 Player

<table>
  <tr>
    <td width="50%"><img src="assets/screenshots/seek-preview.webp" alt="A preview picture above the seek bar" /><br/><sub><b>Seek previews:</b> hover the timeline for a picture of that moment.</sub></td>
    <td width="50%"><img src="assets/screenshots/trim.webp" alt="The trim bar with two handles and the Save trim panel" /><br/><sub><b>Trimming:</b> drag the handles, name the file, Save trim.</sub></td>
  </tr>
</table>

- **Plays what you have:** MP4, MKV, WebM, AVI and MOV, plus MP3, WAV, OGG, AAC, M4A, FLAC, Opus and WEBA. Broken files and AVIs are repaired or converted on the fly (some very old AVI codecs aren't supported yet; more formats will come with updates).
- **Seek previews:** 20 pictures per video, made in the background (they can be switched off).
- **Frame-accurate trimming** with a Save trim panel and a progress bar. The original file is never changed.
- **Playback speed** from 0.1x to 16x, **frame stepping**, jump to 10%…100% with the number keys, fullscreen, and **picture-in-picture** in a small window that stays on top.
- **Captions** (SRT and VTT) with a delay setting, **found online** for the video you're watching (from OpenSubtitles, in your languages, no account needed), and your own **caption style**: colour, size, font, outline, shadow and background.
- **Streams and free TV:** paste any video or stream link (MP4, HLS `.m3u8` and more), or browse thousands of free channels by country, category or language, each with a green / yellow / red dot showing how fast its server answers. Old broadcast channels (MPEG-2, HEVC, Dolby sound) are converted on your graphics card and play a few seconds behind live without stopping; a **sound sync** setting fixes channels whose sound is off.
- **Compress** a video to a target size with your graphics card's encoder (NVIDIA, AMD, Intel) or Windows' own, and **upload** it to Gofile to get a link.
- **Ambient mode:** a soft glow of the video's colours behind the player.
- **File list** with thumbnails, filters and sorting. Open files from Explorer, or make Timeline your default player.
- **Themes:** Dark, Light, or follow Windows.

<details>
<summary><b>See the player settings</b></summary>
<br/>
<img src="assets/screenshots/player-settings.webp" alt="The player settings: auto play, trimming, ambient mode, seek previews, speed, captions, hotkeys" />
</details>

---

## 🔴 Recorder

<table>
  <tr>
    <td width="50%"><img src="assets/screenshots/recorder.webp" alt="The Recorder tab with its video settings" /><br/><sub><b>Your settings:</b> display or one window, resolution, fps, encoder, bitrate.</sub></td>
    <td width="50%"><img src="assets/screenshots/recorder-clips.webp" alt="The Clips tab with clip lengths from 15 seconds to 5 minutes" /><br/><sub><b>Clipping:</b> choose how far back a clip goes.</sub></td>
  </tr>
</table>

- **Record** a whole display, one window, or any fullscreen window, encoded on your graphics card (NVIDIA, AMD or Intel: H.264, H.265 and AV1 where the card supports them), or with Windows' own H.264 encoder on the CPU. Captured frames stay on the graphics card all the way to the file.
- **Clipping (replay buffer):** turn on **Clipping** and Timeline keeps the last 15 seconds to 5 minutes on disk (or any length from 5 s to 10 min). <kbd>Alt</kbd>+<kbd>F10</kbd> saves a clip instantly, without re-encoding. Recording and clipping can run at the same time.
- **Audio:** desktop sound, your microphone, or both, mixed or on separate tracks. When you capture one window, it can record just that program's sound.
- **Your settings:** resolution, frame rate, bitrate in Kbps (constant or variable), encoder and quality preset, and **MKV** (survives crashes) or **MP4**.
- **Runs from the tray** with the window closed, can start with Windows and start clipping by itself.
- **Safe:** crash recovery for unfinished recordings, a disk-space guard, and automatic resume after a lock screen or sleep.
- **Pop-up notifications** with buttons (*Open clip*, *Show in folder*) and their own sound, shown over borderless and windowed games.
- **Live preview** of what is being recorded, and Timeline's own CPU, memory and GPU use.

<details>
<summary><b>See the audio settings</b></summary>
<br/>
<img src="assets/screenshots/recorder-audio.webp" alt="The Audio tab: desktop audio, microphone, tracks and quality" />
</details>

### 📊 Performance tab

<table>
  <tr>
    <td width="50%" align="center"><img src="assets/screenshots/performance-settings.webp" alt="Best settings for my PC: each suggested setting with the reason" width="374" /><br/><sub><b>Best settings for my PC:</b> each setting with the reason; nothing changes until you apply it.</sub></td>
    <td width="50%" align="center"><img src="assets/screenshots/performance-benchmark.webp" alt="Benchmark results: average and low FPS, stutters, what Timeline used, frame rate drops with their cause" width="374" /><br/><sub><b>Benchmark:</b> exact FPS, stutters, what Timeline used, and why frames dropped.</sub></td>
  </tr>
</table>

- **Best settings for my PC** looks at your graphics card, screen, CPU and memory, and suggests the encoder, preset, frame rate, resolution and bitrate that record well without slowing your games, each with the reason.
- **Benchmark:** start it (or press <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>B</kbd> in game), play, and stop. Timeline reads your game's exact frame times (Windows asks once for administrator rights), measures what Timeline itself used, and explains every drop: Timeline, a busy CPU or GPU, or the game itself. Graphs show **what else was running** on your PC (CPU, graphics card, memory and disk per app) and your PC's limits; click a drop to see exactly what ran at that moment. That part stays on your PC and is never sent. Copy the results as text, open them as a graph, or send them to the developer with a note.

<details>
<summary><b>See the benchmark graph</b></summary>
<br/>
<img src="assets/screenshots/benchmark-graph.webp" alt="The benchmark graph: frame rate, every frame's time, and the CPU / GPU load on one time line, with drops and Timeline's actions marked" />
</details>

---

## 👥 Watch together

<table>
  <tr>
    <td width="50%"><img src="assets/screenshots/watch-host.webp" alt="The Host dialog: name, password, how others reach you, session options" /><br/><sub><b>Host:</b> pick a name, an optional password and how guests connect.</sub></td>
    <td width="50%"><img src="assets/screenshots/watch-together.webp" alt="A session with the chat panel and the session code" /><br/><sub><b>Watch:</b> everyone on the same second, with chat beside the video.</sub></td>
  </tr>
</table>

- **Host** the open video and share a **6-digit code** (optional password) or an invite link `timeline://join/<code>`.
- **In sync:** play, pause, seek and speed follow everyone. The host decides whether everyone can control playback or only the host.
- **Chat and a session log** (who paused, seeked, joined, left), shared captions and seek previews, and per-person network numbers.
- **The host is in charge:** kick, ban and unban, and pause everyone while someone is loading.
- **No upload:** the video streams straight from the host's PC, through automatic UPnP, a tunnel address (playit.gg, ngrok) or the same network. Every viewer needs Timeline.

---

## ⚙️ Settings

<img src="assets/screenshots/settings.webp" alt="The Settings window on its General page" />

One window with **General, Player, Recorder, Cache, Logs** and **About**: theme, start-up and closing behaviour, notifications, the default player, every hotkey, a **cache manager** that shows what Timeline stores and clears it, readable logs for bug reports (and a button to send a problem report to the developer), and the release notes.

---

## ⚡ Keyboard shortcuts

Every shortcut can be changed in Settings. Recorder shortcuts can also be a **single key** (<kbd>F1</kbd> to <kbd>F24</kbd>, <kbd>Insert</kbd>, <kbd>Home</kbd>, <kbd>Page Up</kbd> …), and the key keeps working in your game or browser too.

| Player | | Recorder (work anywhere) | |
|---|---|---|---|
| <kbd>Space</kbd> | Play / pause | <kbd>Alt</kbd>+<kbd>F11</kbd> | Start recording |
| <kbd>←</kbd> <kbd>→</kbd> | Skip 10 s | <kbd>Alt</kbd>+<kbd>F12</kbd> | Stop recording |
| <kbd>Ctrl</kbd>+<kbd>←</kbd> <kbd>→</kbd> | One frame back / forward | <kbd>Alt</kbd>+<kbd>F10</kbd> | Save a clip |
| <kbd>↑</kbd> <kbd>↓</kbd> | Volume | <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>B</kbd> | Start / stop a benchmark |
| <kbd>1</kbd> … <kbd>9</kbd>, <kbd>0</kbd> | Jump to 10% … 100% | | |
| <kbd>M</kbd> · <kbd>F</kbd> · <kbd>Shift</kbd>+<kbd>P</kbd> | Mute · Fullscreen · Picture-in-picture | | |
| <kbd>D</kbd> · <kbd>A</kbd> | Next · Previous file | | |
| <kbd>Ctrl</kbd>+<kbd>S</kbd> | Player settings | | |

---

## 📦 Download

1. Get the installer from the **[latest release](../../releases/latest)** (or the [website](https://timeline.softwaretrinkets.com)).
2. Run it. That's all: everything Timeline needs is in the 5 MB installer.
3. Timeline updates itself from GitHub releases, and shows what's new after each update. On 1.x? It moves to 2.0 by itself and keeps your settings.

**Requires** Windows 10 or 11.

---

## 🔒 Privacy

Your files, recordings and clips **stay on your PC**. Watch together streams directly between the people in a session, and the chat never touches a database.

Timeline can share **anonymous usage data** to find bugs and decide what to improve. You can switch it off in **Settings → About → Usage data**.

| Sent | Never sent |
|---|---|
| App version, Windows build, CPU type, rounded RAM | Your name, PC name or IP address |
| Time zone and language | File names, folders or anything you play or record |
| How often features are used (counts only) | Web addresses or e-mail addresses |
| Grouped error messages, with file paths removed | |

**Captions online:** a search sends only the video's file name and a fingerprint to OpenSubtitles, never the video, and only when you press *Search*. **Streams** play straight from the channel's own server.

**Problem reports and benchmarks** are sent to the developer only when you press *Send* (Settings → Logs, Recorder → Performance), with file names, paths and e-mail addresses removed first.

---

## 📚 Guides

Step-by-step guides for every feature are on the website:

- [Save the last 30 seconds of gameplay with one key](https://timeline.softwaretrinkets.com/blog/save-the-last-30-seconds-of-gameplay-on-windows)
- [Record your screen with GPU encoding](https://timeline.softwaretrinkets.com/blog/record-your-screen-on-windows-with-gpu-encoding)
- [Watch videos together with friends](https://timeline.softwaretrinkets.com/blog/watch-videos-together-with-friends-on-windows)
- [Trim a video frame-accurately](https://timeline.softwaretrinkets.com/blog/trim-a-video-on-windows-frame-accurately)
- [Every feature, in one page](https://timeline.softwaretrinkets.com/blog/timeline-features-complete-guide)

---

## ❓ FAQ

<details>
<summary><b>Is Timeline really free?</b></summary>
<br/>
Yes. No paywalls, no ads, no account.
</details>

<details>
<summary><b>Does it work on macOS or Linux?</b></summary>
<br/>
Not yet. Timeline is made for Windows 10 and 11.
</details>

<details>
<summary><b>Where are my recordings and clips saved?</b></summary>
<br/>
By default in a <code>Timeline</code> folder inside your Videos folder. You can change both folders in the Recorder's <b>More</b> tab.
</details>

<details>
<summary><b>A recorder hotkey does nothing.</b></summary>
<br/>
Another program (often a GPU overlay, which can use <kbd>Alt</kbd>+<kbd>F10</kbd>) owns the key. Timeline shows a warning; pick a new key in the Recorder's <b>Keys</b> tab.
</details>

<details>
<summary><b>Why does the benchmark ask for administrator rights?</b></summary>
<br/>
To read your game's exact frame times, Timeline uses Windows' own frame tracing (the same as PresentMon), which Windows only allows with administrator rights. It asks once when a benchmark starts; nothing else in Timeline ever needs them.
</details>

<details>
<summary><b>Do my friends need the video for watch together?</b></summary>
<br/>
No. The video streams from the host's PC; guests only need Timeline and the code.
</details>

---

## 💡 Why Timeline?

Most media players are slow, outdated, bloated or just hard to use. I felt the same, so I built Timeline, and now I'm sharing it with you. It focuses on speed, simplicity and a clean experience, and it is actively developed.

## 💬 Feedback

Found a bug or have an idea? [Open an issue](../../issues), or e-mail me at **sukritthakur821@gmail.com**.

<div align="center">
<sub>Made by <a href="https://github.com/LAAGU">LAAGU</a> · Powered by <a href="https://www.softwaretrinkets.com">softwaretrinkets</a></sub>
</div>
