# CD EasyTime - Weather & Time Management

**Updated for ESX Legacy Compatibility**

A comprehensive weather and time management system for FiveM servers with support for multiple frameworks.

## Features

- 🌤️ Dynamic weather system with customizable weather groups
- ⏰ Real-time clock synchronization
- 🌙 Day/night cycle management
- ⚡ Thunder and lightning effects
- ❄️ Snow weather support
- 🌊 Tsunami warning system for server restarts
- 🔧 Staff UI for weather/time control
- 🎮 Multi-framework support (ESX, QBCore, vRP)

## Framework Support

### ESX Legacy (Recommended)
This script has been fully updated for ESX Legacy compatibility:

- **Permissions System**: Updated to work with ESX Legacy's new permissions system
- **Framework Initialization**: Uses modern ESX export methods
- **Notification System**: Compatible with ESX Legacy notifications
- **Player Management**: Updated player data handling

### Other Frameworks
- QBCore
- vRP
- ACE Permissions
- Identifier-based permissions

## Installation

1. **Download** the resource
2. **Place** it in your server's resources folder
3. **Add** `ensure cd_easytime` to your server.cfg
4. **Configure** the permissions in `configs/config.lua`
5. **Restart** your server

## Configuration

### ESX Legacy Permissions
Update the permissions in `configs/config.lua`:

```lua
Config.Command.Perms = {
    ['esx'] = {'superadmin', 'admin', 'mod', 'user'}, -- ESX Legacy permissions
    -- ... other frameworks
}
```

### Weather Groups
Customize weather patterns in the config:

```lua
Config.WeatherGroups = {
    [1] = {'CLEAR', 'OVERCAST','EXTRASUNNY', 'CLOUDS'}, -- Clear weather
    [2] = {'CLEARING', 'RAIN', 'NEUTRAL', 'THUNDER'},   -- Rain weather
    [3] = {'SMOG', 'FOGGY'},                            -- Foggy weather
    [4] = {'SNOWLIGHT', 'SNOW', 'BLIZZARD', 'XMAS'},   -- Snow weather
}
```

## Commands

- `/easytime` - Open the staff UI (requires permissions)

## Permissions

The script uses ESX Legacy's permission system. Make sure your players have the appropriate permissions configured in your ESX setup.

## Dependencies

- ESX Legacy (for ESX framework)
- FiveM server

## Changelog

### Version 1.3.8 (ESX Legacy Update)
- ✅ Updated for ESX Legacy compatibility
- ✅ Modern framework initialization
- ✅ Updated permissions system
- ✅ Improved notification handling
- ✅ Better error handling
- ✅ Lua 5.4 optimizations

## Support

For support, visit our Discord: discord.gg/codesign

## License

This project is licensed under the terms specified in the LICENSE file.

![674x458](https://i.imgur.com/cHwhpau.png)

![674x458](https://i.imgur.com/PimVsrU.png)

![674x458](https://i.imgur.com/9kUB0Z7.png)

![](https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png)


Easytime is a small standalone but useful UI for FiveM server administrators which allows them to manipulate time and weather with a click of a button!


## Full documentation

https://docs.codesign.pro/free-scripts/easytime-time-and-weather-management

## How do I use?

The default command to open the UI is /easytime. Make sure to configure the Config.Framework.

## Conflicts

It is possible that Easytime conflicts with other time and weather scripts such as vMenu or vSync.

## Preview

https://www.youtube.com/watch?v=-7SMZLyZWcY
