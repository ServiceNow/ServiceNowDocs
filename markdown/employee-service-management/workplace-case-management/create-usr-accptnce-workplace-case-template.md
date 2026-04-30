---
title: Create a User acceptance Workplace case template
description: Create a Workplace case template with user acceptance.
locale: en-US
release: zurich
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a Workplace case template, Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create a User acceptance Workplace case template

Create a Workplace case template with user acceptance.

## Before you begin

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## About this task

Create this case template for use when a user's approval or rejection is required to close the request.

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Case templates**.

2.  Create a template or modify an existing template.

    -   If you are creating a new template, click **New**.
    -   If you are modifying an existing template, open the desired template.
    For information about the template form fields, see [Create a template](https://www.servicenow.com/docs/access?context=t_CreateATemplateUsingTheTmplForm&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

3.  In the **Table** field, select the **Workplace case \[sn\_wsd\_case\_workplace\_case\]** table.

4.  In the **Template** field, enable user acceptance and acceptance time-out.

    1.  In the left column, select **Enable user acceptance** and in the right column, select **True**.

    2.  In the left column, select **Acceptance timeout** and in the right column, specify the duration after which the acceptance request can expire.

5.  Click **Submit**.


## Result

The Case template is created with user acceptance options enabled.

## What to do next

Use the template in Workplace services where user acceptance is required. For more information about creating Workplace services, see [Create a Workplace service](create-workplace-service.md).

