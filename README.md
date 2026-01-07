# Epstein's MAP

A plugin for Endstone that provides a public online map of the your Minecraft Bedrock Edition server world for the lastest version.

## 🌟 Features

- **Web Interface**: Interactive world map accessible through browser
- **Real-time Player Tracking**: Live player position display (can be turned off)
- **Multi-dimensional Support**: Overworld, The End
- **Automatic Scanning**: Periodic map updates
- **Static Linking**: No external dependencies required at runtime
- **High Performance**: Optimized rendering for large maps
- **Black Squares**: Like that ones in Epstein's files.

## 📋 Requirements

- **Endstone**: v0.10.x
- **Operating System**: Linux

## 🚀 Quick Start

### 1. Download the Plugin

Since this project is closed-source, download pre-built releases from the [Releases](https://github.com/foxey747/epsteinsmap/releases) page.

### 2. Installation

Copy the downloaded plugin to the Endstone plugins directory:
```bash
# Linux
cp epstein_map.so /path/to/endstone/plugins/
```

### 3. Configuration

Create the configuration file `plugins/EpsteinMAP/config.json`:

```json
{
  "web_port": 80,
  "show_players_on_map": true,
  "map_rescan_hours": 0
}
```

### 4. Launch

Start the Endstone server and open in your browser:
```
http://your-server-ip
```

## ⚙️ Configuration

File: `plugins/EpsteinMAP/config.json`

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `web_port` | number | 80 | Port for the web server |
| `show_players_on_map` | boolean | true | Show players on the map |
| `map_rescan_hours` | number | 0 | Automatic rescan interval (0 = disabled) |

## 🎮 Commands

### `/mapstatus`
Shows current plugin status
- **Permission**: `epsteinmap.command.status` (default: all players)
- **Usage**: `/mapstatus`

### `/mapscan [dimension]`
Starts scanning the specified dimension
- **Permission**: `epsteinmap.command.scan` (default: operators only)
- **Usage**: 
  - `/mapscan` - scan Overworld
  - `/mapscan Overworld` - scan the overworld
  - `/mapscan TheEnd` - scan the end


## 📚 Dependencies

### Requirements
- **Endstone Server**: v0.10.x
- **Operating System**: Linux
- **Permissions**: Read/write access to plugins directory
- **Network**: Port 80 (or configured port) must be available

## 📦 Releases

Since this is a closed-source project, pre-built binaries are provided in releases.

### Download from Releases
Visit the [Releases](https://github.com/your-org/epsteinsmap/releases) page to download:
- **Linux**: `epstein_map.so`

### Version Information
Each release includes:
- Pre-compiled plugin binary for your platform
- Release notes with new features and bug fixes
- Compatibility information with Endstone versions
- Changelog with detailed changes

### Support for Platforms
- ✅ Linux (x86_64)

### Update Instructions
To update to a new version:
1. Stop the Endstone server
2. Backup your current plugin (optional)
3. Download the latest release
4. Replace the plugin file in the plugins directory
5. Start the Endstone server
6. Check the console for any migration messages

## 🌐 Web Interface

After plugin startup, the web interface is available at:
```
http://your-server-ip
```

### Web Interface Features:
- **Map Viewing**: Pan and zoom functionality
- **Player Display**: Player icons with names
- **Chunk Information**: Coordinates and load status
- **Scan Status**: Progress of map updates
- **API Endpoints**: JSON data for integration

### API Endpoints

- `GET /map_data/{dimension}` - map data
- `GET /players` - player positions
- `GET /scan_status` - scanning status

## 🔒 Permissions

The plugin uses the following permissions:

| Permission | Default | Description |
|------------|---------|-------------|
| `epsteinmap.command.status` | True | View map status |
| `epsteinmap.command.scan` | Operator | Trigger map scan |

## 🐛 Troubleshooting

### Problem: Web interface not accessible

1. Check port configuration
2. Ensure port is not blocked by firewall
3. Check server logs for errors

### Problem: Map not scanning

1. Verify world path is found
2. Check file permissions for world data
3. Use `/mapstatus` command for diagnostics

### Problem: Players not showing

1. Check `show_players_on_map` setting in config

### Problem: Version compatibility

1. Check release notes for Endstone version compatibility
2. Download the appropriate plugin version for your server
3. Ensure you're using the correct binary for your platform

---

**EpsteinMAP** - MCPE 1.21.X!
