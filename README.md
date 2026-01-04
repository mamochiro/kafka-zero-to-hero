# Kafka Zero → Hero 🚀

Learn Apache Kafka from **zero to production-ready basics** in **14 days**
with **15–30 minutes per day**, using **Go (Golang)**.

## Goals
- Understand Kafka fundamentals
- Build producers & consumers in Go
- Learn consumer groups, retry, DLQ
- Run Kafka locally with Docker
- Use Kafka UI for debugging

## Tech Stack
- Apache Kafka (KRaft mode)
- Go (kafka-go)
- Docker & Docker Compose
- Kafka UI

## Structure
```
kafka-zero-to-hero/
├── cmd/ # Executable applications
│ ├── producer/
│ └── consumer/
├── internal/ # Reusable Kafka logic
│ ├── kafka/
│ └── model/
├── docs/ # Daily learning notes
├───── day01-kafka-basics.md
├───── day02-installation.md
├───── day03-topics-partitions.md
├── docker/ # Kafka & Kafka UI setup
├── examples/ # Focused Kafka examples
├── README.md
└── go.mod
```


## Progress
- [x] Day 1 – Kafka Basics
- [ ] Day 2 – Local Setup
- [ ] Day 3 – Topics & Partitions
- [ ] Day 4 – Producer
- [ ] Day 5 – Consumer
- [ ] Day 6 – Consumer Groups
- [ ] Day 7 – Rebalance
- [ ] Day 8 – Delivery Semantics
- [ ] Day 9 – Retry & DLQ
- [ ] Day 10 – Schema
- [ ] Day 11 – Performance
- [ ] Day 12 – Security
- [ ] Day 13 – Kafka UI
- [ ] Day 14 – Mini Project


## 🚀 How to Start

```bash
git clone https://github.com/<your-username>/kafka-zero-to-hero.git
cd kafka-zero-to-hero
go mod tidy