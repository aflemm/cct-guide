---
icon: lucide/download
---

# Firmware Updates

Firmware is the software running inside each SmartBeam. The app checks for compatible updates and installs them over Bluetooth.

## Before updating

- Switch on and [connect](connecting-smartbeam.md) the units you want to update.
- Make sure your phone has internet access for checking and downloading updates.
- Check each unit's charge. The app requires at least **5% battery** to start an update; [charge the unit](charging.md) first if needed.
- Finish or cancel your timed throw before updating. Keep the phone nearby and the app open until the updates finish, and leave the units powered on.

## Check for updates

1. Open **Settings** and tap **Update Centre** beneath the connected units.
2. The **SmartBeam Update Centre** checks connected SmartBeams. Tap **Check Now** to check again.
3. Review the units under **Updates Available**, **Up to Date**, or **Check Status**.

Each unit's row identifies it by name, colour, and serial number, and shows its installed firmware version. When an update is available, it also shows the target version. Updates marked **Urgent** are prioritised when updating several units.

If Update Centre is missing from Settings, connect a SmartBeam first. You can also open a connected unit's details to check its firmware version and update status.

## Install an update

Tap **Update** beside a unit. If several units have updates available, **Update All** queues them and transfers firmware to one unit at a time.

Follow the status shown for each unit:

| Status | What is happening |
| --- | --- |
| **Waiting to update** | The unit is queued behind another update. |
| **Downloading firmware** | The app is obtaining and checking the update file. |
| **Transferring firmware** | The app is sending the firmware to the SmartBeam over Bluetooth. |
| **Waiting for SmartBeam to reconnect and verify firmware** | Transfer has finished; the app is waiting for the unit to restart, reconnect, and report its installed version. |
| **Up to Date** | The check or completed update confirms that no newer eligible update is available. |

**100% transferred is not the final confirmation.** Leave the app open while it waits for the unit to reconnect and verify its firmware.

Firmware with update-light support alternates a dim <span class="led-colour" data-led-colour="purple">purple</span> indication between the system-state LEDs during the transfer. The beam-state and charging indicators keep their usual meanings.

## Cancel an update

Use **Cancel** beside a unit to stop an update that is queued, downloading, or transferring. The top **Cancel** button offers **Continue Updates** or **Cancel Updates** before closing the centre.

An update already sent to a SmartBeam may still finish installing. Cancellation is unavailable while the app is waiting for that unit to reconnect and verify the installed version.

## If an update cannot proceed

Read the status beside the affected unit. It may need more battery charge, a working connection, or completion of another firmware transfer. The app also checks whether the update is compatible with that unit.

If checking or downloading fails, check the phone's internet connection and use **Check Now** again. If Bluetooth disconnects during transfer, reconnect the unit and check its installed version and update status before retrying.

For a unit that has finished transferring, allow it to reconnect before starting another attempt. If it does not reconnect, use the [scanner](connecting-smartbeam.md) to check the connection. Contact [Curling Tools](../contact.md) if the reported error persists.
