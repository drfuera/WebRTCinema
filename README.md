![GitHub release](https://img.shields.io/github/v/release/drfuera/WebRTCinema)    ![GitHub downloads](https://img.shields.io/github/downloads/drfuera/WebRTCinema/total)    ![License](https://img.shields.io/badge/License-MIT-red)  

# WebRTCinema 🎬

**Synchronized P2P video streaming with smart buffering**

WebRTCinema is a browser-based peer-to-peer video streaming application that allows you to watch videos together in real-time without any servers. Stream video files directly between computers with synchronized playback, audio support, and smart buffering.

![WebRTCinema Interface](https://img.shields.io/badge/WebRTC-P2P%20Streaming-blue)

## ✨ Features

### 🎥 **Synchronized Video Streaming**
- Real-time synchronized playback between host and viewers
- Native video controls with automatic sync across all connected devices
- Support for seeking, play, and pause synchronization

### 🔊 **Audio Support**
- High-quality audio streaming alongside video
- Host-controlled audio toggle for bandwidth management
- Automatic audio track detection from video files

### ⚡ **Smart Buffering**
- Adjustable buffer delay (0-2000ms) for lag compensation
- Client-side buffering controls for optimal sync on different network conditions
- Real-time buffering status indicators

### 🖼️ **Adaptive Quality Control**
- Three quality presets: High, Medium, Low
- Dynamic resolution adjustment for bandwidth optimization
- Maintains aspect ratio across all quality settings

### 🌐 **True P2P Connection**
- Direct peer-to-peer streaming with no servers required
- Your data stays completely private - never touches external servers
- Uses STUN servers only for initial connection establishment

### 🔄 **Auto-Processing**
- Automatic processing of WebRTC connection data
- Simple copy-paste connection setup
- Real-time connection status indicators

## 🚀 Quick Start

### Prerequisites
- Modern web browser with WebRTC support (Chrome, Firefox, Safari, Edge)
- Local video files to stream

### Usage

1. **Download and Open**
   ```bash
   git clone https://github.com/drfuera/WebRTCinema.git
   cd WebRTCinema
   # Open WebRTCinema.html in your browser
   ```

2. **Host a Video Stream**
   - Choose "Host Video" on the main screen
   - Select a video file from your computer
   - Copy the generated offer data
   - Share the offer data with viewers

3. **Join as a Viewer**
   - Choose "View Video" on the main screen
   - Paste the host's offer data
   - Copy your generated answer data
   - Send the answer data back to the host

4. **Start Watching**
   - Once connected, use native video controls
   - Adjust buffer delay if experiencing sync issues
   - Change quality settings based on your connection

## 🎛️ Controls & Settings

### Host Controls
- **File Selection**: Choose any local video file
- **Audio Toggle**: Enable/disable audio streaming
- **Playback Controls**: Standard video controls that sync to all viewers

### Viewer Controls
- **Buffer Delay**: Adjust 0-2000ms buffer for sync optimization
- **Quality Settings**: High/Medium/Low quality presets
- **Sync Request**: Manual sync request button
- **Playback Controls**: Standard video controls that sync to host

## 🔧 Technical Details

### WebRTC Implementation
- **Peer Connection**: Direct browser-to-browser streaming
- **Data Channels**: For control message synchronization
- **Media Streams**: Canvas-based video capture with audio track support
- **ICE Candidates**: Automatic NAT traversal using Google STUN servers

### Video Processing
- **Canvas Rendering**: Real-time video frame capture at 30fps
- **Quality Scaling**: Dynamic resolution adjustment (320p/640p/original)
- **Frame Synchronization**: Uses `requestVideoFrameCallback` when available

### Audio Implementation
- **Track Management**: Automatic audio track detection and streaming
- **Fallback Support**: Silent audio track when video has no audio
- **Toggle Control**: Real-time audio enable/disable without reconnection

### Browser Compatibility
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 14+
- ✅ Edge 80+

## 📱 Responsive Design

WebRTCinema works seamlessly across devices:
- **Desktop**: Full-featured experience with all controls
- **Tablet**: Optimized layout for touch interfaces
- **Mobile**: Responsive design with stacked controls

## 🛠️ Development

### File Structure
```
WebRTCinema/
├── WebRTCinema.html    # Complete single-file application
├── README.md           # This file
└── .gitignore         # Git ignore rules
```

### Key Technologies
- **WebRTC**: Real-time communication
- **Canvas API**: Video frame processing
- **MediaStream API**: Audio/video capture
- **Modern CSS**: Glassmorphism design with gradients
- **Vanilla JavaScript**: No external dependencies

### Customization
The application is built as a single HTML file for maximum portability. You can customize:
- **Styling**: Modify CSS variables in the `<style>` section
- **Quality Presets**: Adjust resolution settings in the JavaScript
- **Buffer Settings**: Change default buffer ranges
- **STUN Servers**: Update WebRTC configuration

## 🎨 Design Features

- **Modern Glassmorphism UI**: Frosted glass effects with backdrop blur
- **Gradient Themes**: Purple to cyan gradient accents
- **Smooth Animations**: 60fps animations with cubic-bezier easing
- **Dark Theme**: Optimized for video viewing experience
- **Status Indicators**: Real-time connection and sync status

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Commit your changes** (`git commit -m 'Add amazing feature'`)
4. **Push to the branch** (`git push origin feature/amazing-feature`)
5. **Open a Pull Request**

### Areas for Contribution
- Additional video format support
- Mobile app development
- Screen sharing capabilities
- Chat functionality
- Multiple viewer support
- Recording features

## 📋 Roadmap

- [ ] **Multi-viewer Support**: Support for multiple simultaneous viewers
- [ ] **Screen Sharing**: Share your screen instead of video files
- [ ] **Chat Integration**: Built-in text chat during streaming
- [ ] **Mobile Apps**: Native iOS and Android applications
- [ ] **Recording**: Save synchronized viewing sessions
- [ ] **Playlist Support**: Queue multiple videos for continuous playback

## ⚠️ Known Limitations

- **Two-person limit**: Currently supports one host and one viewer
- **File size**: Large video files may impact initial load time
- **Network dependency**: Requires stable internet for both parties
- **Browser storage**: No localStorage used - settings reset on refresh

## 🔒 Privacy & Security

- **No data collection**: Zero telemetry or analytics
- **No external servers**: Video data never leaves your devices
- **Open source**: Full transparency with public codebase
- **Local processing**: All video processing happens in your browser

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **WebRTC Community**: For the amazing real-time communication standards
- **STUN Servers**: Google's public STUN servers for NAT traversal
- **Open Source**: Built entirely with open web technologies

---

**Made with ❤️ for synchronized video experiences**

*Star ⭐ this repo if you find it useful!*
