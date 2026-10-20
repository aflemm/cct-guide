---
icon: lucide/history
---

# History and Data

Use **History** to review saved throws, and **Settings → Data Management** to export or erase them.

## Find previous throws

Open the **History** tab. Throws appear newest first, with their split times, rock speeds, time of day, and throwing end grouped together.

| Filter | What it shows |
| --- | --- |
| **Today** | Throws recorded today, starting with **Most Recent Rock**. Earlier entries are labelled by how many rocks ago they were recorded. |
| **Yesterday** | Throws recorded on the previous day. |
| **Dates** | Throws between the selected **Start** and **End** dates, including both days. |
| **All** | All saved throws. |

If you see **No Rocks Found**, try another date range or **All**.

The rock speed display filter also applies to History. If a speed is hidden, you can show it again without taking another measurement. See [Choose which speeds to display](understanding-results.md#choose-which-speeds-to-display).

For the meaning and units of each reading, see [Understanding Results](understanding-results.md).

## Check your stored data

Open **Settings → Data Management**. **Database Details** shows the number of timed rocks stored, their date range, and the storage size.

Completed measurements are saved automatically. A timed-out throw can contain only the measurements completed before the timeout; cancelling a throw does not save it. See [Cancelling and Timeouts](cancelling-and-timeouts.md).

## Export to CSV

1. Open **Settings → Data Management**.
2. Tap **Export to CSV**.
3. Use the iPhone share sheet to save the file or send it to the app you want to use for analysis.

The export includes **all saved timing data**, regardless of the date filter selected in History. Speeds hidden by the display filter are included too. Export is unavailable when there is no saved timing data.

### Read the exported file

A throw can occupy several CSV rows: one per split and one per speed reading. Rows with the same **rock_id** belong to the same throw.

The file includes the throw's timestamp and direction, each measurement's locations, split durations in seconds, and speeds in metres per second. Use **record_type** to distinguish split rows from speed rows. Blank fields are normal when a column does not apply to that measurement.

## Erase saved timing data

In **Settings → Data Management**, choose the erase option that matches what you want to remove:

| Option | What it removes |
| --- | --- |
| **Erase all data collected today** | Throws recorded today. |
| **Erase data collected before** | Throws recorded before the selected date. Data from the selected day is kept. |
| **Erase all saved timing data** | Every saved throw. |

Check the confirmation message, then tap **Erase** to proceed or **Cancel** to keep the data.

**Erasing cannot be undone.** Export anything you want to keep before erasing it.
