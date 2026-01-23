# Robotin Network – Data Flow

This document describes the end-to-end data flow for a single data collection task.

---

## Step 1: Task Creation
- Platform defines a data collection task
- Task includes:
  - task_id
  - task_type (e.g. object manipulation)
  - expected data format
  - base reward

(Implemented during hackathon: task schema definition)

---

## Step 2: Task Assignment
- Task is assigned to an available collector node
- Collector reviews and accepts the task via client

(Mocked during hackathon)

---

## Step 3: Task Execution & Data Capture
- Collector performs the physical-world task
- Client records:
  - Sensor data
  - Action timestamps
  - Task metadata

(Planned – simulated inputs during hackathon)

---

## Step 4: Data Upload
- Collected data is uploaded to off-chain storage
- System generates:
  - Data hash
  - Upload metadata

(Mocked during hackathon)

---

## Step 5: Data Validation
- System performs basic validation:
  - File format checks
  - Minimum duration
  - Required fields
- Validation result produced

(Implemented with rule-based checks during hackathon)

---

## Step 6: Quality Scoring
- A simple quality score is calculated
- Score is based on predefined rules (e.g. completeness)

(Implemented during hackathon)

---

## Step 7: Reward Calculation
- Reward amount is calculated using:
  - Base reward
  - Quality score multiplier
- Reward event is recorded

(Implemented off-chain during hackathon)

---

## Step 8: Data Availability
- Validated data is indexed
- Data becomes available for downstream model training and analysis

(Planned)

---

## Notes on Hackathon Implementation
- Device-level data collection is simulated
- Focus is on:
  - Data pipeline structure
  - Validation logic
  - Incentive mechanism
- Architecture is designed to scale to real devices post-hackathon
