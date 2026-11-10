# HERA Development Roadmap

| Field | Value |
|---|---|
| Project | HERA — Humanoid Evaluation for Robotic Assembly |
| Document | Development Roadmap |
| Version | 0.4 |
| Initial date | November 10, 2026 |
| Status | Draft — Initial Planning |

## 1. Purpose

HERA will evaluate whether a commercially available humanoid robot can perform overhead bin installation in aircraft final assembly. The project covers task characterization, robot selection, NVIDIA Isaac Sim development, kinematic assessment, and an engineering financial assessment. Designing a new robot is outside the current scope.

Simulation results will demonstrate **kinematic feasibility** only within the documented model and assumptions. **Industrial feasibility** also requires evidence on dynamics, manipulation reliability, stability, safety, cycle time, integration, maintainability, and economics.

## 2. Current Status

**Status date:** November 10, 2026

Use only: **Not Started**, **In Progress**, **Blocked**, or **Completed**.

| Phase | Development Phase | Period | Status | Next gate |
|---|---|---|---|---|
| DP1 | Application Characterization and Selection Criteria | Nov 10–24, 2026 | Not Started | Criteria review |
| DP2 | Project Planning and Simulation Setup | Nov–Dec 2026 | In Progress | Development plan submission |
| DP3 | Humanoid Platform Selection | Jan–Feb 2027, preliminary | Not Started | Platform selection |
| DP4 | Simulation Environment Development | Feb–May 2027, preliminary | Not Started | Integrated simulation scene |
| DP5 | Qualification Preparation | May–Jul 2027, preliminary | Not Started | Master's qualification |
| DP6 | Kinematic and Feasibility Assessment | After qualification; to be defined | Not Started | Feasibility and financial assessment |
| DP7 | Thesis Consolidation | To be defined | Not Started | Thesis submission |

DP1 and DP2 proceed in parallel. Early Isaac Sim training and CAD investigation do not depend on final robot selection.

## 3. Development Phases

### DP1 — Application Characterization and Selection Criteria

**Objective:** Define the technical and operational requirements used to evaluate humanoid robots for overhead bin installation.

#### Task checklist

**DP1.1 — Characterize the installation task**

- [ ] Define the task boundary, start and end conditions, and representative operational sequence.
- [ ] Record available dimensions, masses, loads, centers of mass, tolerances, and cycle-time context.
- [ ] Describe the work height, floor, access path, obstacles, clearances, and approach directions.
- [ ] Identify tools, fixtures, interfaces, human assistance, and environmental constraints.
- [ ] Separate verified data, sourced estimates, assumptions, and missing information.

**DP1.2 — Define preliminary robot requirements**

- [ ] Define payload and load-handling requirements, including external support assumptions.
- [ ] Define reach, workspace, robot-size, stance, and access requirements.
- [ ] Identify necessary degrees of freedom, joint ranges, and posture constraints.
- [ ] Define manipulation needs: grasping, bimanual operation, tooling, and end-effector compatibility.
- [ ] Identify preliminary stability, positioning, repeatability, speed, and control needs.

**DP1.3 — Classify the criteria**

- [ ] Separate mandatory pass/fail feasibility requirements from comparative selection criteria.
- [ ] Define the evidence needed to assess each mandatory requirement.
- [ ] Flag unclassified criteria and possible double-counting for DP3 resolution.

**DP1.4 — Survey commercial platforms**

- [ ] Create a candidate list supported by evidence of commercial availability.
- [ ] Collect relevant specifications with source, date, configuration, and units.
- [ ] Distinguish manufacturer claims from independently demonstrated capabilities where possible.
- [ ] Record missing specifications and simulation-model availability.

#### Deliverables

- Basic task characterization with assumptions and information gaps.
- Preliminary, technically justified selection criteria.
- Initial feasibility-gate and comparative-criteria classification.
- Traceable candidate-platform survey.

#### Complete when

- The task sequence, environment, loads, spatial constraints, and information gaps are documented.
- The preliminary criteria cover payload, reach, dimensions, degrees of freedom, joints, manipulation, and stability.
- Mandatory requirements and comparative criteria are separated.
- Candidate data are traceable and the criteria review actions are recorded.

DP1 does not include final weights, candidate scoring, or the complete multicriteria method; these belong to DP3.

