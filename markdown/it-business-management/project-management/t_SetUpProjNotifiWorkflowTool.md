---
title: Set up project notifications with the workflow tool
description: Use the workflow tool, for example, to set up a workflow that sends an email notification when the state of a project task becomes Work in Progress.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Activate project task email notifications, Starting a project, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Set up project notifications with the workflow tool

Use the workflow tool, for example, to set up a workflow that sends an email notification when the state of a project task becomes **Work in Progress**.

## Before you begin

Role required: admin

## Procedure

1.  Create a workflow with the following attributes:

    -   **Name:** Notify assignee
    -   **Table:** Project task \[pm\_project\_task\]
    -   **If condition matches:** Run if no other workflows matched yet
    -   **Condition:** State is **Work in Progress** and **Assigned to** is not empty

        **Note:** Do not modify other attributes in this example.

2.  Add a single Notification activity between the Start and End activities.

    Drag the activity onto the connector line until it changes color. The attributes of the activity are similar to the following example:

    -   **Name:** Notify assignee
    -   **To:** $\{assigned\_to\}
    -   **Subject:** Project task $\{number\} has been activated and is assigned to you
    -   **Message:**Project task $\{number\} has been activated and is assigned to you
        -   Number: $\{number\}
        -   Short description: $\{short\_description\}
        -   Planned start date: $\{start\_date\}
        -   Planned end date: $\{end\_date\}
        -   Planned duration: $\{duration\}
    ![screenshot for project notifications](../image/Notificationwf.png)


**Parent Topic:**[Activate project task email notifications](t_ActivateProjTaskEmailNot.md)

**Related topics**  


[Activate project task email notifications](t_ActivateProjTaskEmailNot.md)

