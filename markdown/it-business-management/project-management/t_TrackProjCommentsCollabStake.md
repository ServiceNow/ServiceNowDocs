---
title: Track project comments and collaborate with stakeholders
description: When a project is in progress, you can take advantage of two platform features that help project participants interact and collaborate: journal fields and live feed. Two useful journal fields are Comments and Work notes.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Update a project, Starting a project, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Track project comments and collaborate with stakeholders

When a project is in progress, you can take advantage of two platform features that help project participants interact and collaborate: journal fields and live feed. Two useful journal fields are Comments and Work notes.

## Before you begin

Role required: it\_project\_manager

## Procedure

-   To add journal fields to a project form:

    1.  [Configure](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) any project form to show **Comments** and **Work notes**.

-   To add [live feed](https://www.servicenow.com/docs/access?context=c_GetStartedWithLiveFeed&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) to a project form:

    1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

    2.  Select the **pm\_project** table name that has no corresponding **Column name**.

    3.  In the **Attributes** field, enter `live_feed=true`.

    4.  Select **Update**.

    5.  Navigate to **All** &gt; **System Definition** &gt; **UI Actions**.

    6.  Open the **Follow on Live Feed** list action.

    7.  In the **Table** field, select the \[pm\_project\] table.

    8.  Right-click the header and select **Insert** to create a copy of the UI action for the \[pm\_project\] table.

    9.  Repeat the steps for the UI actions for the **Show Live Feed** form action.

    10. Personalize the Project form and add **Activities \(filtered\)**, which is the activity formatter, to the desired location on the Project form.


**Parent Topic:**[Update a project](t_UpdateAProjectInProgress.md)

**Related topics**  


[Update a project](t_UpdateAProjectInProgress.md)

