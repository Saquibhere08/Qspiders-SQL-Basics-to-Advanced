# Oracle SQL Learning Guide (Basics to Advanced)

## 📘 Introduction

This guide will help you learn Oracle SQL step by step, from beginner
concepts to advanced techniques.

------------------------------------------------------------------------

## 🟢 Basics

### 1. What is SQL?

Structured Query Language used to interact with databases.

### 2. Basic SELECT

``` sql
SELECT * FROM EMP;
```

### 3. Filtering Data

``` sql
SELECT * FROM EMP WHERE SAL > 1000;
```

### 4. Sorting

``` sql
SELECT * FROM EMP ORDER BY SAL DESC;
```

------------------------------------------------------------------------

## 🟡 Intermediate

### 5. Functions

-   Single-row: UPPER, LOWER, INSTR

``` sql
SELECT INSTR(ENAME,'A') FROM EMP;
```

### 6. Aggregate Functions

``` sql
SELECT AVG(SAL), MAX(SAL) FROM EMP;
```

### 7. GROUP BY

``` sql
SELECT DEPTNO, AVG(SAL) FROM EMP GROUP BY DEPTNO;
```

### 8. Joins

``` sql
SELECT E.ENAME, D.DNAME
FROM EMP E
JOIN DEPT D ON E.DEPTNO = D.DEPTNO;
```

------------------------------------------------------------------------

## 🔴 Advanced

### 9. Subqueries

``` sql
SELECT * FROM EMP WHERE SAL > (SELECT AVG(SAL) FROM EMP);
```

### 10. Analytic Functions

``` sql
SELECT ENAME, SAL, RANK() OVER (ORDER BY SAL DESC) FROM EMP;
```

### 11. Indexes

``` sql
CREATE INDEX emp_idx ON EMP(ENAME);
```

### 12. Views

``` sql
CREATE VIEW emp_view AS SELECT * FROM EMP;
```

------------------------------------------------------------------------

## 🚀 Practice Tips

-   Use SQL\*Plus or Oracle Live SQL
-   Practice daily queries
-   Work on real datasets

------------------------------------------------------------------------

## 📚 Resources

-   Oracle Documentation
-   LeetCode SQL Problems
-   HackerRank SQL

------------------------------------------------------------------------

Happy Learning! 🎯
