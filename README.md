# SmartSpace Agent

SmartSpace Agent is a platform concept for autonomous whole-home intelligence across phones, IoT devices, wearables, in-car systems, and cloud services.

This repository contains the public-facing project brief, architecture notes, and a short application summary for token plan submissions.

## Overview

Traditional smart home products are still dominated by fixed rules, isolated device control, and short command-response interactions. They can switch on lights or execute simple automations, but they struggle with real user intent such as:

- "I am heading home, make the room comfortable."
- "The child is asleep, keep everything quiet."
- "Power usage has been abnormal lately, find the cause."

These requests require context fusion across time, location, weather, device status, occupancy, energy records, user preferences, and safety rules. SmartSpace Agent is designed to solve that gap through long-chain reasoning, multi-agent orchestration, and closed-loop execution.

## Core Pain Points

1. Smart home control is fragmented across apps, devices, and rule engines.
2. Existing assistants have weak scene understanding and limited memory.
3. Complex tasks require cross-device planning rather than single-turn answers.
4. Energy, comfort, and safety decisions often conflict and need trade-off reasoning.
5. Feedback from execution results is rarely written back into a persistent preference model.

## Core Workflow

SmartSpace Agent follows a closed loop:

1. Environment sensing
2. Intent understanding
3. Home state modeling
4. Long-chain reasoning
5. Task planning
6. Multi-agent execution
7. Feedback and memory update

The system ingests device telemetry, sensor events, schedules, location updates, power usage, and past interactions. A triage agent detects the user's goal, a digital twin agent builds the current home state, a reasoning agent ranks possible actions, a planner decomposes tasks, execution agents call device APIs, and a safety agent enforces policy and privacy boundaries. A summary agent then records outcomes and updates preference memory.

## Multi-Agent Roles

- `Intent Agent`: classifies user goals, urgency, and target scenes.
- `Digital Twin Agent`: constructs the current household state graph.
- `Reasoning Agent`: performs long-chain analysis and candidate ranking.
- `Planner Agent`: breaks goals into executable subtasks.
- `Execution Agent`: invokes device control and service APIs.
- `Safety Agent`: checks permissions, privacy, and abnormal behavior.
- `Memory Agent`: writes outcomes back into long-term user preference memory.

## Example Scenarios

### Energy Optimization

The system balances weather, occupancy, room temperature, tariff periods, and device power profiles to generate a low-energy comfort plan instead of using fixed automations.

### Elderly Care

The system combines door sensors, motion sensors, wearable signals, and abnormal activity patterns to estimate risk levels and trigger graded notifications.

### Car-to-Home Continuity

The system predicts arrival time from route context and prepares lighting, HVAC, hot water, and access control accordingly.

## Why This Needs Large Token Capacity

This project is a strong fit for high token quota because it requires:

- long-context household state modeling
- multi-agent concurrent orchestration
- multi-modal reasoning over text, telemetry, and event streams
- policy-aware planning and verification
- continuous evaluation and memory updates

## Repository Contents

```text
smartspace-agent/
  README.md
  LICENSE
  .gitignore
  docs/
    architecture.md
    project-brief-zh.md
    token-plan-application-zh.md
```

## Status

This repository is a polished project concept and documentation package suitable for public publishing, proposal review, and token plan application support.
