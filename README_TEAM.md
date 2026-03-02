# 🎙️ Meeting Translator HUD (Team Guide)

This is a real-time Japanese-to-English translation tool designed to sit as a transparent "Heads-Up Display" (HUD) on your screen during meetings.

## 🚀 Quick Start (Windows)

1.  **Download the Executable:**
    *   Go to the `dist/` folder in this project and download `live_gui.exe`.
2.  **Run the App:**
    *   Double-click `live_gui.exe`. 
    *   *Note: If Windows Defender shows a "Windows protected your PC" warning, click **More info** -> **Run anyway**.*
3.  **Select Your Audio Source:**
    *   **Remote Meeting (Zoom/Teams):** Select your **Speakers (Loopback)** or **Headphones (Loopback)**. This captures the audio coming *out* of your meeting software.
    *   **In-Person Meeting:** Select your laptop's **Microphone**.
4.  **Position the HUD:**
    *   Click and drag the window to move it.
    *   Right-click anywhere on the HUD to close the app.

---

## 💡 How to Use in Meetings

### 🎧 Mode A: Remote (Zoom, Teams, Google Meet)
To translate your colleagues on a call:
*   Ensure your meeting audio is playing through your default speakers or headphones.
*   In the app's device selection, choose the **(Loopback)** version of that device.
*   The HUD will now "listen" to the meeting audio and provide live translations.

### 🎙️ Mode B: In-Person
To translate people in the same room as you:
*   Select your physical **Microphone** from the list.
*   Place your laptop or mic closer to the speakers for the best results.

---

## 🛠️ Troubleshooting

*   **"I don't see any text!"**
    *   Check the console window that opens behind the HUD. If it says `[Audio Flowing] Peak: 0.0000`, it means it's not hearing anything. Try selecting a different (Loopback) device.
*   **"The translation is cut off."**
    *   The app waits for a natural pause in speech before translating. If someone speaks very quickly without pausing, there might be a slight delay.
*   **"Is my audio being recorded?"**
    *   The audio is processed in real-time via Deepgram and OpenAI APIs. No audio files are saved locally or permanently stored.

---

## 💻 For Developers (Running from Source)

If you want to run or modify the code yourself:
1.  Install Python 3.11+.
2.  `pip install -r requirements.txt`
3.  Create a `.env` file with your `DEEPGRAM_API_KEY` and `OPENAI_API_KEY`.
4.  Run `python live_gui.py`.
