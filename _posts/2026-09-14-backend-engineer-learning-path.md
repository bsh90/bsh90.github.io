---
layout: post
title:  "Backend engineer learning Path"
date:   2026-09-14
categories: software development concepts
---

🔴 Critical
1. Database fundamentals
2. Transactions & concurrency
3. Algorithms + Big-O
4. Java internals
5. HTTP/networking
6. Linux/system fundamentals
7. System design/scalability

🟠 Important
1. Authentication/security
2. Spring internals
3. Database performance
4. Architecture
5. Observability
6. CI/CD
7. Cloud fundamentals

🟡 Later
1. Kafka/event-driven architecture
2. Redis/caching
3. Kubernetes
4. Terraform/IaC
5. Advanced distributed systems
6. NoSQL

**Phase 1 — Computer science + Java foundations** <br>
Weeks 1–6

~7 hours/week

Learn:

Java
- Collections
- HashMap internals
- ArrayList internals
- equals/hashCode
- Generics
- JVM memory
- Stack vs heap
- Garbage collection
- Exceptions
- Streams
- Lambdas
- Optional
- CompletableFuture
- Virtual threads
  
Computer science <br>
- Big-O
- Arrays
- Hash tables
- Linked lists
- Stacks
- Queues
- Trees
- Heaps
- Graphs
- Binary search
- Sorting

Your objective is:

Understand why the data structure/algorithm works and what its performance characteristics are.

**Phase 2 — Databases** <br>
Weeks 7–12

This should be one of your highest priorities.

Learn PostgreSQL concepts even though you currently use MS SQL; the concepts transfer extremely well.

Topics:

- SQL
- JOIN
- GROUP BY
- HAVING
- Subqueries
- CTEs
- Window functions
- UNION
- EXISTS

Then:

- Database internals
- Tables
- Pages
- Rows
- Indexes
- B-tree
- Composite indexes
- Query planner
- Execution plan

Then:

Performance

Learn to use:

- EXPLAIN
- EXPLAIN ANALYZE

and understand:

- Sequential scan
- Index scan
- Nested loop
- Hash join
- Sort

This will directly build on the performance optimization you've already done.

**Phase 3 — Transactions & concurrency** <br>
Weeks 13–16

This is extremely important for you because you've already encountered a real deadlock.

Learn:

- ACID
- Transactions
- Locks
- Row locks
- Page locks
- Table locks
- Isolation levels
- MVCC
- Deadlocks
- Optimistic locking
- Pessimistic locking

Then reproduce problems yourself.

Once you can deliberately create this locally and understand why it happens, your understanding will jump significantly.

**Phase 4 — HTTP + networking** <br>
Weeks 17–20

This is another major gap.

Study:

- DNS
- TCP
- TLS
- HTTP
- HTTP/1.1
- HTTP/2
- HTTP/3
- Keep-alive
- Connection pooling
- Proxies
- Reverse proxies
- Load balancing

You should eventually be able to explain: "What happens when I call my REST endpoint?" at a surprisingly deep level.

**Phase 5 — Spring Boot internals** <br>
Weeks 21–24

You already have 3/5 Spring Boot, so don't spend months learning basic Spring.

Instead learn what's underneath:

- IoC
- Dependency Injection
- ApplicationContext
- Bean lifecycle
- Bean scopes
- Proxies
- AOP
- @Transactional
- Spring Security
- Configuration
- Auto-configuration

Understanding proxies and transaction boundaries will make your existing knowledge much stronger.

**Phase 6 — Linux + production** <br>
Weeks 25–28

The gap is more specifically:

Linux system administration and operating-system concepts.

Learn:

- Processes
- Threads
- CPU
- Memory
- File descriptors
- Sockets
- Ports
- Signals
- Permissions
- systemd
- Networking

Then learn to diagnose:

Problem A

Java application CPU = 100%

Problem B

Java application memory keeps increasing

Problem C

Application can't connect to database

Problem D

API suddenly has 10× latency

This is where your debugging skills become senior-level skills.

**Phase 7 — Security** <br>
Weeks 29–31

Learn:

- Authentication
- Authorization
- Sessions
- Cookies
- JWT
- OAuth2
- OpenID Connect
- RBAC
- Password hashing
- CSRF
- CORS
- HTTPS
- Secrets
- OWASP Top 10

Then specifically apply it in Spring Security.

**Phase 8 — Architecture + system design** <br>
Weeks 32–38

Now we start moving toward senior-level thinking.

Learn:

- Layered architecture
- Modular monolith
- Microservices
- DDD basics
- Bounded contexts
- Dependency inversion
- Coupling
- Cohesion

Then:

- Load balancing
- Horizontal scaling
- Caching
- Database replication
- Read replicas
- Partitioning
- Sharding
- Queues
- Async processing
- Rate limiting

Then practice designing systems.

Start simple:

Design 1

URL shortener

↓

Design 2

Notification service

↓

Design 3

File upload service

↓

Design 4

Order processing system

↓

Design 5

Large-scale e-commerce backend

**Phase 9 — Distributed systems** <br>
Weeks 39–44

Only now would I go deep into:

- CAP
- Consistency
- Availability
- Partition tolerance
- Replication
- Leader/follower
- Consensus
- Eventual consistency
- Distributed transactions
- Idempotency
- Retries
- Timeouts
- Circuit breakers
- Backpressure
- Message ordering
- Exactly-once vs at-least-once

This is where Kafka becomes much easier to understand.

**Phase 10 — Cloud + infrastructure** <br>
Weeks 45–52

Pick one cloud.

For an enterprise Java career, I'd suggest AWS or Azure, depending on what companies around you use.

Learn the concepts first:

- Compute
- Networking
- IAM
- Load balancers
- DNS
- Object storage
- Managed databases
- Containers
- Secrets
- Monitoring
- Autoscaling

You want to understand why Kubernetes exists before learning all its commands.

**Reference:** ChatGPT
