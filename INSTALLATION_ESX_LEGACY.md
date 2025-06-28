# ESX Legacy Installation Guide

## Prerequisites

- FiveM server with ESX Legacy installed
- Basic knowledge of FiveM server management

## Installation Steps

### 1. Download and Extract
- Download the `cd_easytime` resource
- Extract it to your server's `resources` folder

### 2. Server Configuration
Add the following line to your `server.cfg`:
```
ensure cd_easytime
```

### 3. ESX Legacy Permissions Setup

#### Option A: Using ESX Legacy's Built-in Permissions
1. Open your ESX Legacy admin panel
2. Go to the permissions section
3. Add the following permissions to your admin groups:
   - `superadmin`
   - `admin` 
   - `mod`
   - `user`

#### Option B: Using ACE Permissions
Add to your `server.cfg`:
```
add_ace group.admin command.easytime allow
add_ace group.moderator command.easytime allow
```

### 4. Configuration

#### Basic Configuration
Edit `configs/config.lua`:

```lua
Config.Framework = 'esx'  -- Keep this as 'esx'
Config.Language = 'EN'    -- Change to your preferred language

-- Update permissions for your server
Config.Command.Perms = {
    ['esx'] = {'superadmin', 'admin', 'mod'}, -- Adjust based on your permission groups
    -- ... other frameworks
}
```

#### Weather Configuration
Customize weather patterns:

```lua
Config.WeatherGroups = {
    [1] = {'CLEAR', 'OVERCAST','EXTRASUNNY', 'CLOUDS'}, -- Clear weather
    [2] = {'CLEARING', 'RAIN', 'NEUTRAL', 'THUNDER'},   -- Rain weather
    [3] = {'SMOG', 'FOGGY'},                            -- Foggy weather
    [4] = {'SNOWLIGHT', 'SNOW', 'BLIZZARD', 'XMAS'},   -- Snow weather
}
```

### 5. Restart Server
1. Stop your FiveM server
2. Start your FiveM server
3. Check console for any errors

## Testing

### 1. Check Console
Look for these messages in your server console:
```
[cd_easytime] - Saved settings applied.
[cd_easytime] - Settings Saved
```

### 2. Test Commands
1. Join your server as an admin
2. Type `/easytime` in chat
3. The UI should open if you have proper permissions

### 3. Test Weather Changes
1. Open the UI with `/easytime`
2. Change weather settings
3. Weather should change for all players

## Troubleshooting

### Common Issues

#### "Invalid permissions" error
- Check your ESX Legacy permissions setup
- Verify the permission groups in `configs/config.lua`
- Make sure your player has the correct permissions

#### Script not loading
- Check if `ensure cd_easytime` is in your `server.cfg`
- Verify all files are in the correct location
- Check server console for error messages

#### Weather not syncing
- Ensure all players have the resource downloaded
- Check if there are conflicting weather scripts
- Verify the resource is started after ESX Legacy

#### UI not opening
- Check if you have the required permissions
- Verify the command is `/easytime`
- Check browser console for JavaScript errors

### Debug Mode
To enable debug mode, add this to your `configs/config.lua`:
```lua
Config.Debug = true
```

## Support

If you encounter issues:
1. Check the troubleshooting section above
2. Look at your server console for error messages
3. Join our Discord: discord.gg/codesign
4. Provide error logs and your configuration

## Migration from Old ESX

If you're migrating from an older ESX version:

1. **Backup** your current `cd_easytime` folder
2. **Replace** with the new version
3. **Update** your permissions configuration
4. **Test** thoroughly before going live
5. **Remove** any old ESX-specific configurations

## Performance Notes

- The script is optimized for ESX Legacy
- Uses modern Lua 5.4 features
- Minimal performance impact
- Compatible with most other resources 