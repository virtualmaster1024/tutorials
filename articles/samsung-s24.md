### Why Samsung Devices Need Keepalive Optimization
Samsung Galaxy devices running One UI 6.0 and One UI 6.1 include an aggressive battery-saving daemon called "Device Care". By default, it automatically puts background applications into deep sleep mode after a few minutes of screen inactivity.

Follow the 3 steps below to ensure Virtual Master runs uninterrupted during screen-off gaming and long-running background tasks.

### Step 1: Set Battery Usage to "Unrestricted"
1. On your Samsung S24 home screen or app drawer, find the **Virtual Master** app icon.
2. Long-press the icon and tap the **(i) App Info** button in the top-right corner of the popup menu.
3. Scroll down and tap on **Battery**.
4. Change the selection from *Optimized* to **Unrestricted**.
   - *Note: This prevents One UI from throttling CPU allocations to the virtual machine container when the phone screen turns off.*

### Step 2: Remove from Sleeping Apps
1. Open your phone **Settings** -> Tap **Device Care** (or *Battery*).
2. Tap on **Background usage limits**.
3. Verify that Virtual Master is NOT listed under *Sleeping apps* or *Deep sleeping apps*.
4. Tap **Never sleeping apps**, tap the **+** icon in the top right, and add **Virtual Master** to this list.

### Step 3: Lock App Card in Recent Tasks
1. Swipe up and hold from the bottom of your screen to open the **Recent Apps** task switcher.
2. Tap the round **Virtual Master app icon** above its preview card.
3. Tap **Keep open** (a padlock icon will appear on the bottom-right corner of the card).

### Optional: Verify via Wireless ADB
If you have Wireless ADB enabled, you can execute the command below to verify the power whitelist status:

```bash
dumpsys deviceidle whitelist +app.virtualmaster