# USB Table

| Technical Name                          | Max Speed | Max Power (Std/PD)*                 | Common Connectors          |
|-----------------------------------------|-----------|-------------------------------------|----------------------------|
| USB 1.1                                 | 12 Mbps   | 2.5W (5V, 0.5A)                     | Type-A, Type-B             |
| USB 2.0                                 | 480 Mbps  | 2.5W (5V, 0.5A)                     | Type-A, B, Mini, Micro     |
| USB 3.0 (aka 3.1 Gen 1, 3.2 Gen 1)      | 5 Gbps    | 4.5W (5V, 0.9A) / Up to 100W w/ PD  | Type-A, B, Micro-B, Type-C |
| USB 3.1 Gen 2 (aka 3.2 Gen 2x1)         | 10 Gbps   | 100W (w/ PD)                        | Type-A, Type-C             |
| USB 3.2 Gen 2x2                         | 20 Gbps   | 100W (w/ PD)                        | Type-C ONLY                |
| USB4 (Gen 2x2)                          | 20 Gbps   | 100W - 240W (PD 3.1)                | Type-C ONLY                |
| USB4 (Gen 3x2)                          | 40 Gbps   | 100W - 240W (PD 3.1)                | Type-C ONLY                |
| USB4 v2.0                               | 80 Gbps   | 240W (PD 3.1)                       | Type-C ONLY                |

> [!NOTE]
> This table is about ports (male/female), not cables. Most cables have USB 2.0 speed with USB-C male connectors.


### Pin (The Physical Limit):

- USB-A (3.0) has 9 pins.
- USB-C has 24 pins.

### Power Delivery:

- USB-A is usually limited to low power (typically max 4.5W–12W standard; some proprietary phone cables exceed this limit).
- New laptops can support up to 60W, 100W, or 240W. At high voltages, negotiation requires "communication pins," which are only found in the USB-C connector.

### Basic Adapter Operation

- USB-C Charger: Does not supply power (0V) until it detects a connected device. It waits for a signal.
- Micro-USB Port: Is passive. It expects to receive 5V immediately without requesting anything.
- Detection: When you insert the USB-C cable into the adapter, the USB-C charger "probes" the CC pin.
- The Trick: Instead of finding a smart chip, the charger finds a 5.1kΩ resistor connecting the CC pin to Ground (GND).
- The Signal: This specific resistor tells the charger: "Hey, I'm a legacy device that needs standard 5V."
- Activation: The charger unlocks power (5V) on the VBUS pins.
- Charging: The Micro-USB phone receives the 5V and starts charging.

    
 ```
 ┌───────────────────┐                                  ┌───────────────────┐
 │  USB-C Socket     │             ADAPTER              │  Micro-USB Plug   │
 │  (Female)         │             INTERNAL             │  (Male)           │
 ├───────────────────┼──────────────────────────────────┼───────────────────┤
 │                   │                                  │                   │
 │  VBUS (Power) ────┼───> Direct Connection ───────────┼──> Pin 1 (VCC 5V) │
 │                   │                                  │                   │
 │  GND (Ground)─────┼───> Direct Connection ───────────┼──> Pin 5 (GND)    │
 │                   │                                  │                   │
 │  D+ (Data) ───────┼───> Direct Connection ───────────┼──> Pin 3 (D+)     │
 │                   │                                  │                   │
 │  D- (Data) ───────┼───> Direct Connection ───────────┼──> Pin 2 (D-)     │
 │                   │                                  │                   │
 │  Pin CC1 / CC2    │      ┌──[ Resistor ]────┐        │  (Pin 4 ID)       │
 │  (Config Channel) ├────>─┤ 5.1kΩ (Pull-Down)├───┐    │  (Not connected   │
 │                   │      └──────────────────┘   │    │   or grounded)    │
 │                   │                             ▼    │                   │
 │                   │                          To GND  │                   │
 └───────────────────┴──────────────────────────────────┴───────────────────┘
```
