
# NYRA AI: Your Emotional Bangla AI Companion

NYRA AI is a cutting-edge Android AI Voice Assistant designed to be your emotional companion, primarily focusing on natural Bangla conversations while also understanding Banglish and English. This application aims to provide a human-like interaction experience with a futuristic and premium user interface.

## Features

**Core Capabilities:**
- **Bangla Voice Conversation:** Seamless and natural voice interactions in Bangla.
- **Banglish Understanding:** Naturally comprehends and responds to Banglish (a mix of Bangla and English).
- **Human-like Female Voice:** Utilizes a soft, caring, romantic, and emotional female voice with natural pronunciation.
- **Emotional AI Girlfriend Mode:** An advanced mode for deeper emotional connection (Premium Feature).
- **Offline Voice Assistant:** Performs various tasks without an internet connection.
- **Gemini AI Online Conversation Mode:** Leverages Gemini Live API for real-time, context-aware online conversations.
- **Realtime Voice Chat:** Instantaneous voice communication with the AI.
- **Loud Mobile Speaker Playback:** Optimized audio output for clear and loud playback.
- **Background Voice Conversation:** Continues conversations even when the app is in the background.
- **Wake Word Activation:** Activates upon hearing "Hey Nyra."
- **Chat History:** Maintains a record of past conversations.
- **Phone Automation:** Automates various phone functions.
- **Premium Futuristic UI:** A visually stunning user interface with glassmorphism and neon effects.
- **Lightweight Performance Mode:** Optimized for devices like Huawei Y7.

**Offline Commands:**
- Open apps
- Flashlight ON/OFF
- WiFi ON/OFF
- Bluetooth ON/OFF
- Set alarm
- Open camera
- Play music
- Read battery percentage (Planned for future development)
- Read notifications (Planned for future development)
- Local Bangla replies

**Online AI Features (Powered by Gemini Live API):**
- Realtime voice conversation
- Streaming response audio
- Emotional reply generation
- Bangla-first responses
- Context memory
- Voice interruption support

## Voice Personality

NYRA speaks:
- Natural Bangla
- Banglish
- English

Voice style:
- Cute
- Soft female voice
- Caring
- Romantic
- Emotional
- Human-like
- Natural pronunciation
- Clear and loud through phone speaker

**Example Conversation:**

**User:** Nyra, কেমন আছো? (Nyra, how are you?)
**NYRA:** আমি ভালো আছি 😊 তুমি কেমন আছো? (I am good 😊 How are you?)

**User:** আজকে মন খারাপ (I'm sad today)
**NYRA:** আরে 😔 কী হয়েছে? আমি শুনছি 💜 (Oh 😔 What happened? I'm listening 💜)

## Audio System

- **Input:** PCM 16-bit, Mono, 16kHz
- **Output:** PCM 24kHz, Loud speaker playback, Clear female voice output
- **Support:** Echo cancellation, Noise suppression, Audio interruption, Background playback

## UI Style

**Theme:**
- Futuristic
- Premium dark mode
- Glassmorphism
- Neon effects
- Animated glowing orb
- Voice waveform animation
- Floating particles

**Colors:**
- Purple
- Pink
- Cyan
- Dark background

## Project Structure

```
NYRA_AI/
├── .github/
├── .idea/
├── gradle/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/nyra/assistant/
│   │   │   │   ├── ai/
│   │   │   │   ├── audio/
│   │   │   │   ├── offline/
│   │   │   │   ├── automation/
│   │   │   │   ├── ui/
│   │   │   │   ├── data/
│   │   │   │   ├── utils/
│   │   │   │   └── MainActivity.java
│   │   │   │
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   ├── drawable/
│   │   │   │   ├── values/
│   │   │   │   ├── anim/
│   │   │   │   └── raw/
│   │   │   │
│   │   │   ├── AndroidManifest.xml
│   │   │   └── assets/
│   │   │
│   │   ├── test/
│   │   └── androidTest/
│   │
│   ├── build.gradle
│   └── proguard-rules.pro
│
├── build.gradle
├── gradlew
├── gradlew.bat
├── gradle.properties
├── settings.gradle
├── local.properties.example
├── README.md
└── AUTOMATION_ARCHITECTURE.md
```

## Getting Started

1.  **Clone the repository:**
    ```bash
    git clone <repository_url>
    cd NYRA_AI
    ```
2.  **Open in Android Studio:**
    Open the `NYRA_AI` project in Android Studio.
3.  **Sync Gradle:**
    Android Studio should automatically sync the Gradle files. If not, manually sync the project.
4.  **Build and Run:**
    Build and run the application on an Android emulator or a physical device.

## Contributing

We welcome contributions! Please see `CONTRIBUTING.md` (to be created) for details on how to contribute.

## License

This project is licensed under the MIT License - see the `LICENSE` (to be created) file for details.
