# 🎤 KaraoCPP: The Ultimate C++ Console Karaoke

**Welcome to KaraoCPP!** A creative, interactive C++ application that brings the Karaoke experience directly to your black console window. 

This project demonstrates how to play `.wav` audio files asynchronously while displaying synchronized lyrics using an absolute timing system. Complete with terminal colors and a smooth typewriter effect, it turns standard C++ output into an engaging musical show.

---

## ✨ Key Features

*   🎵 **Asynchronous Audio Playback:** Uses the Windows API (`mmsystem.h`) to play music in the background without freezing the console.
*   ⏱️ **Absolute Timing System:** Relies on a stopwatch mechanism (`GetTickCount()`) to trigger lyrics at exact milliseconds. Tweak one line without breaking the rest of the song!
*   ⌨️ **Typewriter Visual Effect:** Lyrics are printed letter-by-letter to match the natural flow of singing.
*   🎨 **Smart Color Coding:** Automatically detects section headers (like `[Chorus]`) and highlights them in yellow, while the singing lyrics are displayed in cyan.

---

## 🛠️ System Requirements

*   **Operating System:** Windows (Relies on `windows.h` and Windows multimedia libraries).
*   **IDE/Compiler:** Visual Studio (Highly recommended) as it easily links `winmm.lib`.
*   **Audio Format:** The code exclusively supports **`.wav`** files via `PlaySoundA`.

---

## 🚀 How to Run the Project (Step-by-Step)

### Step 1: Prepare Your Audio File
Because the Windows `PlaySound` function only supports `.wav` files, you must convert your `.mp3` song first.
1. Go to any free online audio converter (e.g., [CloudConvert](https://cloudconvert.com/mp3-to-wav) or [FreeConvert](https://www.freeconvert.com/mp3-to-wav)).
2. Upload your `.mp3` file and convert it to **WAV**.
3. Download the new `.wav` file and save it somewhere easy to find, like your `Music` or `Documents` folder.

### Step 2: Get the Correct File Path
C++ needs to know exactly where your song is located. Here is how to get the correct path:
1. Right-click on your new `.wav` file and select **Properties**.
2. Look at the **Location** (e.g., `C:\Users\YourName\Music`).
3. Add the file name at the end (e.g., `C:\Users\YourName\Music\mysong.wav`).
4. **⚠️ CRITICAL C++ RULE:** When pasting the path into the code, you **MUST** change all single backslashes `\` to double backslashes `\\`. 
   * *Wrong:* `C:\Users\Name\Music\song.wav`
   * *Correct:* `C:\\Users\\Name\\Music\\song.wav`

### Step 3: Setup the Code
1. Clone this repository or copy the `main.cpp` code.
2. Open Visual Studio and create a new **Console App** project.
3. Paste the code.
4. Replace the `filePath` variable with your correct double-backslash path:
   ```cpp
   string filePath = "C:\\Users\\YourName\\Music\\mysong.wav";
