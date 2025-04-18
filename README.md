# My Development Environment Configuration

This repository contains my personal configuration files for various development tools that I use daily to create a powerful and efficient development workflow. Below is a detailed breakdown of each tool and its configuration.

## Table of Contents

- [Window Management](#window-management)
  - [Aerospace](#aerospace)
  - [Yabai (Previously Used)](#yabai-previously-used)
- [Terminal Emulators](#terminal-emulators)
  - [Alacritty](#alacritty)
  - [WezTerm](#wezterm)
- [Text Editors](#text-editors)
  - [Zed](#zed)
  - [Neovim](#neovim)
- [Keyboard Customization](#keyboard-customization)
  - [Karabiner-Elements](#karabiner-elements)

## Window Management

### Aerospace

Aerospace is my current window tiling manager for macOS, which I migrated to from Yabai.

**Key Features in My Configuration:**

- **Window Gaps**: 18px gaps between windows and monitor edges for better visual separation
- **Key Bindings**: QWERTY preset with custom keybindings for efficient window management
- **Mouse Behavior**: Mouse follows focus when changing monitors or windows
- **Layout Management**:
  - `alt-slash`: Toggle between horizontal and vertical tiling layouts
  - `alt-comma`: Toggle accordion layout
- **Window Navigation**:
  - `alt-h/j/k/l`: Navigate between windows (vim-style)
  - `alt-shift-h/j/k/l`: Move windows in different directions
- **Workspace Management**:
  - `alt-1/2/3/4/5`: Switch to specific workspaces

**Configuration File**: [aerospace.toml](/aerospace/aerospace.toml)

### Yabai (Previously Used)

Yabai was my previous window manager before switching to Aerospace.

**Key Features in My Configuration:**

- **Layout**: Binary space partitioning (BSP) as default layout
- **Window Placement**: New windows spawn to the right for vertical splits or bottom for horizontal splits
- **Padding**: 12px padding on all sides
- **Mouse Integration**:
  - Mouse follows focus
  - Alt modifier for dragging and resizing windows
  - Window swapping when dropping in center of another window
- **App Exclusions**: System Settings, Calculator, Karabiner-Elements, and QuickTime Player are excluded from management

**Configuration File**: [yabairc](/yabai/yabairc)

## Terminal Emulators

### Alacritty

Alacritty is a GPU-accelerated terminal emulator that I use for its speed and simplicity.

**Key Features in My Configuration:**

- **Appearance**:
  - 70% opacity with background blur for a modern look
  - 10px padding on all sides
  - Buttonless window decoration
- **Font**: MesloLGS Nerd Font Mono at 14pt size
- **Theme**: Custom "coolnight" theme
- **Terminal Compatibility**: Configured with xterm-256color for broad compatibility

**Configuration File**: [alacritty.toml](/alacritty/alacritty.toml)

### WezTerm

WezTerm is my alternative terminal emulator with more advanced features.

**Key Features in My Configuration:**

- **Appearance**:
  - 80% opacity with 10px background blur
  - Hidden tab bar for a cleaner interface
  - Resize-only window decorations
- **Font**: MesloLGS Nerd Font Mono at 14pt size
- **Custom Color Scheme**: Personal "coolnight" theme with:
  - Dark blue background (#011423)
  - Light blue foreground (#CBE0F0)
  - Bright green cursor (#47FF9C)
  - Custom ANSI colors for syntax highlighting

**Configuration File**: [.wezterm.lua](/wezterm/.wezterm.lua)

## Text Editors

### Zed

Zed is a modern, high-performance code editor that I use for quick edits and certain projects.

**Key Features in My Configuration:**

- **Custom Keybindings**:
  - Double-tap Shift to toggle file finder
  - `k j` in insert mode to switch to normal mode (Vim-style escape)
  - Restored standard keyboard shortcuts (Ctrl+C, Ctrl+V, etc.) for better compatibility
  - Custom space leader key mappings for navigation in Vim mode
- **Vim Emulation**: Configured with custom Vim-style keybindings while preserving standard editor functionality

**Configuration Files**:
- [keymap.json](/zed/keymap.json)
- [settings.json](/zed/settings.json)

### Neovim

Neovim is my primary terminal-based editor for more intensive development work.

**Key Features in My Configuration:**

- **Modular Setup**: Configuration split into core settings and plugin management
- **Plugin Management**: Using lazy.nvim for efficient plugin loading
- **Custom Module**: Using a personal "josean" module for organization

**Configuration Files**:
- [init.lua](/nvim/init.lua)
- Additional configuration in the lua/josean directory

## Keyboard Customization

### Karabiner-Elements

Karabiner-Elements is a powerful keyboard customizer that I use to remap keys for improved productivity.

**Key Features in My Configuration:**

- **Hyper Key**: Caps Lock is remapped to act as Command+Control+Option+Shift (Hyper key)
  - This provides a powerful modifier for custom application shortcuts
  - Allows for a single key to trigger complex actions
- **Device-Specific Settings**: Certain keyboards are excluded from remapping

**Configuration Files**:
- [karabiner.json](/karabiner/karabiner.json)
- Automatic backups in the automatic_backups directory

## Usage

To use these configurations:

1. Clone this repository to your local machine
2. Create symbolic links from the appropriate locations to these configuration files
3. Restart the applications to apply the new configurations

For example, to use the Alacritty configuration:

```bash
ln -s /path/to/this/repo/alacritty/alacritty.toml ~/.config/alacritty/alacritty.toml
```

## Benefits of This Setup

- **Efficiency**: Keyboard-driven workflow reduces reliance on mouse/trackpad
- **Consistency**: Similar keybindings across different tools
- **Customization**: Tailored to my specific workflow needs
- **Aesthetics**: Consistent visual theme across applications
- **Productivity**: Reduced context switching with optimized window management

## Notes

These configurations are constantly evolving as I refine my workflow. Feel free to use them as inspiration for your own setup, but be aware that some configurations may be specific to my personal preferences and hardware.