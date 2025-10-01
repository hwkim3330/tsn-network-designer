# TSN Network Designer

Interactive 3D/2D network topology designer for Time-Sensitive Networking (TSN) with support for Microchip LAN9662 and LAN9692 Ethernet switches.

![TSN Network Designer](https://img.shields.io/badge/TSN-Network_Designer-0066FF?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Web-orange?style=for-the-badge)

## 🚀 Live Demo

**[Launch 3D Designer](https://hwkim3330.github.io/tsn-network-designer/)**

- [3D Version (Default)](https://hwkim3330.github.io/tsn-network-designer/) - Interactive 3D visualization with Three.js
- [2D Version](https://hwkim3330.github.io/tsn-network-designer/tsn-designer-2d.html) - Graph-based 2D topology with Cytoscape.js
- [Automotive Version](https://hwkim3330.github.io/tsn-network-designer/tsn-automotive-designer.html) - Specialized for automotive TSN applications

## 🎯 Features

### 3D Interactive Visualization
- **Real-time 3D rendering** with Three.js and WebGL
- **Drag-and-drop** device placement
- **Orbit controls** for camera manipulation (rotate, zoom, pan)
- **Physical port representation** with accurate connector types:
  - MateNET: Blue industrial Ethernet connectors (100BASE-T1 / 1000BASE-T1)
  - SFP: Gray fiber optic slots
  - SFP+: Gold 10G fiber optic slots
  - MGMT: Orange management RJ45 port

### Supported Devices

#### LAN9662 TSN Switch
- **7× MateNET ports** (100BASE-T1 / 1000BASE-T1 industrial Ethernet)
- **4× SFP ports** (1G fiber optic)
- **1× Management RJ45** port
- **Total: 12 ports**
- TSN Features: IEEE 802.1Qbv (TAS), Qav (CBS), Qbu (Frame Preemption), IEEE 1588 PTPv2

#### LAN9692 TSN Switch
- **7× MateNET T1 ports** (100BASE-T1 / 1000BASE-T1)
- **4× SFP+ ports** (1G/10G fiber optic)
- **1× Management RJ45** port
- **Total: 12 ports**
- Enhanced 10G support for high-bandwidth applications

#### Automotive Endpoints
- **Camera**: 100BASE-T1, ~100 Mbps, VLAN Priority 6
- **LiDAR**: 1000BASE-T1, ~500-1000 Mbps, VLAN Priority 7
- **Radar**: 100BASE-T1, ~50-100 Mbps, VLAN Priority 5
- **ECU**: Configurable bandwidth and priority

### TSN Capabilities
- **IEEE 802.1Qbv** - Time-Aware Shaper (TAS)
- **IEEE 802.1Qav** - Credit-Based Shaper (CBS)
- **IEEE 802.1Qbu** - Frame Preemption
- **IEEE 1588** - Precision Time Protocol v2
- **IEEE 802.1CB** - Frame Replication and Elimination for Reliability (FRER)

### Network Configuration
- Interactive connection mode
- VLAN configuration with priority mapping
- Bandwidth allocation visualization
- Port status and statistics
- Export/Import network topology (JSON)

## 🛠️ Technology Stack

- **3D Rendering**: Three.js r128
- **2D Graphs**: Cytoscape.js
- **WebGL**: Hardware-accelerated graphics
- **Pure JavaScript**: No build tools required
- **Responsive Design**: Works on desktop and tablet devices

## 📖 Usage

### Adding Devices
1. Click device buttons in the left toolbar (LAN9662, LAN9692, Camera, LiDAR, etc.)
2. Device appears at the center of the canvas
3. Drag devices to position them in your network topology

### Creating Connections
1. Click the "Connect" button to enter connection mode
2. Click on a port of the first device
3. Click on a port of the second device
4. Connection line is created automatically

### Camera Controls (3D Version)
- **Left Click + Drag**: Rotate view
- **Right Click + Drag**: Pan view
- **Scroll Wheel**: Zoom in/out
- **Double Click**: Focus on device

### Exporting Configuration
1. Click "Export" button in the header
2. JSON file downloads with complete network topology
3. Includes all devices, connections, and configurations

## 🎨 Port Color Coding

| Port Type | Color | Description |
|-----------|-------|-------------|
| MateNET | 🔵 Blue | Industrial Ethernet T1 connectors |
| SFP | ⚫ Gray | 1G fiber optic modules |
| SFP+ | 🟡 Gold | 10G fiber optic modules |
| MGMT | 🟠 Orange | Management RJ45 port |

## 🔧 Local Development

No build process required! Simply open the HTML files in a modern web browser:

```bash
# Clone repository
git clone https://github.com/hwkim3330/tsn-network-designer.git
cd tsn-network-designer

# Open in browser
firefox index.html
# or
chromium index.html
```

### Requirements
- Modern web browser with WebGL support (Chrome, Firefox, Edge, Safari)
- JavaScript enabled
- Recommended: 1920×1080 or higher resolution

## 📦 File Structure

```
tsn-network-designer/
├── index.html                      # 3D Designer (main entry point)
├── tsn-designer-2d.html           # 2D Graph Designer
├── tsn-automotive-designer.html   # Automotive TSN Designer
└── README.md                       # This file
```

## 🌐 GitHub Pages Deployment

This project is configured for GitHub Pages hosting:

1. Push changes to `main` branch
2. GitHub Actions automatically deploys to `gh-pages`
3. Access at: `https://hwkim3330.github.io/tsn-network-designer/`

## 📚 Related Projects

- [Microchip LAN9662 EVB](https://www.microchip.com/en-us/development-tool/ev09d37a)
- [VelocityDRIVE CT Platform](https://www.microchip.com/en-us/solutions/industrial-automation/factory-automation/time-sensitive-networking)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for:
- Bug fixes
- New device types
- Enhanced visualizations
- Performance improvements
- Documentation updates

## 📄 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

- Microchip Technology for LAN9662/LAN9692 hardware
- Three.js community for excellent 3D rendering library
- Cytoscape.js team for powerful graph visualization

## 📞 Contact

For questions or support, please open an issue on GitHub.

---

**Built with ❤️ for TSN Network Design**