# Project HERA

**HERA — Humanoid Evaluation for Robotic Assembly** is a master's research and engineering project evaluating the feasibility of using a commercially available humanoid robot for overhead bin installation in aircraft final assembly.

## Current Planning Reference

The project scope, phases, milestones, and current status are maintained in the [HERA Development Roadmap](HERA_Development_Roadmap.md).

## Scope

- Characterize the overhead bin installation task.
- Define and apply a humanoid-selection methodology.
- Select a commercial humanoid platform.
- Build a representative aircraft assembly scene in NVIDIA Isaac Sim.
- Assess kinematic feasibility and technical limitations.
- Perform an engineering financial assessment.

The project selects and applies an existing humanoid platform; it does not develop a new robot from scratch.

## Repository Layout

Directories will be created when they contain project material. This avoids empty placeholders and keeps the repository easy to navigate.

| Path | Purpose |
|---|---|
| `docs/` | Requirements, technical decisions, methods, and project documentation |
| `references/` | Reference metadata and permitted supporting material |
| `models/` | Approved robot and environment model files |
| `simulation/` | Isaac Sim scenes, scripts, and configuration |
| `experiments/` | Reproducible experiment definitions and run records |
| `results/` | Reviewed figures, tables, and summarized results |
| `thesis/` | Thesis source and qualification material |

## Working Conventions

- Keep `main` in a reviewable state.
- Use short-lived branches named `feature/<topic>`, `docs/<topic>`, `simulation/<topic>`, or `experiment/<topic>`.
- Write concise commits in the imperative form, for example: `Define preliminary payload criteria`.
- Record the source, date, configuration, units, and limitations of technical data.
- Keep experiment inputs, software versions, assumptions, and results traceable.
- Do not commit credentials, private keys, confidential industrial data, or unapproved proprietary files.

## Data Handling

Aircraft CAD and other industrial data must be classified before storage. Confidential or access-restricted material must not be committed to this repository unless the repository, access controls, and data owner explicitly permit it. Use approved controlled storage for restricted assets and keep only non-sensitive metadata or references here when necessary.

| Classification | Repository rule |
|---|---|
| Public | Commit only when publication or redistribution is permitted. |
| Internal | Use only in approved private project storage. |
| Restricted | Keep outside Git unless the data owner explicitly approves the repository and users. |
| Confidential | Keep in owner-approved controlled storage; commit only non-sensitive references or metadata. |

No project license has been assigned. Do not assume that repository content or third-party assets may be redistributed.
