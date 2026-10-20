---
icon: lucide/timer
---

# Arming Modes

Choose how you want to prepare for each throw. Use the three-part arming control on the **SmartBeam** tab, or open **Settings → System Arming**. The text above the control shows the selected mode.

Before delivering, check the [readiness lights](arming-and-timing/timing-lights-and-status.md#how-to-know-the-system-is-ready). The colours below refer to the system-state LEDs at the ends of the top light-bar.

## Manual

1. Select **Manual**. Assigned beams show <span class="led-colour" data-led-colour="blue">blue</span> while idle and disarmed.
2. With the beams clear, tap **Arm**.
3. Wait for **READY** and the [yellow-and-purple readiness pattern](arming-and-timing/timing-lights-and-status.md#how-to-know-the-system-is-ready), then deliver the rock.
4. When the throw is complete, tap **Arm** again when you are ready for the next one.

## Automatic

Set the re-arming delay in **Settings → System Arming**. Choose enough time to prepare the next rock and clear the beams.

During the countdown, the system-state LEDs flash <span class="led-colour" data-led-colour="orange">orange</span> rapidly. Wait for **READY** and the yellow-and-purple readiness pattern before delivering.

Select **Automatic**, then tap **Arm** to start the cycle. After a completed throw or a timeout, the system shows **ARMING**, waits for the configured delay, and arms again.

To stop the cycle, see [Cancelling and Timeouts](cancelling-and-timeouts.md#disarm-or-cancel). Changing the beam setup, throwing direction, or arming mode also stops it; tap **Arm** to start again.

If a beam is blocked when the delay ends, arming fails. Clear or realign it and check the status. If the system has returned to **IDLE**, tap **Arm** to restart; if it shows **ARMING**, another attempt is pending.

## First Beam

For solo practice, sliding back to the hack breaks the first beam and starts arming automatically, without returning to your phone.

Use a setup with a beam near the throwing end so you can reach it before returning to the hack. The first beam is determined by the selected throwing direction.

1. Select **First Beam**.
2. While the system is idle, the near control beam shows <span class="led-colour" data-led-colour="teal">teal</span>, meaning it will arm the system when tripped. Briefly interrupt it, for example as you slide back toward the hack.
3. Clear the beam before the **two-second arming countdown** ends. Its system-state LEDs flash <span class="led-colour" data-led-colour="orange">orange</span> rapidly during the countdown. All beams used for the throw must be established when it finishes.
4. Wait for **READY** and the yellow-and-purple readiness pattern, then deliver the rock.
5. After the throw, briefly interrupt the first beam again to prepare for the next rock.

The interruption that starts the countdown is an arming command; the subsequent rock starts the timed throw. You can also use the app's **Arm** button.

With a single-beam setup, the system pauses for **five seconds** after a timing cycle before accepting another beam-triggered arming command. Its system-state LEDs flash <span class="led-colour" data-led-colour="blue">blue</span> during **PAUSED**, then return to <span class="led-colour" data-led-colour="teal">teal</span> when it is ready to accept the next arming command.

