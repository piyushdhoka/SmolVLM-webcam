# SmolVLM Real-time Webcam Assistant

A real-time webcam assistant that uses SmolVLM (Small Vision Language Model) to provide intelligent responses about what it sees through your webcam. The application features voice commands, real-time processing, and both continuous and single-frame capture modes.

## Features

- 🎥 Real-time webcam feed processing
- 🗣️ Voice command support with speech recognition
- 🔊 Text-to-speech responses
- 🔄 Continuous monitoring mode
- 📸 Single frame capture option
- ⚡ Real-time processing with visual feedback
- 📱 Responsive design for desktop and mobile
- 🎯 Configurable silence threshold for voice commands

## Prerequisites

- A modern web browser (Chrome, Firefox, Edge, or Safari)
- Webcam access
- SmolVLM server running locally (or accessible via network)
- Microphone access (for voice commands)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/smolvlm-realtime-webcam.git
cd smolvlm-realtime-webcam
```

2. Start the SmolVLM server:
```bash
# Navigate to the llama.cpp directory
cd llama.cpp/tools/server

# Start the server
./server
```

3. Open the application:
   - For basic version: Open `index.html` in your browser
   - For voice-enabled version: Open `auto.html` in your browser

## Usage

### Basic Version (index.html)

1. Open `index.html` in your browser
2. Grant camera permissions when prompted
3. Set your API endpoint (default: http://localhost:8080)
4. Enter your instruction or use the default "What do you see?"
5. Click "Start" to begin processing
6. Click "Stop" to end processing

### Voice-Enabled Version (auto.html)

1. Open `auto.html` in your browser
2. Grant camera and microphone permissions when prompted
3. Set your API endpoint (default: http://localhost:8080)
4. Toggle the Voice Assistant switch to enable voice commands
5. Choose your preferred silence threshold
6. Use either:
   - Continuous Mode: Automatically processes frames every 2 seconds
   - Single Frame Capture: Process one frame at a time
7. Speak your commands or type them in the Voice Command field

## Voice Commands

The voice-enabled version supports natural language commands. Some examples:
- "What do you see?"
- "Describe the scene"
- "Is there a person in the frame?"
- "What color is the object?"

## Configuration

### API Endpoint
- Default: `http://localhost:8080`
- Can be changed in the UI to point to any SmolVLM server

### Silence Threshold
- Configurable options: 0.5s, 1s, 1.5s, 2s
- Determines how long to wait after speech before processing

## Browser Support

- Chrome (recommended)
- Firefox
- Edge
- Safari

Note: Voice features require browser support for the Web Speech API.

## Security Considerations

- The application runs entirely in the browser
- No data is stored or transmitted except to your configured API endpoint
- Camera and microphone access require explicit user permission
- All processing is done locally before sending to the API

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Built with SmolVLM and llama.cpp
- Uses the Web Speech API for voice features
- Inspired by the need for accessible AI vision assistance
