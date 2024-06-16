---
author: Pratham Dupare
title: FOSS Alternatives
date: 2022-07-25
description:
keywords: ["alternative", "FOSS", "contact"]
type: alternative
---

## Users Table

```markdown
| Column        | Type         | Description            |
| ------------- | ------------ | ---------------------- |
| user_id       | INT          | Primary Key            |
| username      | VARCHAR(255) | Unique                 |
| email         | VARCHAR(255) | Unique                 |
| password_hash | VARCHAR(255) | Hashed password        |
| profile_pic   | VARCHAR(255) | URL to profile picture |
| summary       | TEXT         | Profile summary        |
```

### Skills Table

```markdown
| Column   | Type         | Description          |
| -------- | ------------ | -------------------- |
| skill_id | INT          | Primary Key          |
| user_id  | INT          | Foreign Key to Users |
| name     | VARCHAR(255) | Skill name           |
| level    | VARCHAR(50)  | Skill proficiency    |
```

### Work Experience Table

- Separated company and role details into their respective tables to eliminate redundancy.
- Added company_id and role_id foreign keys.

```markdown
| Column        | Type | Description                    |
| ------------- | ---- | ------------------------------ |
| experience_id | INT  | Primary Key                    |
| user_id       | INT  | Foreign Key to Users           |
| company_id    | INT  | Foreign Key to Companies       |
| role_id       | INT  | Foreign Key to Roles           |
| start_date    | DATE | Start date                     |
| end_date      | DATE | End date (NULL if current job) |
| description   | TEXT | Job description                |
```

### Education Table

```markdown
| Column       | Type         | Description             |
| ------------ | ------------ | ----------------------- |
| education_id | INT          | Primary Key             |
| user_id      | INT          | Foreign Key to Users    |
| institution  | VARCHAR(255) | Name of the institution |
| degree       | VARCHAR(255) | Degree                  |
| start_date   | DATE         | Start date              |
| end_date     | DATE         | End date                |
| description  | TEXT         | Description of studies  |
```

### Projects Table

```markdown
| Column       | Type         | Description          |
| ------------ | ------------ | -------------------- |
| project_id   | INT          | Primary Key          |
| user_id      | INT          | Foreign Key to Users |
| title        | VARCHAR(255) | Project title        |
| description  | TEXT         | Project description  |
| start_date   | DATE         | Start date           |
| end_date     | DATE         | End date             |
| technologies | VARCHAR(255) | Technologies used    |
| url          | VARCHAR(255) | URL to project       |
```

### Companies Table

```markdown
| Column       | Type         | Description         |
| ------------ | ------------ | ------------------- |
| company_id   | INT          | Primary Key         |
| company_name | VARCHAR(255) | Name of the company |
```

### Roles Table

```markdown
| Column     | Type         | Description              |
| ---------- | ------------ | ------------------------ |
| role_id    | INT          | Primary Key              |
| company_id | INT          | Foreign Key to Companies |
| role       | VARCHAR(255) | Job role                 |
```

## Example Data Entries

**Users Table:**

```markdown
| user_id | username | email            | password_hash           | profile_pic          | summary               |
| ------- | -------- | ---------------- | ----------------------- | -------------------- | --------------------- |
| 1       | john_doe | john@example.com | $2a$12$abcdef1234567890 | /images/john_pic.jpg | Experienced developer |
| 2       | jane_doe | jane@example.com | $2a$12$ghijkl4567890123 | /images/jane_pic.jpg | Backend developer     |
```

**Skills Table:**

```markdown
| skill_id | user_id | name       | level        |
| -------- | ------- | ---------- | ------------ |
| 1        | 1       | JavaScript | Advanced     |
| 2        | 1       | React      | Intermediate |
| 3        | 2       | Python     | Advanced     |
```

**Companies Table:**

```markdown
| company_id | company_name |
| ---------- | ------------ |
| 1          | ABC Corp     |
| 2          | XYZ Inc      |
```

**Roles Table:**

```markdown
| role_id | company_id | role         |
| ------- | ---------- | ------------ |
| 1       | 1          | Frontend Dev |
| 2       | 2          | Backend Dev  |
```

**Work Experience Table:**

```markdown
| experience_id | user_id | company_id | role_id | start_date | end_date   | description               |
| ------------- | ------- | ---------- | ------- | ---------- | ---------- | ------------------------- |
| 1             | 1       | 1          | 1       | 2018-01-01 | 2020-06-30 | Developed user interfaces |
| 2             | 2       | 2          | 2       | 2019-02-01 | 2023-05-15 | Backend development       |
```

**Education Table:**

```markdown
| education_id | user_id | institution    | degree   | start_date | end_date   | description              |
| ------------ | ------- | -------------- | -------- | ---------- | ---------- | ------------------------ |
| 1            | 1       | XYZ University | B.Sc. CS | 2014-08-01 | 2018-05-15 | Studied Computer Science |
| 2            | 2       | ABC University | M.Sc. CS | 2015-09-01 | 2017-07-30 | Specialized in AI        |
```

**Projects Table:**

```markdown
| project_id | user_id | title         | description         | start_date | end_date   | technologies       | url                      |
| ---------- | ------- | ------------- | ------------------- | ---------- | ---------- | ------------------ | ------------------------ |
| 1          | 1       | Portfolio App | Created a portfolio | 2021-01-01 | 2021-03-01 | React, Node.js     | https://myportfolio.com/ |
| 2          | 2       | AI Project    | Developed AI system | 2020-06-01 | 2020-09-01 | Python, TensorFlow | https://aiproject.com/   |
```

This normalized schema reduces redundancy, ensures data integrity, and maintains clear relationships between different entities.
