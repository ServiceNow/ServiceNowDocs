---
title: Define an assignment rule for problems
description: After a problem is logged, it must be assigned to the appropriate group or individual to handle the problem. You can define assignment rules to automate the assignment process.
locale: en-US
release: zurich
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Problem Management, IT Service Management]
---

# Define an assignment rule for problems

After a problem is logged, it must be assigned to the appropriate group or individual to handle the problem. You can define assignment rules to automate the assignment process.

## Before you begin

Role required: assignment\_rule\_admin or admin

## About this task

Some assignment rules are predefined for Problem Management. Review the predefined assignment rules, and verify that the problem assignment rules you want to use are active. For example, the **Network Problem** assignment rule looks at the configuration item class for network problems and assigns the problem to the **Network** group.

In this procedure, define an assignment rule to assign database problems to the **Database** group. It is just an example to let you know how to define an assignment rule. The **Database Problem** assignment rule is already available in the base system.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Assignment** and click **New**.

2.  Complete the form using the following information.

    -   **Name**: `Database Problems`
    -   **Applies To** tab or section:
        -   **Table**: Problem \[problem\]
        -   **Conditions**: Dot-walk to **\[Configuration Item.Class\] \[is\] \[Database\]**.
    -   **Group** in the **Assign To** tab or section: **Database**
3.  Click **Submit**.

4.  Test the assignment rule by completing the following steps.

    1.  Navigate to **Problem** &gt; **Create New**.

    2.  Complete the problem form and select a configuration item with a class of **Database**.

    3.  Click **Submit**.

    4.  Open the problem and verify that the assignment group was added.


**Parent Topic:**[Configuring Problem Management](../concept/configuring-problem-mgmt.md)

**Previous topic:**[Configure problem categories](configure-problem-categories.md)

**Next topic:**[Categorize a problem as a major problem](categorize-major-problem.md)

