# Robotin Network – System Architecture

## Overview
Robotin Network is a decentralized data collection network focused on embodied intelligence.
The system coordinates distributed collector nodes to perform physical-world tasks
(e.g. object manipulation, cleaning-related actions) and produces structured, high-quality
training data for embodied AI models.

This document describes the system architecture and module boundaries.

---

## Core Components

### 1. Data Collection Client
- Runs on mobile app or embedded device
- Responsible for:
  - Receiving task definitions
  - Executing physical-world tasks
  - Capturing raw sensor and interaction data
- Examples of data:
  - RGB / depth frames
  - Action sequences
  - Task metadata

---

### 2. Task Orchestration Service
- Central service that manages task lifecycle
- Responsibilities:
  - Define task schema and constraints
  - Assign tasks to eligible collector nodes
  - Track task status (created / accepted / completed)

---

### 3. Data Ingestion Layer
- Handles data uploads from collector nodes
- Responsibilities:
  - Receive raw data
  - Generate hashes and metadata
  - Store data in off-chain storage

---

### 4. Data Validation & Quality Scoring
- Ensures data usability and basic integrity
- Responsibilities:
  - Rule-based validation (format, duration, completeness)
  - Compute a basic quality score
- Note:
  - Advanced ML-based validation is planned for future phases

---

### 5. Incentive & Reward Logic
- Calculates rewards based on:
  - Task type
  - Data quality score
- Outputs reward events that can be settled on-chain
- Hackathon version focuses on off-chain calculation and simulation

---

### 6. Storage Layer
- Off-chain storage:
  - Raw data (videos, sensor logs)
- On-chain (planned):
  - Task metadata
  - Data hashes
  - Reward settlement records

---

## Planned Tech Stack

- Client: Mobile App / Embedded Device
- Backend: Node.js or Python
- Storage: Cloud Object Storage / IPFS (planned)
- Blockchain: Solana or EVM-compatible chain (planned)

---

## Hackathon Scope

During the hackathon, we aim to:
- Define and implement a minimal task schema
- Build a mock task orchestration flow
- Simulate data ingestion and quality scoring
- Demonstrate reward calculation logic (off-chain)

Full device integration and on-chain settlement are out of hackathon scope.