#### Dependencies

Available task data, operational knowledge, drawings, and confidentiality rules. Missing data may be represented by clearly labeled assumptions.

### DP2 — Project Planning and Simulation Setup

**Objective:** Establish the working infrastructure, begin practical simulation training, investigate CAD integration, and produce the formal master's development plan.

#### Task checklist

**DP2.1 — Project infrastructure**

- [x] Define and implement the local folder structure.
- [x] Define naming, version-control, branch, commit, and review conventions.
- [x] Define technical-decision, requirement, source, and experiment records.
- [x] Define public, internal, restricted, and confidential data-handling rules.
- [ ] Create the GitHub repository and Google Drive workspace only after access and storage rules are approved.

Confidential aircraft CAD must not be placed in a public repository or unrestricted cloud storage.

**DP2.2 — Isaac Sim training, November 16–22, 2026**

- [ ] Confirm software access and basic hardware compatibility.
- [ ] Load and inspect an existing articulated robot model.
- [ ] Exercise joint control, reference frames, and collision visualization.
- [ ] Run and document one small repeatable kinematic experiment.
- [ ] Record software versions, setup issues, and learning resources.

This training uses an available robot model and does not wait for DP3.

**DP2.3 — Aircraft CAD integration**

- [ ] Inventory available geometry, formats, scale, coordinates, ownership, and access restrictions.
- [ ] Define the minimum geometry needed for the representative task.
- [ ] Investigate conversion to OpenUSD-compatible assets.
- [ ] Assess simplification, mesh reduction, scene partitioning, and proxy collision geometry.
- [ ] Test a non-confidential representative asset when practical.

URDF and SDF describe robots or articulated simulation systems. OpenUSD represents the Isaac Sim scene. Aircraft geometry does not need to be converted to URDF or SDF when an OpenUSD-compatible scene asset is appropriate.

**DP2.4 — Computing infrastructure**

- [ ] Inventory the available GPU, memory, storage, operating system, and drivers.
- [ ] Compare them with the requirements of the planned Isaac Sim deployment.
- [ ] Assess acceptable remote workstation or cloud options if needed.
- [ ] Record licensing, remote-access, data-transfer, and confidentiality constraints.

**DP2.5 — Master's development plan**

- [ ] Define the research objective, scope, questions, and feasibility boundary.
- [ ] Describe the planned selection, simulation, kinematic, and financial methods.
- [ ] Include phases, deliverables, resources, risks, and qualification planning.
- [ ] Submit through the applicable academic process.

#### Deliverables

- Organized project infrastructure and working conventions.
- Documented initial Isaac Sim experiment.
- Preliminary CAD integration strategy.
- Computing and access assessment.
- Formal master's development plan.

#### Complete when

- Project organization and data-handling rules are documented.
- An articulated robot has been exercised in Isaac Sim with a repeatable record.
- A plausible OpenUSD integration and geometry-simplification route is documented.
- Required computing access is identified.
- The master's development plan is submitted.

#### Dependencies

Isaac Sim and computing access, available CAD-format information, data-handling approval, and available DP1 findings. Drafting may proceed using labeled assumptions while DP1 remains active.

### DP3 — Humanoid Platform Selection

**Objective:** Select and justify a commercial humanoid platform.

**Main activities:**

- Develop a multicriteria method using AHP or another justified approach.
- Define criteria, feasibility gates, weights, scoring, evidence rules, and uncertainty treatment.
- Evaluate candidates and perform appropriate consistency or sensitivity checks.
- Select a platform or document that no candidate passes the mandatory requirements.

**Deliverable:** Reproducible selection method and technically justified platform decision.

**Complete when:** The method, evidence, evaluation, uncertainties, and decision are documented and reviewable.

**Dependencies:** DP1 requirements and candidate data; DP2 simulation and computing constraints.

### DP4 — Simulation Environment Development

**Objective:** Build a representative Isaac Sim environment and integrate the selected humanoid.

**Main activities:**

- Prepare, simplify, and import the required aircraft geometry.
- Build the overhead bin installation scene.
- Integrate the humanoid and configure articulation, frames, and collision geometry.
- Define initial kinematic verification cases.

**Deliverable:** Reproducible simulation scene containing the aircraft workspace and selected humanoid.

