# 🎧 KaraoCPP: Alan Walker - Faded (Radio Edit)

**Welcome to KaraoCPP!** A creative C++ project that transforms your standard console window into a fully synchronized karaoke machine.

This specific repository features a 100% accurate, hand-tuned synchronization for the song **"Faded" by Alan Walker (Short Version / Radio Edit)**. Watch the lyrics appear smoothly on your screen, perfectly timed with the music!

---

## ✨ Features

*   🎶 **Seamless Background Audio:** Uses the Windows Multimedia API (`PlaySoundA`) to play the track asynchronously without freezing the program.
*   ⏱️ **Absolute Precision Timing:** Built with a `GetTickCount()` stopwatch mechanism. The lyrics are meticulously calculated down to the millisecond to match the exact gaps in this version.
*   ⌨️ **Dynamic Typewriter Effect:** Lyrics are printed letter-by-letter (20ms speed) to keep up with the electronic beat.
*   🎨 **Smart Highlighting:** Automatically detects structural tags like `[Chorus]` and `[Verse]` and highlights them in yellow, while the singing lyrics shine in cyan.

---

## 🛠️ System Requirements

*   **OS:** Windows (Uses `windows.h` and `mmsystem.h`).
*   **Compiler/IDE:** Visual Studio is recommended (it seamlessly links `winmm.lib`).
*   **Audio Format:** Only supports **`.wav`** files.

---

## 🚀 How to Run (Step-by-Step)

### Step 1: Download the Audio File
To experience the perfect synchronization, you must use the exact audio file this code was tuned for. 

🔗 **[Download "Alan Walker - Faded.wav" Here](https://www.mediafire.com/file/apn6hs1lrfuebrj/Alan+Walker+-+Faded.wav/file)**

*After downloading, save it to a known folder on your computer (e.g., your Music folder).*

### Step 2: The Golden Rule of C++ Paths
You must update the `filePath` variable in the `main.cpp` code to point to where you saved the audio file. 
**Important:** You MUST use double backslashes `\\` in your path!
* ❌ `C:\Users\YourName\Music\Alan Walker - Faded.wav`
* ✅ `C:\\Users\\YourName\\Music\\Alan Walker - Faded.wav`

### Step 3: Update & Play
Change line 33 in the code to match your path:
```cpp
string filePath = "C:\\Your\\Path\\Here\\Alan Walker - Faded.wav";
