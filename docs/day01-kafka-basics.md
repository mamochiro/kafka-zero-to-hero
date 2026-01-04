# Day 1 – Kafka Basics

⏱ **Time**: 15–30 minutes  
🎯 **Goal**: Understand *what Kafka is*, *why it exists*, and its *core concepts*.

---

## 1️⃣ What Problem Does Kafka Solve?

Modern systems often need to:
- Handle **high traffic**
- Process events **asynchronously**
- Avoid tight coupling between services
- Scale consumers independently

Traditional approaches:
- Direct HTTP calls → tightly coupled
- Database polling → slow & inefficient
- Message queues → limited scalability

👉 **Kafka solves this with event streaming**.

---

## 2️⃣ What Is Apache Kafka?

**Apache Kafka** is a **distributed event streaming platform** used to:
- Publish events
- Store events
- Process events in real time

Kafka is commonly used for:
- Event-driven architectures
- Microservices communication
- Log aggregation
- Stream processing

> Think of Kafka as a **durable, scalable, distributed commit log**.

---

## 3️⃣ Core Kafka Concepts (Must Know)

### 🔹 Broker
- A Kafka **server**
- Stores data and serves clients
- A Kafka cluster has **multiple brokers**

---

### 🔹 Topic
- A **category / stream** of events  
- Examples:
  - `order-created`
  - `payment-completed`

Topics are **append-only**.

---

### 🔹 Partition
- Topics are split into **partitions**
- Each partition is an **ordered log**
- Enables **parallelism & scalability**

Example:
```
order-created
├── partition-0
├── partition-1
└── partition-2
```

yaml
Copy code

⚠️ Order is guaranteed **only within a partition**.

---

### 🔹 Offset
- A **position** of a message in a partition
- Offset is **per partition**

partition-0: offset 0, 1, 2, 3

yaml
Copy code

Kafka does **not** delete messages after reading.

---

### 🔹 Producer
- Application that **writes messages** to Kafka
- Chooses topic & partition (directly or via key)

---

### 🔹 Consumer
- Application that **reads messages** from Kafka
- Reads messages **by offset**

---

### 🔹 Consumer Group
- A group of consumers sharing work
- Each partition is consumed by **only one consumer per group**

Topic (3 partitions)
Consumer Group (3 consumers)
→ 1 partition per consumer

yaml
Copy code

---

## 4️⃣ Kafka vs Traditional Queue

| Feature | Kafka | Traditional Queue |
|------|------|------------------|
| Message retention | Yes | No |
| Replay messages | Yes | No |
| Multiple consumers | Yes | Limited |
| Ordering | Per partition | Global |
| Scalability | Very high | Medium |

---

## 5️⃣ When NOT to Use Kafka

Kafka is **not** a silver bullet ❌

Avoid Kafka when:
- You need **simple request/response**
- Low traffic, small system
- Strong transactional guarantees only
- You don’t need event replay

---

## 6️⃣ Mental Model (Important 🧠)

- Kafka **does not push** messages
- Consumers **pull** messages
- Kafka does **not track consumers**
- Consumers track their **own offsets**

---

## ✅ Day 1 Checklist

- [ ] I understand what Kafka solves
- [ ] I know broker, topic, partition, offset
- [ ] I understand producer vs consumer
- [ ] I know when Kafka is NOT needed

---

## 🔜 Next: Day 2

➡️ **Day 2 – Local Kafka Setup with Docker (KRaft mode)**