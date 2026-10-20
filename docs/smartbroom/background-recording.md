---
icon: lucide/history
---

# Background Recording

SmartBroom 4 can record sweeping data in its own memory without a phone connected. You can download it afterward for review.

This is different from [Live Sweeping](using-smartbroom.md), where stroke measurements are streamed to the app. It does not mean the phone app needs to stay running in the background.

## Prepare before going on the ice

1. Charge and switch on the broom, then [connect it to the app](connecting-smartbroom.md).
2. Tap **Collect Background Sweeping Data** and complete the ownership check. For an unclaimed broom, choose **Claim SmartBroom**.
3. Wait until ownership is confirmed. The app remembers the key needed to download the recorded data and synchronises the broom's clock during connection.
4. Stop any live sweep or [raw capture](raw-live-data.md) before relying on local recording.
5. If you disconnect for use on the ice, check that **both system-state LEDs show solid <span class="led-colour" data-led-colour="blue">blue</span>**. This indicates the disconnected broom is ready to save locally.

The app may show **Background Sweeping Data Ready** once ownership is unlocked. Before leaving the phone behind, also check the physical recording indication: ownership alone does not confirm that the clock, calibration, and available storage are all ready.

## While sweeping

Leave the broom powered on and use it normally. It detects and saves sweeping strokes for later processing into sweeps and sessions.

A phone connection does not, by itself, stop background collection. A prepared broom can save locally while connected when it is not in live broadcast or file-transfer mode. Connected idle lights blend <span class="led-colour" data-led-colour="blue">blue</span> and <span class="led-colour" data-led-colour="purple">purple</span>, rather than showing the disconnected solid-blue indication.

Power-saving settings can put the broom to sleep after inactivity. Check that it is awake before collecting more data; see [Settings](settings.md#broom-power-saving).

## Download after sweeping

1. Reconnect with the app that holds the broom's bonding key. It attempts to unlock the broom automatically.
2. Check **Saved Data** on the connected screen. Tap **Download** if records are available and have not already started transferring.
3. Keep the connection while **Downloading Saved Data** is shown.
4. Use **Download History** to inspect the download, or **Review → SmartBroom 4** to browse the resulting sessions.

Once the saved records have been synced, the connected screen checks for newly recorded data about every **30 seconds** while it is open, and downloads new records. **Check Now** requests a check immediately.

Downloaded records are cleared from the broom once the app confirms receipt, freeing storage space. Keep the data in the app or [export it](sessions.md#export-or-remove-data) before deleting it.

## If it is not recording

- **Alternating white lights while disconnected:** the broom is not ready to save locally. Reconnect and check ownership and device status.
- **Alternating white and purple:** a bonded broom needs the app to set its clock or download stored data because storage is full.
- **Locked or missing key in the app:** recording may continue on an already bonded broom, but this app cannot download it until it has the owner's key.

See [Bonding and Ownership](bonding.md) before changing ownership, and [LED Indication](led-indicators.md) for the light patterns.
