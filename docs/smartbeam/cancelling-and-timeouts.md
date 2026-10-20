---
icon: lucide/timer
---

# Cancelling and Timeouts

You can stop an armed system or abandon a throw. A timeout ends an incomplete throw automatically. These actions differ in whether completed measurements are saved.

The light patterns below refer to the system-state LEDs at the ends of the top light-bar. See [LED Indication](led-indication.md) for their locations.

## Disarm or cancel

Tap **Disarm** before a rock starts, or **Cancel** while timing, to abandon the current throw. Cancellation does not save that throw's measurements; previous throws remain in History.

Cancellation produces brief, rapid <span class="led-colour" data-led-colour="red">red</span> flashes. Assigned units then return to <span class="led-colour" data-led-colour="blue">blue</span>, with the near control beam returning to <span class="led-colour" data-led-colour="teal">teal</span> in First Beam mode after any single-beam pause.

You can also disarm or cancel by holding the near control beam broken for **two seconds** while the system is ready or timing. This control is available in all three modes when a suitable beam is placed near the throwing end. Clear the beam before arming again.

In [First Beam mode](arming-modes.md#first-beam), a later brief interruption can start a new countdown. Switch to **Manual** if you want to leave the system idle while moving equipment or collecting rocks.

## If the throw does not finish

The system can wait indefinitely for the first beam break after arming. Once timing starts, it times out if the rock does not reach a later expected beam, or if the final beam stays blocked too long.

On a timeout, the system-state LEDs briefly flash <span class="led-colour" data-led-colour="red">red</span> rapidly. Measurements already completed are saved to History; missing measurements may be absent. Automatic mode then starts its re-arming delay with <span class="led-colour" data-led-colour="orange">orange</span> flashes. If you want to discard the current throw instead, use **Cancel** before it times out.

Check the beam alignment, assigned positions, and throwing direction before trying again. A rock stopping short of a later beam can also cause a timeout.

See [Arming and Timing](arming-and-timing/index.md) to check readiness and follow the next throw.
