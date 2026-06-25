# 🚀 MUTUM

A local-AI native IDE designed for visual thinkers. 

---

## 📋 1. Prerequisites

Before launching MUTUM, ensure you have a local AI environment ready on your Mac. You can choose either of the following options:

⚠️ **For macOS Users (Gatekeeper Block)**
Since this build is released directly without Apple Notarization, macOS will display a warning telling you to "Move to Trash." You can easily bypass this using one of the following methods:
<img width="249" height="254" alt="Screenshot 2026-06-22 at 8 46 09" src="https://github.com/user-attachments/assets/8337c64a-e679-4e37-930b-f2c76ceac848" />


Method A (Recommended for Devs):
Move the app to your /Applications folder, open Terminal, and run:
xattr -cr /Applications/MUTUM.app

Method B (System Settings):
Close the warning, go to System Settings ➔ Privacy & Security, and click "Open Anyway".
<img width="705" height="431" alt="Screenshot 2026-06-22 at 8 48 22" src="https://github.com/user-attachments/assets/389ff1c9-81a0-4c5d-a9fd-309ec6a8c042" />


### Option A: Apple Intelligence (Recommended for an Easy Start)
If you are using an **M1 or later Mac**, you can utilize the built-in **Apple Intelligence (Apple Foundation Models "AFM")** as your local AI right out of the box! This is the easiest and most seamless way to get started.
* ⚠️ **Important**: You must configure your macOS System Settings so that the language for your system and Siri / Apple Intelligence matches your preferred language (e.g., Japanese).

### Option B: Ollama (Flexible & Customizable)
If you prefer to use various open-source models, you can install and run **Ollama**.

#### Step 1: Install Ollama
1. Go to the official website: [https://ollama.com](https://ollama.com)
2. Download the Mac application and install it by moving it to your Applications folder.
3. Launch the Ollama application. You will see an icon appear in your Mac's menu bar.

#### Step 2: Download AI Models via Terminal
To use models with MUTUM, you need to download them using your Mac's **Terminal** app.
1. Open the **Terminal** app (Press `Cmd + Space`, type "Terminal", and press Enter).
2. Type the download command and press Enter to pull your preferred model.

#### 💡 Choosing the Right Model Size (Based on your Mac's RAM)
As a rule of thumb, the **AI model's file size equals its memory (RAM) usage**. Since you will likely run MUTUM alongside other heavy applications (like Xcode), choose a model size that leaves enough breathing room for your Mac:

| Mac Memory (RAM) | Recommended Model Size | Model File Size | Example Commands | Performance Note (When Multitasking) |
| :--- | :--- | :--- | :--- | :--- |
| **8 GB** | **3B models** | ~2.0 GB | `ollama pull qwen2.5:3b`<br>`ollama pull llama3.2:3b` | Runs very fast. Essential for 8GB Macs. |
| **16 GB** | **7B / 8B models** | **Under 5.0 GB**<br>*(Up to 7.0 GB)* | `ollama pull qwen2.5:7b` | **Files under 5GB run smoothly** even with other tools open. 7GB models will work but may feel sluggish. Anything higher is not recommended. *(Note: Qwen2.5:7b is around 4.7 GB, making it a perfect sweet spot!)* |
| **24 GB / 36 GB+** | **14B / 32B models** | 9.0 GB ~ 20 GB | `ollama pull qwen2.5:14b` | Highly intelligent. Ideal for complex tasks if your Mac has 24GB+ of RAM. |

3. Once the download reaches 100%, the model is ready to use locally.

---

## 📦 2. Download & Installation

Since MUTUM is distributed directly via GitHub (not the App Store), please follow these steps to install it safely on macOS:

1. Go to the **Releases** page of this repository.
2. Download the latest version of `MUTUM.dmg` (or `MUTUM.zip`).
3. Open the downloaded file and drag **MUTUM** into your **Applications** folder.

### ⚠️ IMPORTANT: macOS Security Bypass
When you open MUTUM for the first time, macOS may show a warning saying: *"MUTUM cannot be opened because the developer cannot be verified."* To bypass this and open the app:
1. Control-click (or right-click) the **MUTUM** icon in your Applications folder.
2. Select **Open** from the shortcut menu.
3. Click **Open** in the dialog box that appears. 
*(Note: You only need to do this once. The app will open normally next time.)*

---

## ⚙️ 3. Initial Setup

Once the app is open, you are just a few steps away from your visual thinking experience:

1. **Connect to Your Local AI**: Select your preferred backend (Apple Intelligence or Ollama) in the settings panel.
   * For Ollama, ensure your server URL (e.g., `http://localhost:11434`) is correctly entered.
2. **Select Your Model**: Choose your preferred local model from the dropdown list.
3. **Open a Project**: Select your workspace folder and start interacting with your local AI natively!

---

How to set up Draw Things API integration
Step 1. Download "Draw Things"
Get the free "Draw Things" app from the Mac App Store.

Step 2. Download a Model
Open the app and download your preferred image generation model from the top-left menu.
(Recommendation: DreamShaper v8 is highly recommended for the best results and performance.)
<img width="283" height="151" alt="Screenshot 2026-06-24 at 17 39 46" src="https://github.com/user-attachments/assets/cc2cb106-5907-43a8-bed9-9eb5f4a46f44" />

Step 3. Enable the API
Open the settings in the Draw Things app (usually a gear icon or via the menu). Find the option for "Enable HTTP API Server" and turn it ON.　**Note: You need to enable HTTP API Server whenever launching Draw Things app.**
<img width="285" height="630" alt="Screenshot 2026-06-24 at 17 33 26" src="https://github.com/user-attachments/assets/e37d01ff-a53a-4769-a6ac-8234dc131895" />


Step 4. Configure the Endpoint in MUTUM
Open MUTUM's Options and navigate to the Integrations tab. Under Local Image Gen Settings, enter the following URL into the Image Gen API Endpoint field:
[http://127.0.0.1:7860/sdapi/v1/txt2img](http://127.0.0.1:7860/sdapi/v1/txt2img)

<img width="313" height="214" alt="Screenshot 2026-06-24 at 17 34 17" src="https://github.com/user-attachments/assets/7428e971-56f1-4206-873f-65cdb0b1a04d" />

Step 5. Ready to Generate!
Keep the Draw Things app running in the background. MUTUM will now communicate with it, allowing you to generate images completely locally and privately!

## 💬 Community & Support

We welcome your feedback, ideas, and questions! 

* For general discussions, questions, or sharing ideas, please join our **[GitHub Discussions](YOUR_DISCUSSIONS_URL_HERE)** tab.
* For bug reports or explicit feature requests, please open an issue in the **[GitHub Issues](YOUR_ISSUES_URL_HERE)** tab.

---

## 📄 Privacy Policy & Terms of Service
Please review our [Privacy Policy](./PRIVACY_POLICY.md) and [Terms of Service](./TERMS.md) before using the application.
