# PadLink

**Make game controllers your computer doesn't recognize work like they should — or use your
phone as one.**

Some USB/Bluetooth gamepads are perfectly valid HID devices, but their report descriptors
aren't on macOS's recognized list — so games ignore them. PadLink reads the controller
directly and re-presents it to the OS, the way Steam Input does, so your games finally see it.

No controller at all? **PadLink Remote** turns your phone into one over Wi-Fi — including a full
racing cockpit with a steering wheel, pedals, and a shifter.

> This is the **public community & downloads** hub for PadLink. Use it to **download the app**,
> **report bugs**, **request features**, and **request support for a new controller**. (The
> application source code is not hosted here.)

---

## ⬇️ Download

<p align="center">
  <img alt="Available soon" src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&duration=2500&pause=700&color=3FB950&center=true&vCenter=true&width=440&height=45&lines=Available+soon...;Coming+soon+to+macOS;Windows+in+final+testing">
</p>

> ⏳ **Available soon** — PadLink is getting ready for its first public release. The download link will appear here when it's ready.

- 🖥️ **macOS** — coming soon (Apple Silicon + Intel, notarized by Apple)
- 💻 **Windows** — built and in final testing (Windows 10/11 — one installer for both Intel/AMD and ARM)

<details>
<summary>💡 <b>Windows may say the installer "isn't commonly downloaded" — here's why, and what to click</b></summary>

<br>

PadLink is new, and Windows hasn't seen enough downloads yet to have built a reputation for it.
That's all this warning means. It is **not** a virus alert — it's a "we haven't met this file
before" notice that every small app gets until enough people have installed it.

To continue past it:

- **Edge** — click the **⋯** next to the download → **Keep** → **Keep anyway**
- **Chrome** — click the **▾** next to the download → **Keep**
- If a blue **"Windows protected your PC"** screen appears when you run the installer, click
  **More info** → **Run anyway**

Want to check the file yourself? GitHub publishes a **SHA256** for every release asset; compare it
with `Get-FileHash .\PadLink-win-Setup.exe` after downloading.

</details>

_⭐ Star or watch this repo to know the moment it drops._

---

## What it does

PadLink takes your input — a physical controller, or your phone via **PadLink Remote** — and
routes it through one of two output modes:

- **Keyboard & Mouse mode** — maps controller buttons/sticks to keystrokes and mouse movement.
  Works with any game or app. On macOS it needs only the Accessibility permission — no driver.
- **Gamepad mode** — presents a standard virtual controller to the OS so games see a real
  gamepad (with full stick/trigger support and on-screen glyphs).

Each connected controller is configured independently — its own mode, its own mapping profile,
its own name — and PadLink remembers it across reconnects.

> **On Windows**, PadLink is **phone-driven**: PadLink Remote is the input source, presented to
> games as a real virtual gamepad or as keyboard/mouse. Windows already recognizes most USB pads
> natively, so it doesn't need the physical-controller rescue that macOS does.

The **free tier** covers the essentials — **1 controller** at a time, both output modes, all
mapping profiles, and the PadLink Remote touch gamepad (ad-supported). **PadLink Pro** raises that
to **4 controllers** at once and adds the **Car Driving** cockpit and an ad-free PadLink Remote.

**Want to try Pro first?** There's an opt-in **7-day free trial** you start from inside the app —
no card, no sign-up. It unlocks **everything Pro does, including the Car Driving cockpit and the
ad-free remote**; only the controller count is lower (**2** during the trial, vs 4 on Pro). See the
in-app About / Plan screen for details.

---

## 📸 Screenshots

### macOS app

<p align="center">
  <img src="assets/screenshots/macOS_RemotePairing.png" width="400" alt="Remote pairing on macOS">
  &nbsp;
  <img src="assets/screenshots/macOS_InputMonitor.png" width="400" alt="Input monitor on macOS">
</p>

### PadLink Remote (iOS)

<p align="center">
  <img src="assets/screenshots/iOS_GamePad.PNG" width="400" alt="Gamepad layout">
  &nbsp;
  <img src="assets/screenshots/iOS_CarDriving.PNG" width="400" alt="Car Driving layout">
</p>

---

## 📱 PadLink Remote — use your phone as a controller

No physical gamepad? **PadLink Remote** (iOS) turns your phone into a wireless controller. It
shows an on-screen touch gamepad — two sticks, an 8-way D-pad, face buttons, shoulders, and
travel-based triggers, plus a touchpad mouse mode — and sends your input to the Mac over your
local network, where it drives the exact same output as a physical pad (gamepad **or**
keyboard/mouse mode).

