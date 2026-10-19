---
icon: lucide/chart-no-axes-combined
---

# Understanding Results

The **SmartBeam** tab shows split times and rock speeds for your current beam setup. Read the label beside each number to see which part of the throw it describes.

## Split times

A split is the time between the front of the rock breaking one beam and the front of the rock breaking another. Times are displayed in **seconds (s)**, to two decimal places.

| Split | What it measures |
| --- | --- |
| **Back to Tee** | Travel time from the throwing-end back line to its tee line. |
| **Back to Hog** | Travel time from the throwing-end back line to its hog line. |
| **Tee to Hog** | Travel time from the throwing-end tee line to its hog line. |
| **Hog to Hog** | Travel time between the two hog lines. |

The app shows the splits supported by the beams you have assigned. Several splits can be measured during one throw; you do not have to choose just one.

For the same pair of beam locations, a shorter split means the rock covered that distance faster. Compare like with like: a back-to-hog time and a hog-to-hog time describe different distances and different parts of the throw.

See [Setting up Beams](setting-up-beams.md#combine-measurements-in-one-setup) to choose and combine measurements.

## Rock speeds

Each beam measures speed at its own location. The app displays speeds in **metres per second (m/s)**, to two decimal places, with a location label such as **Home Hog Line** or **Beyond Home Hog**.

For example, **2.0 m/s at Beyond Home Hog** describes the rock's speed at that beam. It is a local speed reading, rather than the average speed over a split. A higher number means the rock is moving faster at that location.

A speed reading is calculated from how long the rock blocks one beam. The front of the rock must break it first, and the beam must clear behind the rock. A broom, foot, or body extending the interruption can produce an inaccurate speed.

Every beam can measure speed. Beyond the throwing-end hog line is the best position for a clean post-release reading because the rock is more likely to be clear of the thrower and their broom. See [Speed at every beam](setting-up-beams.md#speed-at-every-beam) for placement guidance.

## Read the live display

Before a throw starts, the main numbers show the latest available saved readings for the displayed splits and locations.

Once the first beam starts the timed throw:

1. A split's number counts upward after the rock crosses its start beam.
2. That split stops at its measured time when the rock reaches its end beam. Other splits may still be running.
3. A speed appears after the rock passes and clears that beam.
4. After the final beam, the completed measurements are saved automatically and remain available on the display.

A displayed **0.00 s** or **0.00 m/s** can mean the measurement has not been captured yet. It does not necessarily mean the rock took no time or had zero speed.

Use the lights and app status to tell whether the system is waiting, timing, or finished. See [Arming and Timing](arming-and-timing.md#how-to-know-the-system-is-ready).

## Compare recent readings

Beneath each main result, the app can show up to **three previous readings** for that split or speed location. The most recent of these smaller readings is on the left, followed by older readings to the right.

Use these to compare successive deliveries. They are individual previous measurements, not an average, and a throw without that measurement is skipped.

To hide the smaller readings, enable **Settings → Display → Hide previous times and speeds**. This changes the timing display; your saved results remain in History.

## Choose which speeds to display

Tap the filter icon beside **Rock Speeds**, or open **Settings → Display → Rock speed display locations**.

Select the areas you want to see:

- **First back and tee lines**
- **First hog line**
- **Between hog lines**
- **Far hog line**
- **Far tee and back lines**

Tap an area to switch it between **Shown** and **Hidden**, or use **All** or **None**, then tap **Done**. These groups follow the throwing direction: “first” is the throwing end and “far” is the receiving end.

**Hiding a speed only changes the display.** Speeds are still measured, saved, and included in exports. The filter does not remove beams from the setup or change the timing sequence.

The **Display times in sheet order** option in **Settings → Display** arranges results to match their positions on the sheet. Turn it off to use capture order.

## If a result is missing or unexpected

- **A split row is absent:** check that both required beam locations are assigned in the current setup.
- **A speed row is absent:** check the speed display filter and whether that beam is included in the current throwing direction's timing sequence.
- **A speed looks wrong:** check for a broom, foot, or other obstruction extending the beam break.
- **Some measurements are missing from a saved throw:** the sequence may have timed out before all beams were reached. Completed measurements can still be saved.
- **A row seems unchanged after a throw:** it may be showing an earlier measurement because the new throw did not capture that result. Check the individual throw in History.

For starting, cancelling, and timing out a throw, see [Arming and Timing](arming-and-timing.md).
