# Quadcopter Project

**Status:** In progress | **Phase:** Specification complete, entering analysis | **Week 2 of 10**

## Overview
A quadcopter designed and built from scratch, documenting the full engineering process - calculations, trade studies, CAD, manufacturing, and testing.

The mission: a stable flying quadcopter with accurate hover and movement, intended to serve as a platform for further data collection and experiments with minimal interference and resonance.

## The goal
I will design, build and deeply document a quadcopter of substantial scale with heavy emphasis on first-principles derivation.

Each design decision is grounded in closed-form first-principles analysis - from momentum-theory propulsion sizing to Euler-Bernoulli cantilever resonance - with every prediction validated against experimental measurement.

## Headline requirements
Full spec with rationale: [PDS](00-specification/PDS.md) | Progress against spec: [requirements tracking](00-specification/requirements-tracking.md)

| Requirement | Target |
|---|---|
| Thrust-to-weight ratio | 3:1 design, 2:1 minimum floor |
| All-up weight | ≤ 3.5 kg |
| Flight time | 10 min |
| Max payload | 500 g |
| Arm resonance | f₁ ≥ 1.5× max motor frequency |
| Arm swap | < 5 min, no FC recalibration |
| Power system | 6S LiPo (22.2 V), XT60 |

**Constraints:** ≤ £700 budget · flying in 10 weeks · PLA first, PETG/CNC later · indoor + designated RC zone testing

## Structure
| Folder | Contents |
|---|---|
| `logbook/` | Weekly running log + per-session notes |
| `00-specification/` | PDS and requirements tracking |
| `01-calculations/` | Engineering calculations (typed + handwritten) |
| `02-trade-studies/` | Design decisions with justification |
| `03-cad/` | Source files, drawings, renders |
| `04-manufacture/` | BOM, build photos, assembly notes |
| `05-testing/` | Thrust stand, vibration, flight logs, test vs prediction |
| `06-failure-log/` | Running failure analysis log |
| `07-flight-controller/` | Custom firmware (optional pillar) |
| `08-final-report/` | Final technical report and risk assessment |
| `media/` | Video milestones |

## Where it's at
- **Done:** repo structure, first-draft PDS with 15 quantified requirements, feasibility discussion with researchers at Imperial College London
- **Now:** propulsion momentum-theory sizing; frame diameter vs prop size trade study (Decision #1)
- **Next:** motor/ESC selection, arm resonance calc, first CAD

---
*Part of my engineering portfolio - [alfred-leigh.co.uk](https://alfred-leigh.co.uk) | See also: [72V enduro e-motorcycle build](https://github.com/a365l/enduro-emotorcycle-build)*
