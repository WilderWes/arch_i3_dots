# Arch i3wm Dotfiles

**Author:** Weston Preising

Arch i3 config for development and guitar practice/recording. Emphasis on vim-based applications when possible since vim is fun. A profound thank you to all open source contributors—thank you for making Linux accessible and enjoyable :).

## Main i3wm Setup

- [linux-zen](https://wiki.archlinux.org/title/Kernel) — zen kernel for improved desktop performance and responsiveness
- [AppArmor](https://wiki.archlinux.org/title/AppArmor) — mandatory access control (MAC) security framework
- [ufw](https://wiki.archlinux.org/title/Uncomplicated_Firewall) — uncomplicated firewall
- [NetworkManager](https://wiki.archlinux.org/title/NetworkManager) with nm-applet systray
- [ly](https://github.com/fairyglade/ly) — TUI display manager
- [Picom](https://github.com/yshui/picom) compositor with EGL backend
- [autorandr](https://github.com/phillipberndt/autorandr) — automatic display configuration based on connected hardware
  - profiles: `laptop` (HiDPI 162 DPI) and `docked` (96 DPI)
  - postswitch script restarts i3/apps on profile change
- [rofi](https://github.com/davatorium/rofi) — application launcher (`$mod+/`)
- [feh](https://feh.finalrewind.org/) — wallpaper setter
- [xss-lock](https://bitbucket.org/raymonad/xss-lock) + [i3lock](https://i3wm.org/i3lock/) — screen lock on suspend (`$mod+Escape`)
- [dunst](https://dunst-project.org/) — notification daemon
- [downgrade](https://aur.archlinux.org/packages/downgrade)
- [maim](https://github.com/naelstrof/maim) + [xclip](https://github.com/astrand/xclip) — screenshot to clipboard (`Print` key)
- [brightnessctl](https://github.com/Hummer12007/brightnessctl) — backlight control
- [pasystray](https://github.com/christophgysin/pasystray) — PulseAudio systray applet
- [lxqt-policykit](https://github.com/lxqt/lxqt-policykit) — policykit agent
- [dex-autostart](https://github.com/jceb/dex) — XDG autostart
- [1Password](https://1password.com/) — password manager desktop app (`$mod+p`)
- [dark theme reddit](<https://www.reddit.com/r/hyprland/comments/1h4abmt/how_do_i_apply_dark_theme/>)
  - [qt5ct](https://github.com/desktop-app/qt5ct) [qt6ct](https://github.com/trialuser02/qt6ct) [adw-gtk3-theme](https://github.com/lassekango83/adw-gtk3)
  - `sudo echo "QT_QPA_PLATFORMTHEME=qt6ct" >> /etc/environment`
  - copy my `gtk-*` files to ~/.config
- [libinput](https://wiki.archlinux.org/title/Libinput) — `40-libinput.conf`: caps lock → ctrl, flat pointer accel, tap-to-click, natural scrolling
- [fontconfig](https://wiki.archlinux.org/title/Font_configuration) + `.Xresources` — font rendering (hinting, antialiasing) and HiDPI DPI settings
- [cups/avahi-daemon/nss-mdns](https://wiki.archlinux.org/title/CUPS)
- [keyring/pam setup](https://wiki.archlinux.org/title/GNOME/Keyring)
- [snapper/btrfs-assistant](https://wiki.archlinux.org/title/Snapper)
- [redshift-gtk](https://wiki.archlinux.org/title/Redshift) — blue light filter (`redshift-gtk-git` from AUR)
- [tlp w/ tlp-pd](https://linrunner.de/tlp/index.html)

## Terminal & Shell

- [kitty](https://sw.kovidgoyal.net/kitty/) with [CommitMono](https://commitmono.com/) and Tokyo Night theme
  - Symbols Nerd Font Mono as nerd font fallback for icons
- [oh-my-zsh](https://ohmyz.sh/) with plugins:
  - [git](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git) (built-in)
  - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
  - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
  - [zsh-completions](https://github.com/zsh-users/zsh-completions)
  - [gradle-completion](https://github.com/gradle/gradle-completion)
  - [zsh-nvm](https://github.com/lukechilds/zsh-nvm) (lazy-loaded for faster startup)
- [starship](https://starship.rs/) prompt
- [eza](https://github.com/eza-community/eza) as ls replacement
- [fastfetch](https://github.com/fastfetch-cli/fastfetch) system info (runs on shell start)
- yazi `y()` shell wrapper — changes directory in the shell on exit

## Editor & File Management

- [Neovim](https://neovim.io/) via [LazyVim](https://www.lazyvim.org/) — notable extra plugins:
  - [vimtex](https://github.com/lervag/vimtex) — LaTeX editing (latexmk compiler, zathura PDF viewer)
  - [img-clip.nvim](https://github.com/HakonHarnes/img-clip.nvim) — paste images from clipboard into buffer
  - [presence.nvim](https://github.com/andweeb/presence.nvim) — Discord rich presence
  - [tokyonight.nvim](https://github.com/folke/tokyonight.nvim) — colorscheme (night style)
  - basedpyright as Python LSP
- [yazi](https://github.com/sxyazi/yazi) — terminal file manager
- [zathura](https://pwmt.org/projects/zathura/) with [zathura-pdf-poppler](https://pwmt.org/projects/zathura-pdf-poppler/) for PDF viewing (dark mode, clipboard selection)

## Browsers

- [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/)
  - [DarkReader](https://darkreader.org/)
  - [uBlock Origin](https://ublockorigin.com/)
  - [bypass-paywalls](https://gitflic.ru/project/magnolia1234/bypass-paywalls-firefox-clean)
  - [SponsorBlock](https://sponsor.ajay.app/)
  - [Unhook](https://unhook.app/)
  - [1Password](https://1password.com/downloads/browser-extension)
- [qutebrowser](https://qutebrowser.org/) — keyboard-driven browser, used strictly for [Markdown Preview](https://github.com/iamcco/markdown-preview.nvim)

## Communication

- [Discord](https://discord.com/)

## Development Setup and Tools

- [Docker](https://docs.docker.com/engine/)
  - [Post-Install (non-root setup)](https://docs.docker.com/engine/install/linux-postinstall/)
  - [Shell Autocompletion](https://docs.docker.com/compose/completion/)
- [Clang-Format Style Options](https://clang.llvm.org/docs/ClangFormatStyleOptions.html)
- [pandoc](https://pandoc.org/) — file converter
- [img2pdf](https://pypi.org/project/img2pdf/) — lossless image to PDF
- [cpdf](https://github.com/coherentgraphics/cpdf-binaries) — PDF manipulation CLI
- [tldr](https://github.com/tldr-pages/tldr) — quick cli tips n' tricks
- [zeal](https://zealdocs.org/) — offline coding reference docs
- [SDKMAN](https://sdkman.io/) for JDK management (Gradle)
- [w3m](https://w3m.sourceforge.net/) — text-based browser
- [pdftotext](https://poppler.freedesktop.org/) — PDF text extraction
- [bear](https://github.com/rizsotto/Bear) — reads compile commands from make and adds hints to clangd
- [esp-idf](https://github.com/espressif/esp-idf) toolchain (not currently in use, but planning ESP32 projects)
- [ripgrep-all](https://github.com/phiresky/ripgrep-all)

## Music Production / Guitar

- [Transcribe!](https://www.seventhstring.com/) — slow down audio, loop sections, transcribe by ear
- [yt-dlp](https://github.com/yt-dlp/yt-dlp) — download videos/audio from YouTube
- [DaVinci Resolve Studio](https://www.blackmagicdesign.com/products/davinciresolve) — video editing
- [OBS Studio](https://obsproject.com/) with [DroidCam](https://www.dev47apps.com/)
- [Bitwig Studio](https://www.bitwig.com/) (Flatpak)
- [Handbrake](https://handbrake.fr/) — video transcoding
- [VLC](https://www.videolan.org/vlc/)
- [LocalSend](https://localsend.org/) — cross-platform file sharing (Flatpak)

## AI Usage

- Claude occasionally used in a Socratic tutor capacity and to help debug code if I'm incredibly stuck
- Claude also used to help with README.md, and autorandr postswitch script specifically.
