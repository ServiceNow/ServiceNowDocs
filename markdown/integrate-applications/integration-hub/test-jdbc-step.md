---
title: Test JDBC step
description: Test the JDBC step before testing or publishing an action that contains the JDBC step.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [JDBC step, Integration steps, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Test JDBC step

Test the JDBC step before testing or publishing an action that contains the JDBC step.

## Before you begin

Role required: admin

## About this task

It is mandatory that you test the JDBC step before testing the action. Testing ensures that the relevant complex object output schema is created from table columns, which can be used as data pills in subsequent steps.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  [Create an action](https://www.servicenow.com/docs/access?context=create-action&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) with a [JDBC step](../reference/jdbc-step.md).

3.  Click **Test JDBC Step**.

    The **Test JDBC Step** pop-up window is displayed.

4.  If the JDBC step takes an action input or output of the previous step as its input, provide required input values in the**Step input pills** field to test the JDBC step.

    **Note:** Input values in the **Step input pills** fields are not needed when records are updated, inserted, or deleted.

5.  Click **Run Test**.

    -   When a SELECT query is executed, **Sample Result** is displayed in the **Test JDBC Step** pop-up window. **Sample Result** includes column names, columns types, and the values of the first row.
    -   When an UPDATE, INSERT, or DELETE query is executed, a message is displayed mentioning the number of rows affected.
6.  To use the sample result as the JDBC step output, click **Use Result**.

    **Note:** **Use Result** is not displayed when records are updated, inserted, or deleted.

7.  To retrieve schema of a different table when a SELECT query is executed in the JDBC step, enter the required value in the **Step input pills** field and click **Run Test**.


## Result

When a SELECT query is executed in the JDBC step, **ResultSet** is displayed under **Outputs**. The relevant complex object output is populated. To learn more about complex objects, see [Complex data](https://www.servicenow.com/docs/access?context=complex-data&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## What to do next

Test and publish the action.

