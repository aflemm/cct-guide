---
icon: lucide/activity
---

# Raw Live Data

Raw mode streams individual force samples from SmartBroom 4 to the app. Use it to look closely at the force trace or export samples for your own analysis. For normal practice with stroke statistics, sweepers, and saved sessions, use [Live Sweeping](using-smartbroom.md).

**Raw captures stay in memory for the current app session.** They are not saved to Review as sweep sessions or restored after relaunch. Export any capture you want to keep.

## Capture raw force

1. [Connect your broom](connecting-smartbroom.md) and open **Raw Live Data** on the connected-broom screen. If the broom is bonded, the app needs its key to unlock live data access; see [Bonding and Ownership](bonding.md).
2. Choose a **Sample period**: **2, 5, 10, 50, or 100 ms**. A shorter period requests more frequent samples. The default is **10 ms**.
3. Tap **Start Capture** and keep the broom connected. The force chart updates as samples arrive. The system-state LEDs flash <span class="led-colour" data-led-colour="blue">blue</span> rapidly during raw data transfer.
4. Tap **Stop Capture** when finished. You cannot change the sample period during a capture.

Leaving the Raw Live Data screen stops the current capture. A Bluetooth disconnection also stops it.

## Review and export

After stopping, the latest capture remains on the chart. Tap **Export CSV** to save or share its samples.

**Capture History** lists completed captures from this app session, newest first. Open one to see its start time, sample count, duration, and force chart. Choose **Raw Data Points** to inspect each sample's time since the start and force, displayed in your selected kilograms or pounds.

Each capture's detail screen also offers **Export CSV**. Save the file before closing the app if you need the data later.
