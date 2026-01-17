# 🎤 Interview Practice Tool

A web-based audio practice tool that helps you improve your interview skills by recording your speech and playing it back with a configurable delay. Perfect for identifying filler words, improving pacing, and building confidence before important interviews.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

- 🎙️ **Real-time Audio Recording** - Records your practice sessions
- 🔄 **Delayed Playback** - Hear yourself with 1-10 second delay
- 📥 **Download Recordings** - Save and review your sessions later
- ⏱️ **Session Timer** - Track your practice duration
- 🎚️ **Adjustable Volume** - Control playback volume (0-100%)
- 🎨 **Clean UI** - Professional, distraction-free interface
- 📱 **Mobile Friendly** - Works on desktop and mobile devices

## 🚀 Quick Start

### Option 1: Run Locally

1. **Clone or download** the HTML file
2. **Open** `index.html` in any modern browser
3. **Click** "Start Practice" and allow microphone access
4. **Start speaking** and hear yourself with the configured delay

### Option 2: Run on Mobile (Local Network)

1. **Find your computer's IP address:**
   ```bash
   # Windows
   ipconfig
   
   # Mac/Linux
   ifconfig
   # or
   ip addr
   ```
   Look for something like `192.168.1.x`

2. **Start a local server** in the project folder:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   ```

3. **On your mobile browser**, visit:
   ```
   http://YOUR_IP_ADDRESS:8000
   ```
   Example: `http://192.168.1.5:8000`

### Option 3: Deploy to GitHub Pages

1. Create a new GitHub repository
2. Upload the HTML file (rename to `index.html`)
3. Go to **Settings** → **Pages**
4. Enable GitHub Pages from main branch
5. Access via the provided URL

## 📖 How to Use

### Basic Workflow

1. **Adjust Settings** (before starting):
   - **Playback Volume**: 0-100% (default: 80%)
   - **Playback Delay**: 1-10 seconds (default: 2 seconds)

2. **Click "Start Practice"**:
   - Grant microphone permission when prompted
   - Recording begins automatically
   - Timer starts counting

3. **Speak Naturally**:
   - Answer practice interview questions
   - Hear yourself with the configured delay
   - Notice filler words, pacing, and clarity

4. **Click "Stop"**:
   - Recording saves automatically
   - Download button appears

5. **Download & Review**:
   - Click "Download Recording" to save
   - Review offline to identify improvement areas

## 🎯 Practice Tips

### Recommended Delay Settings

| Delay | Use Case |
|-------|----------|
| **1-2 seconds** | General interview practice - catch filler words in real-time |
| **3-4 seconds** | Review pacing while continuing to speak |
| **5-7 seconds** | Advanced: hear complete sentences while forming new ones |
| **8-10 seconds** | Challenge mode - maintain coherent thought despite delay |

### Best Practices

✅ **Use headphones** to avoid audio feedback  
✅ **Practice in a quiet environment**  
✅ **Record 2-3 minute responses** to common questions  
✅ **Listen for filler words**: "um", "uh", "like", "you know"  
✅ **Check your pacing** - too fast or too slow?  
✅ **Review recordings** to track improvement over time  

### Common Interview Questions to Practice

- Tell me about yourself
- What are your strengths and weaknesses?
- Why do you want this position?
- Describe a challenging situation and how you handled it
- Where do you see yourself in 5 years?

## 🛠️ Technical Details

### Technologies Used

- **HTML5** - Structure
- **CSS3** - Styling with modern gradients
- **JavaScript** - Core functionality
- **Web Audio API** - Audio processing and delay
- **MediaRecorder API** - Recording functionality
- **MediaDevices API** - Microphone access

### Browser Compatibility

- ✅ Chrome 47+
- ✅ Firefox 25+
- ✅ Safari 11+
- ✅ Edge 79+
- ✅ Mobile Safari (iOS 11+)
- ✅ Chrome Mobile

### Audio Processing Flow

```
Microphone Input
    ↓
MediaStreamSource
    ↓
DelayNode (1-10 seconds)
    ↓
GainNode (Volume Control)
    ↓
Speakers/Headphones
```

Simultaneously:
```
Microphone Input
    ↓
MediaRecorder
    ↓
WebM Audio File
    ↓
Download
```

## 🔧 Customization with GitHub Copilot

Want to add more features? Here are prompts for GitHub Copilot:

```javascript
// Add an array of common interview questions that randomly display when you start recording

// Use Web Speech API to transcribe what I'm saying in real-time and display it below the timer

// Detect and count filler words like "um", "uh", "like", "you know" and display a counter

// Calculate and display speaking pace (words per minute) and pause duration

// Add a canvas element that shows an audio waveform visualization while recording

// Store multiple recordings in IndexedDB so they persist after page reload

// Add a playback button to listen to recordings without downloading
```

## 🐛 Troubleshooting

### Microphone not working?
- Check browser permissions (camera icon in address bar)
- Ensure no other app is using the microphone
- Try a different browser

### Audio feedback/echo?
- Use headphones instead of speakers
- Lower the playback volume
- Ensure you're not too close to speakers

### Can't download recording?
- Check browser's download settings
- Ensure popup blocker isn't active
- Try a different browser

### Works on desktop but not mobile?
- Use HTTPS (required for microphone on mobile)
- GitHub Pages/Netlify provide HTTPS automatically
- Local HTTP works but some features may be limited

## 📝 File Format

Recordings are saved as **WebM** audio files with the format:
```
interview-practice-[timestamp].webm
```

Compatible with most media players. Convert to MP3 if needed using tools like FFmpeg or online converters.

## 🤝 Contributing

Want to improve this tool? Feel free to:
- Report bugs
- Suggest features
- Submit pull requests
- Share your experience

## 📄 License

MIT License - feel free to use, modify, and distribute.

## 💡 Future Ideas

- [ ] AI-powered feedback on speech quality
- [ ] Built-in question prompts with timer
- [ ] Filler word detection and counter
- [ ] Speech-to-text transcription
- [ ] Visual waveform display
- [ ] Multiple recording sessions management
- [ ] Export to MP3 format
- [ ] Dark mode toggle

## 🙏 Acknowledgments

Built with modern web technologies. Inspired by the need for accessible, effective interview preparation tools.

---

**Made with ❤️ for job seekers and interview preparation**

*Good luck with your interviews! 🚀*