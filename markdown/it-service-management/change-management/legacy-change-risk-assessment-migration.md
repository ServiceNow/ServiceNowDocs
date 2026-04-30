---
title: Migrate to legacy change risk assessments
description: Users can migrate legacy change risk assessments to versions compatible with the new Change Risk Assessment table schema and logic.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Analyze change request risk and impact rating, Reference section for Change Management, Change Management, IT Service Management]
---

# Migrate to legacy change risk assessments

Users can migrate legacy change risk assessments to versions compatible with the new Change Risk Assessment table schema and logic.

## Before you begin

Few points to remember:

-   Customers with Change Management - Risk Assessment \[Legacy\] \(**com.snc.change.risk\_assessment**\) plugin already installed on their instances should only follow this task.
-   The Change Management - Risk Assessment \[Legacy\] \(**com.snc.change.risk\_assessment**\) plugin cannot be installed for customers who are on Kingston and later releases.
-   Migration guidance and best practice suggests that the migration should be performed on a development instance and not on a production instance.
-   The development instance must have the new Change Management - Risk Assessment \[com.snc.change\_management.risk\_assessment\] plugin installed.
-   All migration work must be captured in an update set, moved to a test instance, and then tested before moving them to a production instance.

Role required: itil\_admin

## About this task

The following legacy risk assessment components are migrated:

-   Risk assessment definition, questions, and question choices.
-   For multiple assessment conditions, the migration might result in the following one or more than one risk assessment records:
    -   If all the multiple assessment conditions are on the same table, then the migration results in only one risk assessment.
    -   If the multiple assessment conditions are on different tables, then the migration creates as many risk assessments as they pertain to different tables.

## Procedure

1.  Create an update set and set it as the current set.

    For more information, see [Create and select an update set as the current set](https://www.servicenow.com/docs/access?context=create-select-update-set&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

2.  Navigate to **Change** &gt; **Risk Assessment \(legacy\)**.

3.  Open the legacy risk assessment that you want to migrate to a change risk assessment.

4.  Click the **Migrate to Risk Assessment** related link.

5.  Click **OK**.

6.  Repeat steps 4-5 for all the legacy risk assessment to be migrated.


## What to do next

After all the legacy risk assessments are migrated, reach out to the support team to run the following scripts:

```
disable_legacy_change_risk_assessment.js
```

Capture the results in the update set created and later mark the update set as closed complete. For more information, see [Mark an update set complete](https://www.servicenow.com/docs/access?context=t_CompleteUpdateSets&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

**Note:** The given procedure is a suggested practice. Alternatively, you can capture each migrated Change Risk Assessment in their own update set. You can also capture the results of disabling of the Change Management - Risk Assessment \[Legacy\] using `disable_legacy_change_risk_assessment.js` in a separate update set.

-   **[Migrated risk assessment components](../reference/migrated-risk-assessment-components.md)**  
When you migrate a change risk assessment, the system maps records from legacy risk assessment to the new risk assessment tables.

**Parent Topic:**[Analyze change request risk and impact rating](../concept/change-risk-conflict-analysis.md)

