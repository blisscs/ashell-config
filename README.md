# Ashell Configuration

This project provides centralized ashell configuration files that users can symlink to their local ashell configuration directory.

**Ashell** is a ready-to-go Wayland status bar for Hyprland. For more information about ashell, visit: https://github.com/MalpenZibo/ashell

## Setup

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd ashell-config
   ```

2. Find your ashell configuration directory (usually `~/.config/ashell/`)

3. Create symlinks to the configuration file:
   ```bash
   # Link to the default ashell configuration file
   ln -s /path/to/ashell-config/configs/config.toml ~/.config/ashell/config.toml
   ```

## Configuration Structure

- `configs/` - Ashell configuration files
  - `config.toml` - Default ashell configuration file with minimal widget setup

### Default Configuration (config.toml)

The default configuration implements a minimal but functional status bar with:

**Layout:**
- **Left**: Workspaces widget - shows active and available workspaces
- **Center**: Window Title widget - displays focused window title
- **Right**: Keyboard Language, Clock, and System Tray widgets

**Features:**
- Clean, minimal appearance with transparent background
- Positioned at the top of the screen
- Displays on all monitors
- Theme-friendly neutral colors
- Proper widget spacing and alignment
- 24-hour clock format
- Truncated window titles to prevent overflow

## Usage

After setting up the symlinks, restart ashell to load the new configurations. Ashell watches the configuration file for changes and will apply updates immediately, so you can tweak the configuration while Ashell is running.

## Configuration Options

The main configuration file (`config.toml`) contains:

- **Log Level**: Control verbosity of logs
- **Outputs**: Configure which monitor(s) display the status bar
- **Position**: Set bar position (Top/Bottom)
- **Modules**: Configure left, center, and right modules
- **Appearance**: Customize colors, style, and themes
- **Settings**: Configure various module-specific settings

## Contributing

1. Add new configuration files to the `configs/` directory
2. Update this README with setup instructions for new configurations
3. Ensure all configurations follow ashell TOML format standards
4. Test configurations before committing