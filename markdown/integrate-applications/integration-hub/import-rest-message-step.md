---
title: Import a REST message into a REST step
description: Transfer data from an existing Platform REST message into a REST step.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [REST step, Integration steps, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Import a REST message into a REST step

Transfer data from an existing Platform REST message into a REST step.

## Before you begin

-   This import is done from within a REST step in Workflow Studio. To create a REST step, Create an action and add a [REST step](../reference/rest-request-action-designer.md) to it.
-   The REST step uses Connection and Credential aliases for authentication details. If your REST message stores authentication details, create a Connection and Credential alias for them. For more information, see Create a Connection and Credential alias.
-   Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  On the Workflow Studio landing page, select **Actions** and open the action that has the REST step you want to use for the import.

3.  In the REST step, locate the **Build Request** field and select **From REST Message**.

4.  In the **REST Message** field, select the REST message to import.

5.  In the **REST Message Function** field, select the function.

    The available options are determined by the HTTP methods associated with the selected REST message.

6.  Select the **Import REST Message** button.

    The Import ServiceNow REST Message window displays the data from the selected REST message.

7.  Select the **Configure step** button.


## Result

The data from the REST message is loaded into the REST step. No future changes to the REST message are copied to the derivative REST steps. Rather than maintain two versions of your REST logic, you should only maintain and update the REST step.

If the imported REST message has a MID Server configured in any of its functions, the **Use MID** check box in the Connection Details section is checked and a data pill provided for the MID Server.

## What to do next

Fill in any other required fields and test the step with the **Test REST step** button.

**Parent Topic:**[REST step](../reference/rest-request-action-designer.md)

