# Product Design Specification (PDS)

_Living document - update as requirements evolve._

## Mission
A stable flying quadcopter with accurate hover and movement, intended to serve as the platform for further data collection and experiments with minimal interference and resonance.
 
## Performance Requirements
| # | Requirement | Target | Priority | Rationale |
|---|---|---|---|---|
| R01 | Hover stability | ±1.5 m | Must | Position-hold tolerance bounded by available indoor test space; baseline until control-loop data justifies tightening. |
| R02 | Flight time | 10 min | Should | Used for the propulsion calc; sets the battery capacity floor and defines a usable test window per charge cycle. |
| R03 | Attitude stability | ±2° | Should | Bounds the vibration/noise floor the IMU must tolerate; kept loose until arm resonance (R13) and control tuning are decided. |
| R04 | Thrust-to-weight ratio | 3:1 design, 2:1 minimum floor | Must | 3:1 gives margin for wind rejection (R06) and payload growth (R05) [aim]; 2:1 is the minium needed for sustainable hover. |
| R05 | Max payload capacity | 500 g | Should | Sized for planned sensor/data-collection payloads without pushing past AUW limits (R09). |
| R06 | Wind tolerance | Stable hover in ≤5 m/s wind | Should | Matches expected outdoor conditions for occasional Slovakia countryside flights; indoor sessions are unaffected. |
| R07 | Frame diameter | TBD, pending Decision #1 | Must | Coupled to prop diameter (R08) by the non-overlap constraint - adjacent arms must clear spinning props; also sets arm length feeding into R13. |
| R08 | Prop diameter | TBD, pending Decision #1 | Must | Coupled to frame diameter (R07) by the same non-overlap constraint; driven by the propulsion momentum-theory sizing calc. |
| R09 | All-up weight (AUW) | ≤3.5 kg maximum | Must | Budget and motor-class ceiling; keeps the T/W floor (R04) achievable without over-sized, over-budget motors. |
| R10 | Arm swap time | <5 min with basic tools | Should | Supports rapid iteration between arm material/design variants during the test phase without specialist tooling. |
| R11 | Arm swap recalibration | No FC recalibration required | Should | Keeps arm swaps mechanical-only so resonance/vibration comparisons across variants aren't confounded by re-tuned control gains. |
| R12 | Arm-clamp interface | Two dowel pins per modular interface | Must | Locked decision - dowel pins carry shear/alignment load so clamp bolts only carry preload, keeping arm swaps (R10/R11) repeatable without shifting axis alignment. |
| R13 | Arm resonance frequency | TBD, f₁ ≥ 1.5× max motor mechanical frequency, pending propulsion calc | Must | Standard vibration-isolation margin to avoid resonant coupling with motor-order harmonics and other sensor interferance. |
| R14 | Battery | 6S LiPo, 22.2V nominal | Must | Voltage class sized to the motor/ESC selection needed for target T/W (R04) at the target AUW (R09). |
| R15 | Power connector | XT60 | Must | Standard connector for 6S packs in this current range; ensures charger/ESC compatibility with headroom for potential overcurrents or future boost mode implementation. |

## Constraints
- Budget: ≤£700
- Time phrame: Flying in 10 weeks 
- Material: PLA only initially (PETG, CNC eventual)
- Regulation: Indoor flight, designated RC zone or Slovakia Countryside
- Safety: LiPo charging supervision required, indoor flight preferred for initial tests
- Test equipment: thrust stand, blackbox logging, no oscilloscope
- Software: FC must support bidirectional DShot + blackbox, software pillar on ESP32 or Pi 5
- Tools: torque driver required for bolt preload logging

## Assumptions
- FDM 3D printer access is assumed for all initial PLA parts; CNC access is assumed only for the later PETG/CNC phase and is not yet confirmed.
- A 6S-capable balance charger is assumed available for LiPo charging; not yet purchased or confirmed.
- Day-to-day flight testing is assumed to happen indoors or in a local designated RC zone; Slovakia countryside flights are occasional , not the primary test venue.
- Test equipment (thrust stand, blackbox logging) is assumed self-built/sourced within the £700 budget; no lab-grade instrumentation (e.g. oscilloscope) is assumed available.
