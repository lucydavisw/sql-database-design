# sql-database-design

 SQL Project

## Overview

This project demonstrates the design and implementation of a normalized relational database to support a university course registration system. It showcases my ability to translate written business rules into an Entity Relationship Diagram (ERD), define a clean relational schema, and write SQL scripts with real-world relevance to secure systems.

---

## Entity Relationship Model

This project models:

- One-to-many: `Course` → `Section`
- One-to-many: `Instructor` → `Section`
- One-to-many: `Room` → `Section`
- One-to-many: `MeetingTime` → `Section`
- Many-to-many: `Student` ↔ `Section` via `Enrollment`

The ERD was built to ensure data integrity, enforce relationships, and prevent redundancy — core principles in scalable and secure systems.

---

## Schema

```sql
Course(CourseID, CourseName)
Instructor(InstructorID, InstructorName)
Room(RoomID, Capacity)
MeetingTime(MeetingTimeID, TimeSlot)
Section(SectionID, CourseID, InstructorID, RoomID, MeetingTimeID)
Student(StudentID, StudentName)
Enrollment(StudentID, SectionID)
