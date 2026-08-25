# Design Calculations

## Given Specifications

| Parameter | Value |
|---|---:|
| Input Voltage (Vin) | 24 V |
| Output Voltage (Vo) | 12 V |
| Switching Frequency (fs) | 20 kHz |
| Rated Output Power | 24 W |
| Inductor Current Ripple | 20% |
| Output Voltage Ripple | 10% |

## 1. Duty Ratio

For an ideal buck converter:

D = Vo / Vin

D = 12 / 24 = 0.5

Therefore, the required duty ratio is **50%**.

## 2. Load Resistance

R = Vo² / Po

R = 12² / 24

R = 6 Ω

Therefore, the equivalent load resistance is **6 Ω**.

## 3. Average Output/Inductor Current

Io = Po / Vo

Io = 24 / 12

Io = 2 A

For continuous conduction mode:

IL(avg) = Io = 2 A

## 4. Inductor Current Ripple

Given inductor current ripple = 20%:

ΔIL = 0.20 × 2

ΔIL = 0.4 A

## 5. Inductor Selection

For a buck converter:

L = [(Vin - Vo)D] / [ΔIL × fs]

L = [(24 - 12)(0.5)] / [(0.4)(20000)]

L = 750 μH

Therefore, the calculated minimum inductance is approximately **750 μH**.

## 6. Output Capacitor

Given output voltage ripple = 10%:

ΔVo = 0.10 × 12

ΔVo = 1.2 V

For an ideal capacitor:

ΔVo = ΔIL / (8fsC)

Therefore:

C = ΔIL / (8fsΔVo)

C = 0.4 / [8 × 20000 × 1.2]

C ≈ 2.08 μF

Therefore, the calculated minimum capacitance is approximately **2.08 μF**.

## Design Summary

- Duty ratio: **50%**
- Load resistance: **6 Ω**
- Average inductor current: **2 A**
- Inductor current ripple: **0.4 A**
- Calculated inductance: **750 μH**
- Calculated minimum capacitance: **2.08 μF**