- **Multiple layouts** — a standard **gamepad** layout, plus a **Car Driving** cockpit for racing
  games: a rotating steering wheel (or optional tilt/motion steering), gas and brake pedals, a
  sequential gear shifter, and a handbrake. Switch to the surface that fits what you're playing.
  _(The gamepad layout is free. The Car Driving cockpit needs **Pro** — or the **7-day free
  trial**, which includes it.)_
- **Switch surfaces mid-game** — hold one button to flip between the gamepad and the cockpit, so
  you have a familiar pad for the menus a game drops you into between races.
- **Driving button profiles** — the cockpit's buttons aren't fixed. Pick a control-style preset or
  build your own, and every control shows the button it actually sends, labelled the way your game
  uses it (DRIFT, NITRO, …) instead of a caption that lies.
- **Pair in seconds** — scan a QR code or enter the host's IP; reconnect to known hosts with one tap.
- **Feels real** — haptic vibration (including live trigger rumble) and optional click sounds.
- **Make it yours** — drag, resize, and restyle the on-screen controls with the built-in layout editor.
- **Stays awake** — keeps the phone screen on while you play.

Get **PadLink Remote**, open PadLink on your computer, and pair. _(iOS available now; the Android
version is built and in final testing.)_

---

## 🎮 Supported controllers

| Controller | USB VID:PID | Status |
|------------|-------------|--------|
| SHANWAN "Android Gamepad" | `0x2563:0x0526` | ✅ Supported |
| "PS3/PC Gamepad" clone | `0x2563:0x0575` | ✅ Supported |

_This list is for **macOS**, where PadLink reads the pad directly. On Windows, controllers are
handled by the OS — PadLink Remote (your phone) is the input source there._

**Don't see your controller?** PadLink can likely support it — open a
**[New Controller Support request](https://github.com/nimets-dev/PadLink-Community/issues/new?template=controller_support.yml)**
and include the details the form asks for (we use them to add a decode profile for your pad).

---

## 🗺️ Roadmap

### ✅ Built & working
- 🖥️ macOS menu-bar app & dashboard
- ⌨️ Keyboard & Mouse mode
- 🎮 Up to 4 controllers at once, each with its own mode and reusable mapping profiles
- 📱 PadLink Remote (iOS) — Gamepad & Car Driving layouts
- 🏎️ Driving button profiles — switchable button maps + honest control labels for the cockpit
- 🔀 Fast surface switch — flip Gamepad ⇄ Car Driving without leaving the game
- 📳 Haptics & trigger rumble
- ✏️ Drag-to-edit layout editor & QR / IP pairing
- 🔐 Connection approval — approve, deny, or block any phone that asks to connect
- 🔔 Connect notifications & 🚀 launch at login
- 💎 PadLink Pro

### 🔜 In testing — next out the door
- 💻 **Windows app** — feature-complete (virtual Xbox 360 pad, keyboard/mouse, tray app,
  light/dark themes, one-click driver install). Finishing hardware testing and code signing.
- 🤖 **PadLink Remote for Android** — built at feature parity with iOS and running on real
  devices. Finishing the on-device polish pass.
- 🕹️ **Virtual Gamepad mode on macOS** — code complete; waiting on Apple's driver entitlement approval.
- 🔄 **Automatic updates** — wired on both platforms, ships with the first public release.

### 🔭 Planned / future
- ➕ More controllers
- ✈️ More Remote layouts & skins (incl. an **Airplane** type)
- 🎨 Purchasable wheel & controller skins
- 📡 Zero-config pairing (no IP or QR needed)
- 🌍 Play over the internet, not just your local network

> Timelines aren't promises. Want something prioritized?
> [Request a feature](https://github.com/nimets-dev/PadLink-Community/issues/new?template=feature_request.yml)
> or join the [Discussions](https://github.com/nimets-dev/PadLink-Community/discussions).

---

## 💬 Community & support

- **🐛 Found a bug?** → [Open a bug report](https://github.com/nimets-dev/PadLink-Community/issues/new?template=bug_report.yml)
- **💡 Want a feature?** → [Request a feature](https://github.com/nimets-dev/PadLink-Community/issues/new?template=feature_request.yml)
- **🎮 New controller?** → [Request controller support](https://github.com/nimets-dev/PadLink-Community/issues/new?template=controller_support.yml)
- **❓ Questions & ideas?** → [Discussions](https://github.com/nimets-dev/PadLink-Community/discussions)

Faster, direct help:

- **Telegram:** [@nimets_support](https://t.me/nimets_support)
- **Email:** [support@nimets.com](mailto:support@nimets.com)
- **Website:** [padlink.nimets.com](https://padlink.nimets.com)

---

## License

PadLink is proprietary software. See [EULA.md](EULA.md) for the end-user license agreement.
Content in this repository (issue templates, docs) is provided for community use with PadLink.
