# 🔊 DownPlay

<p align="center">
  <img src="resources\ic_SoundFixer.png" alt="DownPlay icon" width="140" />
</p>

<p align="center">
  <a href="https://github.com/BLCK-N/DownPlay/upload">
    <img src="https://img.shields.io/badge/GitHub-DownPlay-181717?logo=github&logoColor=white" alt="GitHub Repo" />
  </a>
  <a href="https://github.com/BLCK-N/DownPlay/upload/stargazers">
    <img src="https://img.shields.io/github/stars/BLCK-N/DownPlay?style=social" alt="GitHub stars" />
  </a>
</p>

## Fix Linux audio issues in seconds

**DownPlay by /＠**

DownPlay is a fast, lightweight Linux audio repair tool built to restore sound in virtual machines, minimal Linux environments, and broken desktop setups. It automates the setup of PipeWire, disables conflicting audio services, and fixes common sound issues without manual system configuration.

Whether you are dealing with no audio, echo, crackling, or misconfigured sound settings, DownPlay gives you a clean and reliable way to recover audio quickly.

## Why this project exists

Linux virtual machines often come with broken or incomplete audio configuration. DownPlay solves that by handling the setup automatically so you can focus on using your system instead of debugging sound settings.

## Features

- Installs and configures PipeWire as the default audio server
- Installs required audio libraries and `pavucontrol`
- Disables PulseAudio to prevent conflicts
- Starts and enables the correct PipeWire services (`pipewire`, `pipewire-pulse`, `wireplumber`)
- Shows colored terminal output and progress feedback
- Saves logs to `~/SoundFixer.log` for debugging

## Requirements

- Debian/Ubuntu-based Linux distribution
- `sudo` access
- A terminal emulator

## Quick start

```bash
wget https://raw.githubusercontent.com/BLCK-N/DownPlay/upload/main/main/src/SoundFixer-by-0v1.sh
chmod +x SoundFixer-by-0v1.sh
./SoundFixer-by-0v1.sh
```

## Installation

### Package installation

#### Debian/Ubuntu (.deb)
```bash
wget https://github.com/BLCK-N/DownPlay/upload/releases/soundfixer.deb
sudo apt install ./soundfixer.deb
soundfixer
```

#### RPM-based systems (Fedora/RHEL/openSUSE)
```bash
wget https://github.com/BLCK-N/DownPlay/upload/releases/soundfixer-1.0-2.noarch.rpm
sudo dnf install ./soundfixer-1.0-2.noarch.rpm
soundfixer
```

#### Generic Linux (.tgz)
```bash
wget https://github.com/BLCK-N/DownPlay/upload/releases/soundfixer-1.0.tgz
tar xzf soundfixer-1.0.tgz
sudo cp -r usr/ /usr/
/usr/bin/soundfixer
```

### Run directly without installation
```bash
wget https://raw.githubusercontent.com/BLCK-N/DownPlay/upload/main/main/src/SoundFixer-by-0v1.sh
chmod +x SoundFixer-by-0v1.sh
./SoundFixer-by-0v1.sh
```

### Source installation

#### Method 1: Clone and run
```bash
mkdir -p ~/.local/bin/linux-soundfixer \
  && cd ~/.local/bin/linux-soundfixer \
&& curl -sLO https://raw.githubusercontent.com/BLCK-N/DownPlay/upload/main/main/src/SoundFixer-by-0v1.sh \
  && chmod +x SoundFixer-by-0v1.sh \
  && ./SoundFixer-by-0v1.sh
```

#### Method 2: One-line install to ~/.local/bin
```bash
git clone https://github.com/BLCK-N/DownPlay.git
cd DownPlay/main/src/
chmod +x SoundFixer-by-0v1.sh
./SoundFixer-by-0v1.sh
```

> After installation, you can run DownPlay from anywhere:
>
> ```bash
> ~/.local/bin/linux-soundfixer/SoundFixer-by-0v1.sh
> ```
>
> Or add `~/.local/bin/linux-soundfixer` to your `PATH`:
>
> ```bash
> echo 'export PATH="$HOME/.local/bin/linux-soundfixer:$PATH"' >> ~/.bashrc
> source ~/.bashrc
> ```

## Usage

### Interactive mode
```bash
~/.local/bin/linux-soundfixer/SoundFixer-by-0v1.sh
```

### Automated mode (no TTY)
```bash
bash ~/.local/bin/linux-soundfixer/SoundFixer-by-0v1.sh
```

In non-TTY environments, the script runs quietly and writes output to `~/SoundFixer.log`.

## Logging and troubleshooting

All command output is stored in:

```bash
~/SoundFixer.log
```

If something fails, the log file stays available for troubleshooting and debugging.

## Customization

- Modify the log file path in the `LOGFILE` variable
- Edit the package list in `install_audio_fix()`
- Toggle the GitHub prompt by changing `SHOW_GITHUB`

## Contributing

Contributions are welcome. If you want to improve the project, fork the repository, create a feature branch, commit your work, and open a pull request.

## Project status

This project is ready for publication and optimized for quick setup, clean audio restoration, and reliable use in Linux VM environments.

## License

This project is licensed under the [MIT License](https://github.com/BLCK-N/DownPlay/blob/main/LICENCE).

---

*DownPlay by /＠*
