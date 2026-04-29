---
title: Create spoke and build actions manually
description: Automate an integration and generate reusable actions manually.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Building spokes using Spoke Generator, Workflow Studio, Build workflows]
---

# Create spoke and build actions manually

Automate an integration and generate reusable actions manually.

## Before you begin

-   Install the Spoke Generator app from the ServiceNow Store.
-   Role required: admin or action\_designer

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click **Create new** &gt; **Spoke**.

3.  On the General Info screen, select an image as the logo for your integration and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Spoke name|Name to identify the custom spoke.|
    |Description|Description about the custom spoke.|

4.  Click **Create and continue**.

    The spoke is created and a confirmation message is displayed.

5.  On the Build Info screen, select the method using which you want to build your spoke.

6.  Select **Manually** and click **Continue**.

    The spoke details page is displayed.

7.  Click **New action** to create an action.

    -   If you want to create actions by importing the required OpenAPI Specification, select **From OpenAPI spec**. For information about selecting the required operations and creating actions, see [Create spoke and build actions by importing an OpenAPI Specification](create-spoke-fd.md).
    -   If you want to create actions manually, select **Manually**. The Action Properties screen is displayed. You should create and publish the action in the Action Designer. For more information, see [Building actions](../concept/actions.md).

