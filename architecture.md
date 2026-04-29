# Architecture Notes

## System Layers

### 1. Perception Layer

Inputs include:

- device telemetry
- room sensors
- geolocation and route status
- calendar and schedule signals
- power and energy logs
- historical user interactions

### 2. State Layer

The digital twin maintains a structured graph for:

- rooms
- devices
- occupants
- environmental state
- routines
- safety constraints

### 3. Reasoning Layer

The reasoning layer runs:

- intent classification
- context retrieval
- long-chain causal analysis
- candidate action ranking
- conflict resolution between comfort, safety, and efficiency

### 4. Planning Layer

The planner converts user goals into executable tasks with dependency ordering, fallback logic, and policy checks.

### 5. Execution Layer

Execution agents call external services and device APIs, monitor outcomes, and retry or escalate when actions fail.

### 6. Learning Layer

Outcome summaries, explicit feedback, and observed acceptance patterns are written into a long-term preference model.

## Example Decision Path

User says: "I will be home in 20 minutes. Prepare the house but keep power usage reasonable."

The platform may:

1. estimate arrival time from route data
2. read current indoor temperature and air quality
3. check occupancy status
4. inspect tariff period and recent power usage
5. decide HVAC target values
6. stage lighting and curtain changes
7. keep noisy devices off if quiet mode is active
8. log final actions and user feedback

## Design Goal

The goal is not only voice control or routine execution. The goal is autonomous, policy-aware, explainable orchestration across a living environment.
