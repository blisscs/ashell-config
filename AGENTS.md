# AGENTS.md

This document provides information for AI agents working on the ashell configuration project.

## Project Overview

This project hosts ashell configuration files that users can symlink to their default ashell configuration locations. Ashell is a ready-to-go Wayland status bar for Hyprland. The project provides a centralized way to manage and share ashell configurations.

**Ashell Repository**: https://github.com/MalpenZibo/ashell  
**Ashell Documentation**: https://malpenzibo.github.io/ashell/

## Project Structure

```
ashell-config/
├── README.md           # User documentation for setting up configurations
├── AGENTS.md           # This file - information for AI agents
└── configs/            # Configuration files directory
    └── config.toml     # Default ashell configuration file
```

## Configuration Format

Ashell uses TOML configuration files. The main configuration file is `config.toml` located at `~/.config/ashell/`. Key sections include:

- **Log Level**: Controls verbosity (debug, info, warn, error)
- **Outputs**: Monitor configuration (All, Active, or specific targets)
- **Position**: Bar position (Top/Bottom)
- **Modules**: Left, center, and right module configuration
- **Appearance**: Colors, style, and theme settings
- **Settings**: Module-specific configurations

## Common Tasks

### Adding New Configuration Files
- Place configuration files in the `configs/` directory
- Use `.toml` extension and follow TOML format
- Update README.md with instructions for the new configuration
- The main configuration file should be named `config.toml`

### Updating Documentation
- Keep README.md synchronized with any configuration changes
- Provide clear symlink instructions for users
- Include any dependencies or requirements
- Reference official ashell documentation when applicable

### Testing Configurations
- Test configurations work with ashell before committing
- Verify TOML syntax is valid
- Check for any conflicting settings
- Ensure all required sections are present

## Commands

### Setup and Validation
```bash
# Check if configurations are properly structured
find configs/ -name "*.toml" | sort

# Validate TOML syntax (if toml-cli is available)
toml lint configs/*.toml

# Check configuration file structure
grep -E "^\[|^log_level|^outputs|^position" configs/*.toml
```

### Documentation Updates
```bash
# Check README.md is up to date
grep -r "configs/" README.md

# Validate all TOML files have proper structure
for file in configs/*.toml; do
    echo "Checking $file..."
    toml-lint "$file" 2>/dev/null || echo "TOML validation failed for $file"
done
```

## Important Notes

- This project uses symlinks rather than copying files to maintain single source of truth
- Users should be instructed to create symlinks from `~/.config/ashell/config.toml` to files in this project
- Ashell watches the configuration file for changes and applies updates immediately
- Configuration files should be compatible with the latest ashell version
- Include example configurations for common use cases (minimal, full-featured, custom)
- Always reference the official ashell documentation for configuration options