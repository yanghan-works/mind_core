---
tags: 
alias: 
date: 2025-08-03 08:32
---

**上层地图**: [[PostgreSQL MOC]]

---

> 这里是如何让 PostgreSQL 飞驰起来的知识。从索引的原理到查询计划的解读，再到高级的调优策略。

---

## 索引策略与类型 (Index Strategies & Types)

*索引是提升查询性能最直接有效的工具。*

- [[什么是数据库索引？]]

- [[CREATE INDEX]]

- [[B-Tree 索引]]

- [[PostgreSQL 其他索引类型 (Hash, GiST, GIN)]]

- [[部分索引 (Partial Index)]]  <-- (高价值补充)

- [[表达式/函数索引 (Expression/Functional Index)]] <-- (高价值补充)

- [[覆盖索引 (Covering Index)]] <-- (高价值补充)

- [[多列索引与列顺序]] <-- (高价值补充)


## 查询分析与调优 (Query Analysis & Tuning)

*工欲善其事，必先利其器。这里是诊断和解决性能问题的工具与方法。*

- [[EXPLAIN 与 EXPLAIN ANALYZE - 解读查询计划]]

- [[PostgreSQL 统计信息的重要性]] <-- (建议补充)

- [[慢查询定位]]

- [[查询重写技巧]] <-- (建议补充)

- [[避免全表扫描 (Full Table Scan)]]

- [[VACUUM, ANALYZE - 数据库维护]]

- [[配置参数调优 (postgresql.conf)]] <-- (建议补充)