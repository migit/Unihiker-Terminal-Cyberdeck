# UNIHIKER Terminal-Cyberdeck
### A Portable SSH Terminal & Mini Control Station
![Release](https://img.shields.io/github/v/release/migit/Unihiker-Terminal-Cyberdeck)
![License](https://img.shields.io/github/license/migit/Unihiker-Terminal-Cyberdeck)
![Last Commit](https://img.shields.io/github/last-commit/migit/Unihiker-Terminal-Cyberdeck)
![Repo Size](https://img.shields.io/github/repo-size/migit/Unihiker-Terminal-Cyberdeck)
![Code Size](https://img.shields.io/github/languages/code-size/migit/Unihiker-Terminal-Cyberdeck)


A compact cyberdeck-style terminal built on the UniHiker M10.

This project transforms the board into a fast, minimal Linux device that boots directly into a custom terminal and acts as a portable SSH control station for more powerful systems.

## 🎥 Preview

[![Unihiker Terminal Cyberdeck Demo](https://img.youtube.com/vi/Gawl7apVdLo/0.jpg)](https://www.youtube.com/watch?v=Gawl7apVdLo&t=105s)
<img width="1022" height="1236" alt="U-cyberdeck" src="https://github.com/user-attachments/assets/e61228b2-7f7a-4e56-ab26-4189f910fe51" />
## Features

- Fast terminal boot (no GUI overhead)
- GUI toggle (switch between CLI and desktop)
- SSH control station (remote system management)
- Custom terminal themes (local vs SSH optimized)
- Live dashboard (tmux-based monitoring)

## Why?

The UniHiker is not powerful enough to run heavy frameworks like ROS efficiently.

Instead of forcing it into a role it cannot handle, this project reimagines the device as a dedicated interface a lightweight terminal designed to control more powerful machines remotely.

## How It Works

- The system boots into a lightweight terminal environment
- Custom `.bashrc` handles UI and behavior
- Local terminal uses framebuffer colors (`setterm`)
- SSH sessions use ANSI color reset
- Tools like `tmux` create a multi-pane dashboard

##  Setup

```bash
sudo apt update
sudo apt install tmux htop bmon

```

Clone repo:
```bash
git clone https://github.com/migit/Unihiker-Terminal-Cyberdeck.git
cd unihiker-cyberdeck
```

Run setup:
```bash
sudo chmod +x scripts/a2r3
./scripts/a2r3
```

Toggle GUI:
```bash
gui-toggle
```

Launch dashboard:
```bash
deck_dashboard
```

##  Hardware & Case

This project includes a custom 3D-printed case designed for:
- Secure mounting of the UniHiker board
- Easy access to ports
- Improved ergonomics for handheld use

Download the STL files from [here](https://www.thingiverse.com/thing:7331105)

## Use Cases

- Portable SSH terminal
- Remote server management
- Embedded system debugging  
- Network diagnostics tool
- Robot control interface (I have used it to control my mobile robot [a2r3](https://github.com/migit/AI-Autonomous-Room-Rover-Robot-A2R3), so do not be suprised if you encounter this shell script name)
- Field deployment terminal

## Future Improvements

- Custom boot animation
- Expanded dashboard features
- 3D printed Sensor attachment modules (plug and play type)

## Disclaimer

This project is built on the UniHiker platform.
No proprietary firmware or OS images are redistributed.

## License
MIT License
