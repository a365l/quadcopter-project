# Product Design Specification (PDS)

_Living document - update as requirements evolve._

## Mission
A stable flying quadcopter with accurate hover and movement, intended to serve as the platform for further data collection and experiments with minimal interference and resonance.
 
## Performance Requirements
| # | Requirement | Target | Priority |
|---|---|---|---|
| R01 | Hover stability | ±1.5 m | Must |
| R02 | Flight time | 10 min | Should |
| R03 | Attitude stability | ±2° | Should |
| R04 | Thrust-to-weight ratio | 3:1 design, 2:1 minimum floor | Must |
| R05 | Max payload capacity | 500 g | Should |
| R06 | Wind tolerance | Stable hover in ≤5 m/s wind | Should |
| R07 | Prop diameter | TBD, pending Decision #1 | Must |
| R08 | All-up weight (AUW) | ≤3.5 kg maximum | Must |
| R09 | Arm swap time | <5 min with basic tools | Should |
| R10 | Arm swap recalibration | No FC recalibration required | Should |
| R11 | Arm resonance frequency | TBD, f₁ ≥ 1.5× max motor mechanical frequency, pending propulsion calc | Must |
| R12 | Battery | 6S LiPo, 22.2V nominal | Must |
| R13 | Power connector | XT60 | Must |

## Constraints
- Budget around £700
- TODO
-
Budget: ≤£700
Time: 10 working weeks
Manufacturing: FDM in-house (PETG, mid-range printer), CNC outsourced, CF purchased pre-made
Regulatory: Slovak CAA — 3.5kg requires registration, check licence category before first flight
Safety: LiPo charging supervision required, indoor flight preferred for initial tests
Test equipment: thrust stand, blackbox logging, no oscilloscope
Software: FC must support bidirectional DShot + blackbox, software pillar on ESP32 or Pi 5
Tools: torque driver required for bolt preload logging

## Assumptions
- 
