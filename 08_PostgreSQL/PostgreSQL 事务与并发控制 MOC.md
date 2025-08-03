---
tags: 
alias: 
date: 2025-08-03 08:32
---

**上层地图**: [[PostgreSQL MOC]]

---

> 理解事务与并发，是区分“会用数据库”和“精通数据库”的分水岭。这里是保证数据一致性的内功心法与实战招式。

---

## 核心理论 (Core Theory)

*这里是数据库保证数据一致性的底层基石与规则。*

- [[ACID 属性]]

- [[BEGIN, COMMIT, ROLLBACK]]

- [[事务隔离级别 (Transaction Isolation Levels)]]

- [[MVCC (多版本并发控制)]]

- [[锁 (Locking)]]

    - [[行级锁 (Row-level Lock)]]

    - [[表级锁 (Table-level Lock)]]

    - [[死锁 (Deadlock)]]

## 实践与应用模式 (Practical Application & Patterns)

*这里是理论在应用开发中的具体体现和常用解决方案。*

- [[SELECT ... FOR UPDATE / FOR SHARE (显式锁定)]]

- [[悲观锁 vs 乐观锁]]

- [[事务重试与幂等性]]

- [[Advisory Locks (建议锁)]]