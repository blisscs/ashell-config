# User Story: Add Minimal Recommended Widgets and Keyboard Language Display

## Story ID: US-001

## Title
Add minimal recommended widgets and keyboard language display to ashell configuration

## As a
Hyprland user using ashell

## I want
To have a minimal set of essential widgets displayed on my status bar, including keyboard language indicator and system controls

## So that
I can see important system information at a glance, easily identify my current keyboard layout, and access system controls

## Acceptance Criteria

### Functional Requirements
1. **Workspaces Widget**: Display Hyprland workspaces on the left side of the bar
2. **Clock Widget**: Display current date and time on the right side
3. **Keyboard Language Widget**: Show current keyboard layout/language on the right side
4. **System Info Widget**: Display CPU and memory usage on the right side
5. **Privacy Widget**: Provide microphone and camera privacy controls on the right side
6. **Settings Widget**: Provide access to system settings and power management on the right side

### Configuration Requirements
1. Use solid background style with theme-matching colors
2. Position bar at the top of the screen
3. Display on all monitors
4. Use full-width bar appearance
5. Ensure widgets are properly spaced and aligned

### Technical Requirements
1. Configuration should be valid TOML format
2. Follow ashell configuration structure
3. Include necessary module configurations for each widget
4. Ensure all required dependencies are documented

### User Experience Requirements
1. Widgets should be responsive and update in real-time
2. Layout should be clean and not cluttered
3. Information should be easily readable
4. Keyboard language should be clearly visible but not intrusive

## Implementation Notes

### Recommended Modules
- `Workspaces` - For Hyprland workspace management
- `Clock` - For date/time display
- `KeyboardLayout` - For keyboard language/layout display
- `SystemInfo` - For CPU and memory usage monitoring
- `Privacy` - For microphone and camera privacy controls
- `Settings` - For system settings and power management access

### Actual Layout
```
Left: [Workspaces]
Right: [Clock, KeyboardLayout, SystemInfo, Privacy, Settings]
```

### Dependencies
- Hyprland (for workspaces)
- Keyboard layout detection
- System monitoring capabilities

## Definition of Done
- [x] All required widgets are configured and functional
- [x] Keyboard language display shows current layout correctly
- [x] Configuration follows ashell TOML format
- [x] README.md is updated with new configuration details
- [x] Configuration is tested and working
- [x] User can successfully symlink and use the configuration

## Additional Notes
- This configuration should serve as a good starting point for users
- Consider adding comments in the configuration file to explain each section
- Ensure the configuration is easily customizable for user preferences