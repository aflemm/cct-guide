---
icon: lucide/key-round
---

# Bonding and Ownership

Bonding is how SmartBroom 4 remembers which app can access its saved sweeping data. The app calls this **claiming** the broom. It is separate from simply connecting over Bluetooth.

## Claim an unclaimed broom

1. Connect the broom in the **SmartBroom** tab.
2. Open **Collect Background Sweeping Data** and choose **Claim SmartBroom**, or use **Claim** beside the ownership status.
3. Wait for ownership to be confirmed. The status becomes **Owned and unlocked**.

The app creates and remembers a bonding key and sends it to the broom. The broom can then save background data, provided its clock, calibration, and storage are ready. On later connections, the app uses its remembered key to unlock saved-data access automatically.

An unclaimed broom can stream live sweeps, but does not save offline background records. Once bonded, the broom requires the matching key for downloads and live data access. It can continue saving locally while disconnected and locked.

## Use another Apple device

The app syncs remembered brooms and bonding keys through iCloud when available. Another device using the same iCloud account can obtain the same key and unlock the broom. Allow for sync to complete; confirm ownership in the app rather than assuming a Bluetooth connection has unlocked it.

Separate windows on the same iPad use the same remembered keys. They do not need separate claims. See [Multiple Windows on iPad](ipad-windows.md).

## If the key is unavailable

**Locked — key unavailable** means the broom is already bonded but this app does not have a usable key. Use the owner's app, or restore access to the same key through your own synced device.

**Erase & Claim** is a change of ownership: it deletes all data stored on the broom and creates a new key for this app. It cannot recover the previous owner's recordings. Download anything you need with the original key before taking over.

## Release or forget a broom

- **Release** removes the broom's ownership and erases its stored data. Confirm only after downloading anything you want to keep.
- **Forget This Device**, under **Settings → Saved SmartBroom Devices**, removes the remembered broom and its key. Without that same key, recordings still on the broom cannot be recovered. The app warns before forgetting a bonded broom.
- **Disconnect** only ends the connection. Use it when you want to keep ownership and saved-data access for later.

After claiming, follow [Background Recording](background-recording.md) to check that local collection is ready.
