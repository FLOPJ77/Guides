# Ethernet Cable (Cat5 to Cat8)

A quick-reference guide comparing the most common twisted-pair Ethernet cable categories, their maximum speeds, bandwidth frequencies, and typical use cases.

---

## Comparison Table

| Category | Max Speed | Max Bandwidth (Frequency) | Max Distance at Top Speed | Common Shielding | Typical / Recommended Use |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Cat5** | 100 Mbps | 100 MHz | 100 m (328 ft) | UTP (Unshielded) | **Obsolete.** Legacy phone/slow network systems. |
| **Cat5e** | 1 Gbps (1,000 Mbps) | 100 MHz | 100 m (328 ft) | UTP | Basic home networks, older office installs, smart TVs/consoles. |
| **Cat6** | 10 Gbps (up to 55m)<br>1 Gbps (up to 100m) | 250 MHz | 55 m @ 10 Gbps<br>100 m @ 1 Gbps | UTP or STP | Standard modern home/office wiring, Gigabit internet. |
| **Cat6a** | 10 Gbps | 500 MHz | 100 m (328 ft) | STP / FTP (usually shielded) | **Best all-rounder for new runs.** 10G LAN, NAS, future-proofing. |
| **Cat7** | 10 Gbps | 600 MHz | 100 m (328 ft) | S/FTP (Fully Shielded) | Proprietary standard. High EMI industrial environments. *(Generally skip for home/office).* |
| **Cat7a** | 10 Gbps (40G/50m unofficial) | 1,000 MHz (1 GHz) | ~50 m (high speed) | S/FTP (Fully Shielded) | Industrial setups. Mostly bypassed in favor of Cat6a or Cat8. |
| **Cat8** | 25 Gbps / 40 Gbps | 2,000 MHz (2 GHz) | **30 m (98 ft)** | S/FTP (Fully Shielded) | Data centers, server-to-switch links, very short high-speed runs. |

---

## Shielding Types (What the Acronyms Mean)

Shielding prevents **EMI (Electromagnetic Interference)** and crosstalk between pairs.

* **UTP (Unshielded Twisted Pair):** No foil or braiding. Flexible, cheap, standard for Cat5e and most Cat6.
* **FTP (Foiled Twisted Pair):** Pairs are wrapped together in an outer foil shield.
* **STP (Shielded Twisted Pair):** Individual pairs wrapped in foil.
* **S/FTP (Shielded Foiled Twisted Pair):** Each pair is individually wrapped in foil, plus an overall braided wire shield around all pairs. (Standard on Cat7/Cat8; thick, stiff, and requires proper grounding).

---

## Quick Rules of Thumb & Recommendations

1. **For standard home networking & gaming:** 
   * **Cat6** is the sweet spot: cheap, flexible, supports up to 10 Gbps over shorter domestic runs (< 55m).
2. **For running cables inside walls / future-proofing:** 
   * **Cat6a** is the gold standard: full 10 Gbps across the entire 100-meter range with better resistance to crosstalk.
3. **Why avoid Cat7 for normal setups?**
   * Cat7 was never officially recognized by the TIA/EIA standard committee. It uses strict grounding requirements, is very stiff, and many cheap "Cat7" cables online are counterfeit.
4. **Is Cat8 overkill?**
   * Yes, for 99% of home users. Cat8 is limited to **30 meters** and designed specifically for short-distance rack connections in enterprise data centers.
5. **Connector Compatibility:**
   * All categories (Cat5 to Cat8) use the standard **RJ45** connector form factor. However, thicker cables (Cat6a, Cat7, Cat8) require larger gauge RJ45 ends and proper crimping tools if terminating yourself.
