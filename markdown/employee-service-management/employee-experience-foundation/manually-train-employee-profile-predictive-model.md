---
title: Manually train the employee profile predictive model
description: Manually train the employee profile predictive intelligence to model similar users if auto-train is not enabled by default.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage the employee profile AI and ML model, Employee profile, Setup task management, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Manually train the employee profile predictive model

Manually train the employee profile predictive intelligence to model similar users if auto-train is not enabled by default.

## Before you begin

Role required: sn-employee.admin

## Procedure

1.  Navigate to **Self-Service** &gt; **** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  Select **Train** for **Similar users model for employee profile** \(**ml\_x\_snc\_sn\_employee\_global\_similar\_users\_model\_for\_employee\_profile**\).

    A similarity definition record is created after the training is finished.

    **Note:**

    -   Set the variable system property to **True** with the **Application** scope set to **Global** to use the auto-train model on Employee Profile.
    -   Provide a minimum of 10 records to use the auto-train model.

