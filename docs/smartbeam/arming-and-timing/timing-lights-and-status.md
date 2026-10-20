---
icon: lucide/lightbulb
---

# Timing Lights and Status

The **system-state LEDs at the ends of the top light-bar** show readiness and timing progress. The arrow-shaped beam-state LED is separate; see [LED Indication](../led-indication.md) for the LED locations and other patterns.

## How to know the system is ready

You can use the colour of the lights to understand what the system is doing without looking at your phone. When it is ready to time your throw, the closest beam shows <span class="led-colour" data-led-colour="yellow">yellow</span> and the beams farther down the sheet show <span class="led-colour" data-led-colour="purple">purple</span>.

The <span class="led-colour" data-led-colour="yellow">yellow</span> beam is the **hot beam**: the next one the system expects the rock to break. The <span class="led-colour" data-led-colour="purple">purple</span> beams are armed and waiting their turn. The app shows **READY** at this point too.

### Follow the lights as the rock travels

1. **At the first beam:** timing starts as the rock breaks it. Once the beam clears behind the rock, its system-state LEDs show <span class="led-colour" data-led-colour="green">green</span> to confirm the rock has passed. The app shows **ACTIVE**.
2. **Down the sheet:** each next beam turns <span class="led-colour" data-led-colour="yellow">yellow</span> when it becomes hot, then <span class="led-colour" data-led-colour="green">green</span> once the rock has passed and the beam clears. Beams still waiting their turn remain <span class="led-colour" data-led-colour="purple">purple</span>.
3. **After the last beam:** the throw finishes and its measurements are saved to **History**. The lights then change according to the arming mode: idle, a new arming countdown, or waiting for a First Beam arming command.

Split times finish as the rock reaches their end beams, and speed readings appear as each beam clears. One throw can capture several measurements; see [Combine measurements in one setup](../choosing-measurements.md#combine-measurements-in-one-setup).

Breaking a waiting <span class="led-colour" data-led-colour="purple">purple</span> beam does not advance the timing sequence. The system follows the <span class="led-colour" data-led-colour="yellow">yellow</span> hot beam.

### Hot, idle, or outside the setup

- **<span class="led-colour" data-led-colour="blue">Blue</span>:** the beam is in the setup, but the system is idle and disarmed. Wait until it is armed before delivering.
- **<span class="led-colour" data-led-colour="teal">Teal</span>:** the First Beam control is waiting for you to trip it to start arming. This is different from being ready to time a rock.
- **<span class="led-colour" data-led-colour="white">White</span>:** the unit is connected but outside the setup. It will not participate until you assign it a location.

The readiness colours apply to participating beams. By default, receiving-end tee and back-line beams are excluded from the sequence, so a draw can finish before reaching them. See [Active Beam Locations](../settings.md#active-beam-locations) to include them for hit-speed practice.

## Understand the status

| Status | Meaning |
| --- | --- |
| **IDLE** | Waiting to be armed. |
| **ARMING** | An arming countdown is running. Wait for **READY**. |
| **READY** | Armed and waiting for the first beam break. |
| **ACTIVE** | A throw is being timed. |
| **PAUSED** | The single-beam First Beam pause is running. |

See [Arming Modes](../arming-modes.md) to prepare for the next throw, or [Cancelling and Timeouts](../cancelling-and-timeouts.md) to stop a cycle or handle an incomplete throw.
