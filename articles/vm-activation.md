https://www.youtube.com/watch?v=fyWWn6nl5AQ

### Overview: On-Device VM Activation (No PC Required)
Virtual Master supports native on-device activation on **Android 11 and above** via Android Wireless Debugging. Once activated, the virtual environment unlocks system-level hardware acceleration and background privileges:
- **120Hz Vulkan Direct Dispatch**: Bypasses host throttling to deliver ultra-low render latency in 3D games.
- **WRITE_SECURE_SETTINGS Access**: Ensures your guest operating system runs uninterrupted during overnight screen-off execution.
- **Enhanced Window Multitasking**: Smoother floating picture-in-picture window scaling and multi-instance split-screen performance.

Watch the video walkthrough above or follow the step-by-step instructions below.

---

### Step 1: Enable Developer Options & Wireless Debugging
1. Open your device **Settings** -> **About Phone** (or *Software Information*).
2. Tap **Build Number** 7 times continuously until the prompt confirms you are a developer.
3. Return to **Settings** -> **System** (or *Additional Settings*) -> **Developer Options**.
4. Scroll down and toggle on **Wireless Debugging**.
5. Check "Always allow on this network" and tap **Allow**.

---

### Step 2: Split-Screen or Floating Window Pairing
1. In the Wireless Debugging menu, tap **"Pair device with pairing code"**.
2. A system dialog will pop up displaying a **6-digit pairing code** along with an **IP address and Port** (e.g. `127.0.0.1:39485`).
3. Open **Virtual Master** in split-screen or floating window mode alongside your Settings app.
4. Navigate to the **Activation Wizard** in Virtual Master.
5. Enter the 6-digit pairing code and the 5-digit port number shown in the system dialog, then tap **Connect & Activate**.

---

### Step 3: Verify Activation Status
Once paired, Virtual Master automatically executes the secure authorization grant in the background:

```bash
pm grant app.virtualmaster android.permission.WRITE_SECURE_SETTINGS
