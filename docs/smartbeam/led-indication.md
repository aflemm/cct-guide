---
icon: lucide/lightbulb
---

# LED Indication

SmartBeam uses separate LEDs for the beam itself, battery charging, and the timing system state.

## Where to look

![SmartBeam with labels identifying the beam state, system state, and charging state LEDs](../assets/images/smartbeam/led-locations.jpg)

- **Beam state:** an arrow-shaped LED pointing down the top of the unit, within the top light-bar.
- **System state:** LEDs at the two ends of the top light-bar.
- **Charging state:** an LED shining through a small hole on the side, directly above the USB port.

## Beam state LED

The arrow-shaped LED always indicates the state of that unit's beam.

| LED colour | Beam state |
| --- | --- |
| <span class="led-colour" data-led-colour="red">Red</span> | Beam broken. |
| <span class="led-colour" data-led-colour="green">Green</span> | Beam established. |

This is separate from the system-state LEDs: the arrow shows the beam state, while the ends of the light-bar show connection and timing states.

## Charging state LED

The LED above the USB port shows <span class="led-colour" data-led-colour="orange">orange</span> while charging and <span class="led-colour" data-led-colour="green">green</span> when full. See [Charging](charging.md#read-the-charging-light) for the full indication table and USB power instructions.

## System-state LEDs

The LEDs at the ends of the top light-bar indicate the following states.

### Connection and readiness

| LED indication | Meaning |
| --- | --- |
| Flashing <span class="led-colour" data-led-colour="white">white</span> | Searching for a Bluetooth connection. |
| Solid <span class="led-colour" data-led-colour="white">white</span> | Connected, but not included in the beam setup. |
| Solid <span class="led-colour" data-led-colour="yellow">yellow</span> | Hot beam: the next expected beam break. |
| Solid <span class="led-colour" data-led-colour="blue">blue</span> | Idle and disarmed. |
| Solid <span class="led-colour" data-led-colour="purple">purple</span> | Idle and armed. |
| Solid <span class="led-colour" data-led-colour="teal">teal</span> | The system will arm when the beam is tripped. |

### Timing and countdowns

| LED indication | Meaning |
| --- | --- |
| <span class="led-colour" data-led-colour="red">Red</span> | Beam broken during timing. |
| <span class="led-colour" data-led-colour="green">Green</span> | Beam complete during timing. |
| Rapid <span class="led-colour" data-led-colour="orange">orange</span> flashes | Arming countdown. |
| <span class="led-colour" data-led-colour="blue">Blue</span> flashes for about five seconds | Paused countdown. |
| Brief rapid <span class="led-colour" data-led-colour="red">red</span> flashes | Timing cancelled or timed out. |
| Dim <span class="led-colour" data-led-colour="purple">purple</span> alternating between the two system-state LEDs | Firmware transfer in progress, on firmware with update-light support. See [Firmware Updates](firmware-updates.md). |

### Identification and low battery

| LED indication | Meaning |
| --- | --- |
| Brief, rapid random-colour pattern | Identifying the device. |
| <span class="led-colour" data-led-colour="red">Red</span> flashes before shutdown | Battery depleted; the unit is about to shut down. |

## Related topics

- [Arming and Timing](arming-and-timing/index.md)
- [Charging](charging.md)
- [Connecting](connecting-smartbeam.md)

