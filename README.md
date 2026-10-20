 <div align="center">

# 💠 end4-pC

### A different feel for your Hyprland desktop.

A personal Quickshell customization built on [illogical-impulse](https://github.com/end-4/dots-hyprland).

**Made with care by Bryan.**

[Installation](#-installation) · [Screenshots](#-screenshots) · [Community presets](#-community-presets) · [FAQ](#-faq)

</div>

---

## 🎬 Showcase

<div align="center">

<a href="https://www.youtube.com/watch?v=o0Vsh7eVchs">
  <img src="https://img.youtube.com/vi/o0Vsh7eVchs/maxresdefault.jpg" alt="end4-pC desktop showcase" width="90%" />
</a>

*Watch the desktop experience in action.*

</div>

---

## ✨ About

**end4-pC** is a personal fork of the [illogical-impulse](https://github.com/end-4/dots-hyprland) Quickshell setup, customized by Bryan to give the Hyprland desktop its own look and feel.

The project focuses on a cohesive interface, useful desktop widgets, customizable appearance, and a straightforward way to interact with shell settings.

This is an ongoing project. Features, styling, and configuration may change as development continues.

> [!NOTE]
> end4-pC requires [illogical-impulse](https://github.com/end-4/dots-hyprland) to be installed and running.

## 🎨 Features

<table>
<tr>
<td width="50%" valign="top">

### 🌈 Visual customization

- Material-inspired design
- Custom colors and styling
- Configurable shell appearance
- Consistent interface elements

</td>
<td width="50%" valign="top">

### 🖥️ Desktop experience

- Desktop widgets
- Lyrics display
- Weather integration
- Configurable bar

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🌌 Personalization

- Online wallpaper browsing
- Shader transitions
- Customizable desktop elements
- Settings overlay

</td>
<td width="50%" valign="top">

### ⚙️ Hyprland workflow

- Quickshell integration
- Launcher-based settings search
- Configurable keybinds
- Separate `end4-pC` configuration

</td>
</tr>
</table>

*Features depend on the underlying configuration and installed dependencies.*

---

## 📸 Screenshots

<div align="center">

| Lyrics | Online wallpapers |
|:---:|:---:|
| ![Lyrics](screenshots/1.png) | ![Online wallpapers](screenshots/2.png) |

| Configurable bar | Desktop interface |
|:---:|:---:|
| ![Configurable bar](screenshots/3.png) | ![Desktop interface](screenshots/4.png) |

| Desktop widgets | Hyprland configuration |
|:---:|:---:|
| ![Desktop widgets](screenshots/5.png) | ![Hyprland configuration](screenshots/6.png) |

</div>

---

## 🎨 Community presets

Explore and share desktop configurations through [**end4-pCpresets**](https://github.com/pctrade/end4-pCpresets).

From the shell, open **Dashboard → Presets** to browse available presets.

- **Download** a preset to try it.
- **Install** a preset to use it in your configuration.
- **Upload** your own preset to share your desktop.
- **Remove from gallery** to remove a preset you previously shared.

Uploading may require the [GitHub CLI](https://cli.github.com) (`gh`) and GitHub authentication. A browser-based alternative is available if you skip the CLI setup.

---

## ⚡ Installation

### Requirements

- Hyprland
- [illogical-impulse](https://github.com/end-4/dots-hyprland)
- Quickshell
- Git

### 1. Clone the repository

```bash
mkdir -p ~/.config/quickshell
cd ~/.config/quickshell

git clone https://github.com/pctrade/end4-pC.git
```

### 2. Launch the shell

```bash
qs -c end4-pC
```

To run it in the background:

```bash
qs -c end4-pC > /tmp/end4-pC.log 2>&1 &
disown
```

If something goes wrong, check the log:

```bash
tail -n 100 /tmp/end4-pC.log
```

### 3. Set it as the default shell (optional)

Open:

```text
~/.config/hypr/hyprland/variables.lua
```

Find:

```lua
hl.env("qsConfig", "ii")
```

Change it to:

```lua
hl.env("qsConfig", "end4-pC")
```

Reload Hyprland:

```bash
hyprctl reload
```

### 4. Add a settings keybind (optional)

Add this to your Hyprland configuration:

```lua
hl.bind(
    "SUPER + escape",
    hl.dsp.global("quickshell:settingsToggle"),
    { description = "Toggle settings" }
)
```

Use `Super + Escape` to toggle the settings overlay. You can also press `Escape` to close it.

---

## ⌨️ Tips

**Find settings:** Open the launcher with `Super` and search for a keyword such as `wallpaper`, `bar`, or `blur`.

**View keybinds:** Open the launcher and type `<` to see the configured keybinds.

**Switch back to illogical-impulse:** Change the `qsConfig` value back to `"ii"` in `variables.lua`, then reload or restart the relevant shell components.

---

## ❓ FAQ

<details>
<summary><strong>Does end4-pC replace illogical-impulse?</strong></summary>

No. It is a personal fork that builds on the existing illogical-impulse setup.

</details>

<details>
<summary><strong>Will it overwrite my existing configuration?</strong></summary>

The repository uses its own directory, `~/.config/quickshell/end4-pC`. However, both configurations may share system dependencies and Hyprland settings, so back up important customizations before making changes.

</details>

<details>
<summary><strong>How do I troubleshoot startup problems?</strong></summary>

Run `qs -c end4-pC` directly in a terminal to inspect errors. If you launched it in the background, check `/tmp/end4-pC.log`.

</details>

<details>
<summary><strong>Is the project finished?</strong></summary>

No. end4-pC is an ongoing personal project, and features and styling may evolve over time.

</details>

---

## 🙏 Credits

- **[@end-4](https://github.com/end-4)** — For creating [dots-hyprland / illogical-impulse](https://github.com/end-4/dots-hyprland), the foundation of this project.
- **[@gh0stzk](https://github.com/gh0stzk)** — For the weather API integration.
- **[@StarS2112](https://github.com/StarS2112)** — For showcasing the fork.
- **[@simeulinuxkaliaiwr](https://github.com/simeulinuxkaliaiwr)** — For shader transitions.

---

<div align="center">

### Made with care by Bryan.

**end4-pC** · A personal project for the Hyprland desktop.

[Repository](https://github.com/pctrade/end4-pC) · [Original project](https://github.com/end-4/dots-hyprland)

</div>
