# Robotin Network

Robotin Network is a decentralized data collection network designed to produce
high-quality embodied intelligence training data from real-world physical tasks.

The system coordinates distributed collector nodes, defines structured tasks,
validates collected data, and calculates incentives based on data quality.

This repository contains the initial system design and hackathon implementation
for the Robotin Network data pipeline.

---

## Problem

Embodied AI systems require large volumes of high-quality, diverse, real-world
interaction data. However, existing data collection pipelines are:

- Centralized and expensive
- Hard to scale across real environments
- Poorly aligned with data quality incentives

Robotin Network addresses this by introducing a decentralized, task-based
data collection and validation framework.

---

## Solution Overview

Robotin Network provides:

- A task orchestration layer for physical-world data collection
- A standardized data schema for embodied tasks
- A validation and quality scoring pipeline
- A reward calculation mechanism aligned with data quality

The architecture is designed to support future on-chain settlement and
large-scale device deployment.

---

## System Architecture

High-level architecture and module breakdown can be found here:

- [`/docs/architecture.md`](./docs/architecture.md)

End-to-end data flow for a single task is described here:

- [`/docs/data-flow.md`](./docs/data-flow.md)

---

## Hackathon Scope

During the hackathon, this project focuses on building a **minimal but complete
data pipeline**, including:

- Task schema definition
- Mock task assignment flow
- Simulated data ingestion
- Rule-based data validation
- Quality scoring and reward calculation (off-chain)

Out of scope for the hackathon:

- Full device integration
- On-chain reward settlement
- Large-scale model training

---

## Planned Tech Stack

- Backend: Node.js or Python
- Storage: Cloud Object Storage / IPFS (planned)
- Blockchain: Solana or EVM-compatible chain (planned)
- Client: Mobile App / Embedded Device (simulated during hackathon)

---

## Repository Structure

```text
.
├── README.md
├── docs/
│   ├── architecture.md
│   └── data-flow.md
├── backend/        # Planned
├── contracts/      # Planned
└── frontend/       # Planned
```

---

## Development Status

- System architecture: Defined
- Data flow: Defined
- Hackathon implementation: In progress
- Active development will take place during the hackathon

---

## Team

Robotin Network is built by a team focused on embodied intelligence, robotics, and decentralized data networks.

---

## License

MIT License (subject to change)
