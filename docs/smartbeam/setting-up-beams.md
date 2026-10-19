---
icon: lucide/scan-line
---

# Setting up Beams

Choose where you want to measure, place and align the hardware, then match those positions in the app. [Connect your SmartBeams](connecting-smartbeam.md) before assigning them to the sheet.

## Choose your beam locations

Choose the measurements you want to capture together. Every beam measures rock speed, and beams on sheet lines also work together to produce split times automatically.

| What you want to measure | Where to place the beams |
| --- | --- |
| Hog-to-hog time | One beam across each hog line. This is a simple starting setup with two SmartBeams. |
| Delivery split time | One beam across the back line or tee line at the throwing end, and another across that end's hog line. |
| Rock speed | Any beam location. Beyond the throwing-end hog line is the best choice for a clean post-release reading. |

### Combine measurements in one setup

You can combine the placements above. For example, with four SmartBeams, place one at each of these locations:

1. The throwing-end back line.
2. The throwing-end hog line.
3. Beyond the throwing-end hog line.
4. The receiving-end hog line.

That single setup captures **back-to-hog and hog-to-hog split times, plus rock speed at all four beams**, during the same throw. The throwing-end hog-line beam serves both splits; the beyond-hog beam adds another speed reading without replacing either hog-line beam.

With three beams at the back line and both hog lines, you still get both splits and speed at all three locations. Add the fourth beyond the hog line when you want a cleaner post-release speed reading.

### Speed at every beam

Speed is measured from how long the rock interrupts an individual beam. Back-line, tee-line, and hog-line beams all measure speed too. For a valid reading, the front of the rock must break the beam first, and the beam must re-establish behind the rock without a broom, foot, or other body part extending the interruption.

**Beyond the throwing-end hog line is the best location for post-release speed** because the rock is more likely to be clear of the thrower and their broom. Other locations work when the rock passes cleanly through the beam.

A beam on a marked line and a beam beyond it are different locations. Keep your physical placement and the location selected in the app consistent.

For a beam beyond a hog line, use **Beyond Home Hog** or **Beyond Away Hog** in the app. If these positions are hidden, check the between-hog-line locations option in **Settings**.

## Place and align each beam

Each SmartBeam uses a sensor and a separate reflector. The reflector attaches to the sensor as a cover for transport; separate them for use.

1. Place the sensor at one side of the sheet and the reflector opposite it, with the reflecting surface facing the sensor.
2. Position both so the beam crosses the sheet at your chosen measurement location. For a line-based split, align the beam across that line rather than diagonally along the sheet. Use a consistent reference on the painted line when repeating a setup.
3. Aim the sensor at the reflector. Make small adjustments until the arrow-shaped beam-state LED turns <span class="led-colour" data-led-colour="green">green</span>.
4. With the system disarmed, briefly interrupt the beam and then clear it. The arrow should turn <span class="led-colour" data-led-colour="red">red</span>, then return to <span class="led-colour" data-led-colour="green">green</span>.
5. Repeat for each beam. Recheck alignment after any unit or reflector is moved or bumped.

Use the arrow-shaped LED to check alignment; the other LEDs show different states. See [LED Indication](led-indication.md) for their meanings.

If you need to adjust the beam height or are having trouble aiming on uneven ice, see [Beam Alignment](beam-alignment.md).

Never look directly into the laser beam.

## Match the setup in the app

The sheet diagram represents the beam's position along the sheet. The coloured marker identifies the sensor assigned to that position.

1. Open the **SmartBeam** tab.
2. Tap the location on the sheet diagram that matches a physical beam.
3. Under **Place Beam Here**, choose that SmartBeam by name and case colour.
4. Repeat for the remaining units.

If a unit is missing from the choices, use **Connect New Beam** to open the scanner. If it is already assigned elsewhere, use **Move Beam Here** to move its assignment to the selected location.

### Check which unit you selected

Tap an assigned beam and choose **Identify**. The unit flashes an identification pattern so you can match it to the hardware on the ice.

### Set the throwing direction

Tap the direction arrow on the sheet diagram so it points from the throwing end toward the receiving end. Keep a consistent physical end for the diagram's **Home** labels and the other for **Away**.

When you change ends, reverse the arrow. If the hardware stays in place, keep its location assignments; if you move the hardware, update those assignments too.

## Change or remove a beam

Moving an assignment in the app does not move the equipment on the ice. Keep both in agreement.

=== "iPhone"

    Tap an assigned beam and choose **Move Beam To ...**, then select its new location. You can also tap the destination and choose the unit under **Move Beam Here ...**.

=== "Android"

    Tap the destination on the sheet diagram and choose the unit under **Move Beam Here**.

To stop using a beam in the current setup, tap it and choose **Remove From Setup**. The unit remains connected and can be assigned again later. For ending the Bluetooth connection, see [Connecting](connecting-smartbeam.md#disconnecting).

## Before the first rock

Check that every beam is clear and established, each colour is assigned to its actual location, and the direction arrow matches the throw. Ask the thrower and sweepers to keep brooms and feet clear of the beam as the rock passes.

[Continue to Arming and Timing →](arming-and-timing.md)
