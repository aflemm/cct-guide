---
icon: lucide/timer
---

# Arming and Timing

Arming tells SmartBeam to wait for the next rock. Timing starts when the rock breaks the first beam in its path.

Before you begin, [connect your SmartBeams](connecting-smartbeam.md), [assign their locations](setting-up-beams.md), and check the throwing direction. At least one beam must be in the setup, and every beam used for the throw must be clear and established before the system can arm.

The colours below refer to the **system-state LEDs at the ends of the top light-bar**. See [LED Indication](led-indication.md) for the LED locations and the separate beam-state and charging indicators.

## How to know the system is ready

You can use the colour of the lights to understand what the system is doing without looking at your phone. When it is ready to time your throw, the closest beam shows <span class="led-colour" data-led-colour="yellow">yellow</span> and the beams farther down the sheet show <span class="led-colour" data-led-colour="purple">purple</span>.

The <span class="led-colour" data-led-colour="yellow">yellow</span> beam is the **hot beam**: the next one the system expects the rock to break. The <span class="led-colour" data-led-colour="purple">purple</span> beams are armed and waiting their turn. The app shows **READY** at this point too.

### Follow the lights as the rock travels

1. **Before delivery:** the nearest participating beam is <span class="led-colour" data-led-colour="yellow">yellow</span>; the later beams are <span class="led-colour" data-led-colour="purple">purple</span>.
2. **At the first beam:** timing starts as the rock breaks it. Once the beam clears behind the rock, its system-state LEDs show <span class="led-colour" data-led-colour="green">green</span> to confirm the rock has passed. The app shows **ACTIVE**.
3. **Down the sheet:** each next beam turns <span class="led-colour" data-led-colour="yellow">yellow</span> when it becomes hot, then <span class="led-colour" data-led-colour="green">green</span> once the rock has passed and the beam clears. Beams still waiting their turn remain <span class="led-colour" data-led-colour="purple">purple</span>.
4. **After the last beam:** the throw finishes and its measurements are saved to **History**. The lights then change according to the arming mode: idle, a new arming countdown, or waiting for a First Beam arming command.

