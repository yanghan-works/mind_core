---
tags: 
alias: 
date: 2025-08-03 08:31
---

**上层地图**: [[PostgreSQL MOC]]

---

## 查询的逻辑处理顺序  <-- (新增)
> `SELECT` 语句的执行并非按照其书写顺序。理解这个逻辑顺序是精通 SQL 的关键。
> (FROM -> WHERE -> GROUP BY -> HAVING -> SELECT -> DISTINCT -> ORDER BY -> LIMIT)

- [[SQL 查询的逻辑处理流程]]

---

## 核心查询子句 (Core Query Clauses)

- [[SELECT ... FROM ...]]

- [[WHERE - 数据过滤]]

- [[ORDER BY - 结果排序]]

- [[LIMIT 与 OFFSET - 分页查询]]

- [[JOINs - 连接查询]]

    - [[INNER JOIN]]

    - [[LEFT JOIN / RIGHT JOIN]]

    - [[FULL OUTER JOIN]]

    - [[CROSS JOIN]]

- [[GROUP BY - 分组]]

- [[聚合函数 (Aggregate Functions) - COUNT, SUM, AVG, MAX, MIN]]

- [[HAVING - 分G组后过滤]]

- [[UNION 与 UNION ALL - 结果集合并]]

---

## 高级查询模式 (Advanced Query Patterns) <-- (新增)

- [[Subquery - 子查询]]

- [[CASE 表达式]]

- [[公共表表达式 (CTE - Common Table Expressions)]]

- [[窗口函数 (Window Functions)]]

- [[递归查询 (Recursive Queries)]]