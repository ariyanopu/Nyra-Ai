# AUTOMATION_ARCHITECTURE.md

This document will detail the architecture for phone automation features within NYRA AI.

## Overview

The phone automation module is designed to allow NYRA AI to interact with various device functionalities based on user voice commands. This includes actions like toggling Wi-Fi, Bluetooth, flashlight, setting alarms, opening applications, and potentially more advanced features like reading notifications and battery status.

## Components

1.  **Speech-to-Text (STT) Integration:**
    *   Transcribes user voice commands into text.
    *   This text is then fed into the `OfflineCommandEngine`.

2.  **OfflineCommandEngine:**
    *   **Command Parsing:** Analyzes the transcribed text to identify specific keywords and phrases that correspond to predefined automation commands (e.g., "flashlight on", "open camera").
    *   **Intent Recognition:** Determines the user's intent (e.g., `TOGGLE_FLASHLIGHT`, `OPEN_APP`).
    *   **Action Execution:** Based on the recognized intent, it triggers the appropriate Android system API calls or intents to perform the desired action.
    *   **Response Generation:** Formulates a verbal response to confirm the action or provide feedback to the user.

3.  **Android System APIs/Intents:**
    *   **`WifiManager`:** For toggling Wi-Fi.
    *   **`BluetoothAdapter`:** For toggling Bluetooth.
    *   **`CameraManager`:** For controlling the flashlight (torch mode).
    *   **`AlarmClock` Intent:** For setting alarms.
    *   **`Intent.ACTION_VIEW` / `Intent.ACTION_MAIN`:** For opening applications or system components like the camera or music player.
    *   **`NotificationListenerService` (Future):** For reading notifications.
    *   **`BatteryManager` (Future):** For reading battery percentage.

4.  **Permissions Management:**
    *   The application will require various Android permissions (e.g., `CAMERA`, `BLUETOOTH_ADMIN`, `CHANGE_WIFI_STATE`, `SET_ALARM`) to execute automation commands.
    *   Permissions will be requested at runtime where necessary, and users will be informed of the required permissions.

## Workflow

1.  User speaks a command (e.g., "Hey Nyra, turn on flashlight").
2.  The `MicRecorder` captures the audio.
3.  The audio is processed by the STT component (either offline or via Gemini Live API).
4.  The transcribed text is passed to the `OfflineCommandEngine`.
5.  `OfflineCommandEngine` parses the command and identifies the intent.
6.  If a matching automation command is found, the `OfflineCommandEngine` executes the corresponding Android API call or intent.
7.  NYRA AI provides a verbal confirmation or feedback to the user via `AudioPlayer`.

## Future Enhancements

-   **Advanced NLP for Command Parsing:** Implement more sophisticated natural language processing to understand a wider range of command variations and contexts.
-   **Dynamic App Opening:** Develop a mechanism to dynamically map spoken app names to their respective package names for opening.
-   **Notification Reading:** Integrate `NotificationListenerService` to allow NYRA to read out notifications.
-   **Battery Status:** Implement functionality to read and report the device's battery percentage.
-   **Contextual Automation:** Enable NYRA to perform actions based on the current context (e.g., "turn on silent mode when I'm in a meeting").
-   **User-defined Routines:** Allow users to define custom automation routines or macros.
