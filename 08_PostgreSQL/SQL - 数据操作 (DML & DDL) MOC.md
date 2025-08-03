---
tags: 
alias: 
date: 2025-08-03 08:32
---

**上层地图**: [[PostgreSQL MOC]]

---

> 这里是数据库的“建造”与“装潢”指南，包含了用于塑造数据结构和内容的命令。

---

## 数据操纵语言 (DML)

*用于操作、改变表中的数据。*

- [[INSERT INTO - 插入数据]]

    - [[INSERT ... ON CONFLICT (UPSERT)]] <-- (高价值补充)

- [[UPDATE ... SET - 更新数据]]

- [[DELETE FROM - 删除数据]]

- [[TRUNCATE TABLE - 清空表]]

- [[RETURNING 子句]]  <-- (高价值补充)


## 数据定义语言 (DDL)

*用于定义、修改数据库对象的结构。*

- [[CREATE SCHEMA - 创建模式]]

- [[CREATE TABLE - 创建表]]

    - *包含组件: [[数据类型 (Data Types)]] (交叉链接)*

    - *包含组件: [[约束 (Constraints)]] (交叉链接)*

    - *包含组件: [[序列 (Sequences)]] (交叉链接)*

- [[ALTER TABLE - 修改表结构]]

- [[DROP TABLE - 删除表]]

- [[视图 (Views)]]

- [[索引 (Indexes)]]  <-- (建议交叉链接)