Split times finish as the rock reaches their end beams, and speed readings appear as each beam clears. One throw can capture several measurements; see [Combine measurements in one setup](setting-up-beams.md#combine-measurements-in-one-setup).

Breaking a waiting <span class="led-colour" data-led-colour="purple">purple</span> beam does not advance the timing sequence. The system follows the <span class="led-colour" data-led-colour="yellow">yellow</span> hot beam.

### Hot, idle, or outside the setup

- **<span class="led-colour" data-led-colour="blue">Blue</span>:** the beam is in the setup, but the system is idle and disarmed. Wait until it is armed before delivering.
- **<span class="led-colour" data-led-colour="teal">Teal</span>:** the First Beam control is waiting for you to trip it to start arming. This is different from being ready to time a rock.
- **<span class="led-colour" data-led-colour="white">White</span>:** the unit is connected but outside the setup. It will not participate until you assign it a location.

A beam can also remain assigned while excluded from the current throwing direction's timing sequence. By default, receiving-end tee and back-line beams do not become hot, so a draw does not need to reach them to finish. Enable the far tee/back-line option in **Settings** when you want to include those positions, such as for hit-speed practice. The yellow-and-purple readiness pattern applies to the beams participating in the current throw.

## Choose an arming mode

Use the three-part arming control on the **SmartBeam** tab. The text above it shows the selected mode. You can also choose the mode in **Settings → System Arming**.

| Mode | How you get ready for the next rock |
| --- | --- |
| **Manual** | Tap **Arm** for each throw. |
| **Automatic** | The system re-arms after each throw and a configurable delay. |
| **First Beam** | Best for solo practice: sliding back to the hack breaks the first beam and re-arms the system automatically. |

### Manual

1. Select **Manual**. Assigned beams show <span class="led-colour" data-led-colour="blue">blue</span> while idle and disarmed.
2. With the beams clear, tap **Arm**.
3. Wait for **READY**. The first beam shows <span class="led-colour" data-led-colour="yellow">yellow</span> and the other waiting beams show <span class="led-colour" data-led-colour="purple">purple</span>. Deliver the rock.
4. When the throw is complete, tap **Arm** again when you are ready for the next one.

Arming does not start a stopwatch immediately. The system waits for the first beam to be broken.

### Automatic

Set the re-arming delay in **Settings → System Arming**. Choose enough time to prepare the next rock and clear the beams.

During the countdown, the system-state LEDs flash <span class="led-colour" data-led-colour="orange">orange</span> rapidly. Once armed, the first beam shows solid <span class="led-colour" data-led-colour="yellow">yellow</span> and the other waiting beams show <span class="led-colour" data-led-colour="purple">purple</span>.

Select **Automatic**, then tap **Arm** to start the cycle. After a completed throw or a timeout, the system shows **ARMING**, waits for the configured delay, and arms again.

Tap **Disarm** while waiting for a rock or during the re-arming delay to stop the cycle. During a throw, tap **Cancel**. Changing the beam setup, throwing direction, or arming mode also stops the cycle; tap **Arm** to start it again.

If a beam is blocked when the delay ends, arming fails. Clear or realign it and check the status. If the system has returned to **IDLE**, tap **Arm** to restart; if it shows **ARMING**, another attempt is pending.

### First Beam

**First Beam is best for solo practice.** As you slide back to the hack for your next delivery, you break the first beam and start the arming countdown automatically. You can prepare for the next throw without returning to your phone or having someone else tap **Arm**.

Use a setup with a beam near the throwing end so you can reach it before returning to the hack. The first beam is determined by the selected throwing direction.

1. Select **First Beam**.
2. While the system is idle, the near control beam shows <span class="led-colour" data-led-colour="teal">teal</span>, meaning it will arm the system when tripped. Briefly interrupt it, for example as you slide back toward the hack.
3. Clear the beam before the **two-second arming countdown** ends. Its system-state LEDs flash <span class="led-colour" data-led-colour="orange">orange</span> rapidly during the countdown. All beams used for the throw must be established when it finishes.
4. Wait for **READY**. The first beam shows solid <span class="led-colour" data-led-colour="yellow">yellow</span>, with other waiting beams <span class="led-colour" data-led-colour="purple">purple</span>. Deliver the rock through the setup.
5. After the throw, briefly interrupt the first beam again to prepare for the next rock.

The interruption that starts the countdown is an arming command; the subsequent rock starts the timed throw. You can also use the app's **Arm** button.

With a single-beam setup, the system pauses for **five seconds** after a timing cycle before accepting another beam-triggered arming command. Its system-state LEDs flash <span class="led-colour" data-led-colour="blue">blue</span> during **PAUSED**, then return to <span class="led-colour" data-led-colour="teal">teal</span> when it is ready to accept the next arming command.

## Understand the status

| Status | Meaning | System-state LEDs |
| --- | --- | --- |
| **IDLE** | The system is waiting to be armed. | Assigned beams are <span class="led-colour" data-led-colour="blue">blue</span>; in First Beam mode, the near control beam is <span class="led-colour" data-led-colour="teal">teal</span>. |
| **ARMING** | An arming countdown is running. Wait for **READY**. | Rapid <span class="led-colour" data-led-colour="orange">orange</span> flashes on the beams counting down. |
| **READY** | The system is armed and waiting for the first beam break. | First beam <span class="led-colour" data-led-colour="yellow">yellow</span>; other waiting beams <span class="led-colour" data-led-colour="purple">purple</span>. |
| **ACTIVE** | A throw is being timed. | Next beam <span class="led-colour" data-led-colour="yellow">yellow</span>; the beam being crossed changes <span class="led-colour" data-led-colour="red">red</span> → <span class="led-colour" data-led-colour="green">green</span>. |
| **PAUSED** | The single-beam First Beam pause is running. | <span class="led-colour" data-led-colour="blue">Blue</span> flashes on the control beam. |

The hardware also indicates readiness and timing progress. See [LED Indication](led-indication.md) for the colours and patterns.

## Disarm or cancel

Tap **Disarm** before a rock starts, or **Cancel** while timing, to abandon the current throw. Cancellation does not save that throw's measurements; previous throws remain in History.

Cancellation produces brief, rapid <span class="led-colour" data-led-colour="red">red</span> flashes. Assigned units then return to <span class="led-colour" data-led-colour="blue">blue</span>, with the near control beam returning to <span class="led-colour" data-led-colour="teal">teal</span> in First Beam mode after any single-beam pause.

You can also disarm or cancel by holding the near control beam broken for **two seconds** while the system is ready or timing. This control is available in all three modes when a suitable beam is placed near the throwing end. Clear the beam before arming again.

In First Beam mode, a later brief interruption can start a new countdown. Switch to **Manual** if you want to leave the system idle while moving equipment or collecting rocks.

## If the throw does not finish

The system can wait indefinitely for the first beam break after arming. Once timing starts, it times out if the rock does not reach a later expected beam, or if the final beam stays blocked too long.

On a timeout, the system-state LEDs briefly flash <span class="led-colour" data-led-colour="red">red</span> rapidly. Measurements already completed are saved to History; missing measurements may be absent. Automatic mode then starts its re-arming delay with <span class="led-colour" data-led-colour="orange">orange</span> flashes. If you want to discard the current throw instead, use **Cancel** before it times out.

Check the beam alignment, assigned positions, and throwing direction before trying again. A rock stopping short of a later beam can also cause a timeout.
