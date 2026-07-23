# 🎤 KaraoCPP: Past Lives Edition

**Welcome to KaraoCPP!** A creative, interactive C++ application that brings the Karaoke experience directly to your black console window. 

This specific repository demonstrates a perfect, 100% synchronized console karaoke for the song **"Past Lives" by sapientdream**. Complete with terminal colors and a smooth typewriter effect, it turns standard C++ output into an engaging musical show.

---

## ✨ Key Features

*   🎵 **Asynchronous Audio Playback:** Uses the Windows API (`mmsystem.h`) to play music in the background without freezing the console.
*   ⏱️ **Absolute Timing System:** Relies on a stopwatch mechanism (`GetTickCount()`) to trigger lyrics at exact milliseconds. The lyrics in this project are hand-tuned for 100% accuracy!
*   ⌨️ **Typewriter Visual Effect:** Lyrics are printed letter-by-letter to match the natural flow of singing.
*   🎨 **Smart Color Coding:** Automatically detects section headers (like `[Chorus]`) and highlights them in yellow, while the singing lyrics are displayed in cyan.

---

## 🛠️ System Requirements

*   **Operating System:** Windows (Relies on `windows.h` and Windows multimedia libraries).
*   **IDE/Compiler:** Visual Studio (Highly recommended) as it easily links `winmm.lib`.
*   **Audio Format:** The code exclusively supports **`.wav`** files via `PlaySoundA`.

---

## 🚀 Setup Instructions (Step-by-Step)

### Step 1: Download the Audio File
Because the `.wav` audio file is large, it is hosted safely on MediaFire to keep this repository lightweight and fast.

🔗 **[Download "Past Lives" WAV Audio File Here](https://www.mediafire.com/file/167pb93587mp0dl/sapientdream+-+Past+Lives+(Lyrics).wav/file)**

*After downloading, place the `.wav` file in a known folder on your computer (e.g., your Music folder).*

### Step 2: Get the Exact File Path
C++ needs to know exactly where the audio file is located on your computer.
1. Right-click your downloaded `.wav` file and select **Properties**.
2. Copy the **Location** path (e.g., `C:\Users\YourName\Music`).
3. Add your file's name and extension at the end (e.g., `C:\Users\YourName\Music\sapientdream - Past Lives (Lyrics).wav`).

### Step 3: The Critical C++ Path Rule (IMPORTANT)
In C++, a single backslash `\` is used for special commands (like `\n` for a new line). To write a Windows file path correctly, you **MUST** change every single backslash `\` into a double backslash `\\`.
* ❌ **Wrong:** `C:\Users\YourName\Music\sapientdream - Past Lives (Lyrics).wav`
* ✅ **Correct:** `C:\\Users\\YourName\\Music\\sapientdream - Past Lives (Lyrics).wav`

### Step 4: Update the Code & Run
1. Open the source code file (`main.cpp`) in Visual Studio.
2. Find the `filePath` variable near the beginning of `main()`.
3. Replace the text between the quotes with your correct double-backslash path:
   ```cpp
   string filePath = "C:\\Your\\Correct\\Path\\Here\\sapientdream - Past Lives (Lyrics).wav";
