---
title: Components installed with Career Assessment
description: Several types of components are installed with the activation of Career Assessment, including tables, user roles, and scheduled jobs.
locale: en-US
release: yokohama
product: Talent Development Core
classification: talent-development-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Career Assessment reference, Career Assessment, Talent Development, Employee Service Management]
---

# Components installed with Career Assessment

Several types of components are installed with the activation of Career Assessment, including tables, user roles, and scheduled jobs.

## System properties

|Property|Description|
|--------|-----------|
|sn\_lep.show\_exam\_guidelines|Property to show the exam guidelines pop-up before the user starts the quiz.|

## Roles installed

|Role title|Description|Contains roles|
|----------|-----------|--------------|
|sn\_exam.admin|Sets up Career Assessment application configurations.|sn\_exam.admin|
|sn\_exam.catalog\_admin|Creates and administers catalogs on Career Assessment.|sn\_exam.catalog\_admin|

## Tables installed

|Table|Description|
|-----|-----------|
|Exam Catalog \[sn\_exam\_catalog\]|Stores all catalogs created on Career Assessment.|
|Exam \[sn\_exam\_exam\]|Stores information on all exams on Career Assessment.|
|Exam Instance \[sn\_exam\_instance\]|Stores all exam instances on Career Assessment.|
|Exam Instance Attempt \[sn\_exam\_instance\_attempt\]|Stores all exam instance attempts on Career Assessment.|
|Exam Catalog Cannot Contribute \[sn\_exam\_m2m\_catalog\_cannot\_contribute\]|List of users who cannot add exams to an exam catalog on Career Assessment.|
|Exam Catalog Cannot Take \[sn\_exam\_m2m\_catalog\_cannot\_take\]|List of users who cannot attempt exams in an exam catalog on Career Assessment.|
|Exam Catalog Can Contribute \[sn\_exam\_m2m\_catalog\_can\_contribute\]|List of users who can add exams to an exam catalog on Career Assessment.|
|Exam Catalog Can Take \[sn\_exam\_m2m\_catalog\_can\_take\]|List of users who can attempt exams in an exam catalog on Career Assessment.|
|Question \[sn\_exam\_question\]|Stores questions in an exam on Career Assessment.|
|Question option \[sn\_exam\_question\_option\]|Stores options for questions in an exam on Career Assessment.|
|Exam Question Response \[sn\_exam\_question\_response\]|Stores responses for questions in an exam on Career Assessment.|

**Parent Topic:**[Career Assessment reference](../concept/exam-engine-reference.md)

**Related topics**  


[Exam form](exam-form.md)

[Question form](question-form.md)

[Question option form](question-option-form.md)

[Learning internal content form](../concept/learning-internal-content-form-ca.md)

[Exam instance form](exam-instance-form.md)

[Exam instance attempt form](exam-instance-attempt-form.md)

