# Assignment 2: Relational Model Constraints

## Introduction

In this module, we learned about relational model constraints. This assignment applies these concepts to the **Car Dealership** relational database schema.

The database is designed to keep track of automobile sales in a car dealership.

### Car Dealership Schema Diagram

![Car Dealership Relational Database Schema](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork/DB0101EN-SkillsNetwork/labs/Assignment%202/images/Module1_Car_Schema.png)

## Question 1: Identify the primary key of the relation `Car`.

**Answer:** The primary key of the `Car` relation is `Serial_No` (Serial Number).

## Question 2: Identify the foreign key of the relation `Sale`.

**Answer:** The foreign keys of the `Sale` relation are `Serial_No` and `Salesperson_ID`.

- `Serial_No` references the `Car` relation.
- `Salesperson_ID` references the `Salesperson` relation.

## Question 3: How many constraint types are there in the relation `Sale`?

**Answer:** There are **2 types of constraints** in the `Sale` relation:

1. **Primary Key Constraint**
2. **Foreign Key Constraint**