**Complete when:** Scale, coordinates, articulation, frames, and collisions are verified and initial checks can be repeated.

**Dependencies:** DP1 task definition, DP2 CAD strategy, and DP3 platform selection. Aircraft-scene work may begin before DP3 is complete.

### DP5 — Qualification Preparation

**Objective:** Consolidate the selection method, simulation scene, and qualification materials.

**Main activities:**

- Consolidate technical decisions, assumptions, limitations, and results.
- Prepare the qualification report and presentation.
- Perform a preliminary kinematic demonstration if sufficiently mature.

**Deliverable:** Qualification materials supported by the selection method and simulation scene.

**Complete when:** Materials are submitted and the qualification event is completed.

**Dependencies:** DP3 and adequate DP4 maturity.

The supervisor's stated minimum expectation is an established humanoid-selection methodology and a constructed simulation scene. A preliminary kinematic demonstration is desirable, not mandatory.

### DP6 — Kinematic and Feasibility Assessment

**Objective:** Assess kinematic feasibility, technical limitations, and engineering financial implications.

**Main activities:**

- Simulate representative task cases.
- Evaluate reachability, joint constraints, collision avoidance, and task execution.
- Identify limitations and test important assumptions where practical.
- Estimate relevant investment and operating costs.
- Compare with the current process when sufficient data are available.

**Deliverable:** Simulation results, technical feasibility assessment, and engineering financial analysis.

**Complete when:** Cases and assumptions are reproducible, conclusions stay within the evidence boundary, and financial sources and uncertainty are documented.

**Dependencies:** Qualification outcome, mature simulation environment, and sufficient technical and economic data.

### DP7 — Thesis Consolidation

**Objective:** Consolidate the research into the final thesis and supporting documentation.

**Main activities:**

- Integrate the methodology, results, limitations, and contributions.
- Complete traceability from requirements to conclusions.
- Finalize and submit the thesis and required supporting material.

**Deliverable:** Final master's thesis and associated project deliverables.

**Complete when:** The required documents are submitted through the academic process.

**Dependencies:** Completed research assessments, supervisor review, and the academic schedule.

## 4. Milestones

| ID | Milestone | Target date | Phase | Status | Notes |
|---|---|---|---|---|---|
| M1 | Robot Selection Criteria Review | 2026-11-24 | DP1 | Not Started | Review preliminary requirements, criteria, and evidence gaps. |
| M2 | Master's Development Plan Submission | December 2026 | DP2 | Not Started | Exact date to be confirmed. |
| M3 | Master's Qualification | July 2027 | DP5 | Not Started | Exact date to be confirmed. Minimum expectation is defined in DP5. |

## 5. Decision Log

| Date | ID | Decision | Basis |
|---|---|---|---|
| 2026-11-10 | D1 | Study overhead bin installation using an existing commercial humanoid. | Project scope |
| 2026-11-10 | D2 | Use Miotto's 2023 work as inspiration, without automatically reusing its criteria or weights. | Method constraint |
| 2026-11-10 | D3 | Run DP1 and DP2 in parallel and train in Isaac Sim before platform selection. | Schedule constraint |
| 2026-11-10 | D4 | Develop final criteria weights and the complete selection method in DP3. | Phase boundary |
| 2026-11-10 | D5 | Keep kinematic-feasibility claims separate from industrial-feasibility claims. | Research validity |
| 2026-11-10 | D6 | Require the selection method and constructed scene for qualification; treat an early demonstration as desirable. | Supervisor expectation |

## 6. Roadmap Maintenance

- Update the status table, milestone table, and relevant checklist when evidence changes.
- Mark work **Completed** only when its completion criteria are met.
- Record material scope or method changes in the decision log.
- Keep verified facts and assumptions distinct.

This roadmap will be updated progressively as the project advances.

## 7. Revision History

| Version | Date | Summary |
|---|---|---|
| 0.1 | 2026-11-10 | Initial roadmap. |
| 0.2 | 2026-11-10 | Condensed the roadmap, removed repeated content, and emphasized current status and next actions. |
| 0.3 | 2026-11-10 | Removed the continuous activities, upcoming actions, open questions, and risk register sections. |
| 0.4 | 2026-11-10 | Started DP2 and recorded the local repository conventions and data-handling rules. |
