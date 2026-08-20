# Equalizer APO Download (v1.3) – Free Windows Audio Equalizer & VST Host

[Equalizer APO](https://equalizerapo.com/) is an open-source, system-wide parametric and graphical equalizer designed for Microsoft Windows operating systems. Developed by Jonas Thedering, the application operates as an Audio Processing Object (APO) filter directly integrated into the Windows Audio Session API (WASAPI) infrastructure. 

By running as an architectural audio infrastructure component rather than a standalone media player, https://equalizerapo.com/ enables real-time, low-latency audio processing, custom equalization curves, and VST plugin hosting across all active system output channels and input recording devices.

<img width="876" height="293" alt="image (6)" src="https://github.com/user-attachments/assets/a7483b2e-e48c-41c6-8e6e-97918a7f9581" />

---

## Technical Architecture & Core System Capabilities

Equalizer APO processes audio signals via custom configuration scripts (`.txt` files) interpreted dynamically by its engine. The software operates with near-zero latency, avoiding heavy CPU overhead.

* **Unlimited Filter Nodes:** Configure infinite parametric filters, graphic peak bands, high/low-pass filters, and shelving filters per channel without hardware processing limits.
* **Low-Latency Architecture:** Designed for real-time applications such as Twitch streaming, competitive gaming, and professional voice monitoring with virtually no audio delay.
* **VST Plugin Integration:** Native hosting support for 32-bit and 64-bit VST audio processing plugins (e.g., noise gates, compressors, and de-essers).
* **Multichannel Audio Support:** Full compatibility with mono, stereo, 5.1, 7.1, and custom surround sound spatial configurations.
* **Modular Configuration UI:** Flexible graphical user interface allowing users to isolate devices, link nested configuration files, and inspect live signal metrics.

---

## Technical Specifications & Installation Requirements

Equalizer APO installs directly into the Windows audio pipeline, requiring standard system privileges during setup.

| Parameter | System Requirement Details |
| :--- | :--- |
| **Supported Operating System** | Microsoft Windows 7, 8, 8.1, 10, and 11 |
| **Audio Architecture Integration** | Windows Audio Processing Object (APO) / WASAPI |
| **Resource Overhead** | Extremely low CPU footprint and minimal RAM usage |
| **Plugin Compatibility** | VST 2.x plugin architecture (32-bit / 64-bit) |
| **Primary Developer** | Jonas Thedering (Open-Source Distribution) |

---

## Installation & Setup Protocol

Setting up Equalizer APO requires mapping the filter engine to specific hardware endpoints on your machine.

1. **Installer Execution:** Download and launch the setup executable file on your host computer.
2. **Audio Endpoint Selection:** During the installation sequence, the Configurator window will open automatically. Manually check the specific playback (speakers, headphones) or recording (microphones) devices you want to control.
3. **System Reboot:** Restart your PC when prompted to allow Windows to register the system-level APO driver wrappers.

---

## Basic Configuration & Pre-Amplification Workflow

To set up a custom pre-amplification chain for your speakers or microphone, follow this step-by-step procedure:

1. **Launch Configuration Editor:** Navigate to your installation directory (typically `C:\Program Files\EqualizerAPO`) and launch `Editor.exe`.
2. **Clear Default Tabs:** On the main workspace, remove pre-populated configuration blocks to start with a fresh layout.
3. **Create Module File:**
   * Click the green **+** icon, navigate to **Control** $\rightarrow$ **Include**.
   * Click the folder icon, create a new text file (e.g., `Tutorial.txt`), and select it.
   * Click the green arrow icon to switch focus into the new module tab.
4. **Target Hardware Device:**
   * Click the green **+** icon, choose **Control** $\rightarrow$ **Device**.
   * Uncheck *Select all options* and choose your target hardware output (e.g., Speakers) or input device.
5. **Add Pre-Amplification Filter:**
   * Click the green **+** icon, navigate to **Basic Filters** $\rightarrow$ **Preamplification**.
   * Adjust the gain slider to increase or decrease system volume levels.
6. **Save & Activate:** Inspect signal behavior in the bottom **Analysis Panel**, select **File** $\rightarrow$ **Save**, and ensure the power button toggle icon is highlighted to activate the filter network.

<p align="center">
  <img src="https://github.com/user-attachments/assets/1fb199ad-d4e9-4f6e-a6ce-3c4f813fd1c7" alt="Screenshot 2026-08-20 001902-4x" width="120" height="112" />
</p>

---

## Troubleshooting Common Operational Issues

* **Filters Not Taking Effect:** Open the `Configurator.exe` utility in the installation folder, verify that your active playback/recording device is checked, select *Troubleshooting options*, and set the install mode to *Install as LFX/GFX* or *SFX/EFX*.
* **Audio Distortion or Clipping:** Check the bottom Analysis Panel in the Configuration Editor. If the signal peak exceeds 0 dB, decrease the Preamplification gain slider to maintain clean headroom.
* **Third-Party GUI Add-ons:** For an expanded graphical interface, users can optionally install community-developed interfaces such as Peace Equalizer or HeSuVi on top of the core engine.

---

## Developer Credits & Legal Notice

Sincere thanks to **Jonas Thedering** and the open-source community contributors who developed and maintain Equalizer APO. This repository serves as a technical configuration and usage document.
