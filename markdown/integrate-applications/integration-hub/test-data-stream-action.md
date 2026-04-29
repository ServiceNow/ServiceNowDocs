---
title: Test a Data Stream action
description: Test your Data Stream action to ensure that it works the way you expect before you add it to a flow.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Stream actions and pagination, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Test a Data Stream action

Test your Data Stream action to ensure that it works the way you expect before you add it to a flow.

## Before you begin

-   [Create a Data Stream action](create-data-stream-action.md)
-   Role required: action\_designer or admin

## About this task

Testing a Data Stream action returns the first 20 items by default. To change this value, add the **com.glide.hub.action\_type.datastream.test\_max\_iterations** system property with a value between one and 50.

## Procedure

1.  Open the Data Stream action you want to test.

    1.  Navigate to **Flow Designer** &gt; **Designer**.

    2.  Select the Actions tab.

    3.  Select the row for the Data Stream action you want to test.

2.  Select **Test**.

    The system displays the Test Action dialog. The contents of the Test Action dialog depend on the Data Stream action inputs.

3.  In the Test Action dialog, provide values for any action inputs and select **Run Test**.

4.  Open the Execution Details to ensure that the action executed as expected.

    The Execution Details **Runtime Value** returns the first 20 items returned by the Data Stream action.


## What to do next

[Use a Data Stream action in a flow](use-data-stream-in-flow.md).

**Parent Topic:**[Data Stream actions and pagination](../concept/data-stream-actions.md)

