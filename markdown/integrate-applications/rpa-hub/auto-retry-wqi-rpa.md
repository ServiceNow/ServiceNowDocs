---
title: Using auto-retry functionality for your failed work items in RPA Hub
description: You can use auto-retry functionality in RPA Hub to retry the failed items automatically in your work queue. The retry functionality is based on the Application exception type only.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Exploring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Using auto-retry functionality for your failed work items in RPA Hub

You can use auto-retry functionality in RPA Hub to retry the failed items automatically in your work queue. The retry functionality is based on the **Application** exception type only.

## Auto-retry overview

Usually, in an existing Robotic Process Automation \(RPA\) work queue, the items are processed by the criteria that you specified. The items in this type of work queue are picked by the robots for execution.

Let's consider a scenario where the first item in your work queue is processed successfully, and the status is updated to success. But, when the robot picks the second item in the work queue for execution, it isn't processed successfully and the status is updated to failure.

By using auto-retry functionality instead in this scenario, the work items are retried automatically based on the value in the **Exception Type** field on the Work Item form, and based on the values that you enter in the **Maximum Attempts** field and the **Attempt Delay** field on the Queue form.

There are two exception types: application and business.

In the Work Item form, if the value of the **Exception Type** field is **Application**, the value of the **Maximum Attempts** field is greater than 1, and the current value in the **Attempts Count** field is less than the value in the **Maximum Attempts** field, the failed item in the work queue is automatically retried.

**Note:** If the value in the **Exception Type** field is **Business**, the auto-retry functionality isn’t enabled.

## Queue fields and system property configuration

To enable auto-retry functionality, you must define the values in the **sn\_rpa\_fdn.queue.maximum\_attempts\_max\_value** system property. For more information about these values, see [Configure RPA Hub properties](../reference/rpahub-sys-properties.md).

You can enable auto-retry functionality by configuring the following fields on the Queue form:

-   **Maximum Attempts**
-   **Attempt Delay \(mins\)**

In the **Maximum Attempts** field, you define the number of attempts for the failed work items. In the **Attempt Delay \(mins\)**, you define the maximum delay, in minutes, before the work item is attempted again. For more information about these fields, see [Queue form in RPA Hub](../reference/queue-form.md) and [Create a queue in RPA Hub](../task/create-queue.md).

You can view the following fields that are related to the auto-retry functionality on the Work Item form:

-   **Exception Type**
-   **Attempts Count**

Based on the value in the **Exception Type** field, the auto retry functionality retries the work items. In the **Attempts Count** field, you can view the number of times the work item is picked for auto retry. For more information about these fields, see [Work item form in RPA Hub](../reference/work-queue-form.md).

## Auto-retry workflow

When the status of the work item that is selected in the automation is **In progress**, the auto-retry workflow is as follows:

-   If the **Exception Type** field is Application, the **Attempts Count** field is incremented by 1, and the current value in the **Attempts Count** field is equal to the value in the **Maximum Attempts** field, the status of the work item is updated to **Failed** and the **Exception Type** field is updated to Application. The work item isn’t available for auto-retry.
-   If the **Exception Type** field is Application, the **Attempts Count** field is incremented by 1, and the current value in the **Attempts Count** field is less than the value in the **Maximum Attempts** field, the status of the work item is updated to **In progress** and the **Exception Type** is updated to Application. The work item is available for auto-retry only after you set the duration \(if any\) in minutes in the **Attempts Count** field.
-   If the **Exception Type** field is Business and the **Attempts Count** field is incremented by 1, the status of the work item is updated to **Failed**, and the **Exception Type** field is updated to Business. The work item isn’t available for auto-retry.
-   When there’s no value in the **Exception Type** field and the **Attempts Count** field isn’t incremented by 1, the status of the work item is updated to **In progress**. The **Exception Type** isn’t updated. The work item is available for auto-retry only after you set the duration \(if any\) in minutes in the **Attempts Count** field.

**Note:** If the value in the **ReleaseMode** field is locked, then you can't increment the value in the **Attempts Count** field because the robot is still executing the work item. The value in the **Attempts Count** field must be incremented only when the value in the **ReleaseMode** field is release. The value in the **Attempts Count** field is incremented when an item is released by the robot or when an item's status is set to **Failure**.

The following table shows the auto-retry workflow for an **In progress** work item.

|Exception Type|Attempts Count \(Increment by 1\)|Condition|Status updated to|Exception Type updated to|
|--------------|---------------------------------|---------|-----------------|-------------------------|
|Application|Yes|If the current value in the **Attempts Count** field is equal to the value in the **Maximum Attempts** field.|Failed|Application|
|Application|Yes|If the current value in the **Attempts Count** field is less than the value in the **Maximum Attempts** field.|In progress|Application|
|Business|Yes|&lt;No condition&gt;|Failed|Business|
|&lt;empty&gt;|No|&lt;No condition&gt;|In progress|&lt;No update&gt;|

When the status of a work item that is selected in the automation is **Success**, the auto-retry workflow is as follows:

-   If the **Exception Type** field is Application and the **Attempts Count** field is incremented by 1, the status of the work item is updated to **Success** and the **Exception Type** is updated to blank. The work item isn’t available for auto-retry.
-   If the **Exception Type** field is Business and the **Attempts Count** field is incremented by 1, the status of the work item is updated to **Success**. The **Exception Type** is updated to blank, and the work item isn’t available for auto-retry.
-   If there’s no value in the **Exception Type** field and the **Attempts Count** field is incremented by 1, the status of the work item is updated to **Success**. The **Exception Type** field is updated to blank, and the work item isn’t available for auto-retry.

The following table shows the auto-retry workflow for a **Success** work item.

|Exception Type|Attempts Count \(Increment by 1\)|Status updated to|Exception Type updated to|
|--------------|---------------------------------|-----------------|-------------------------|
|Application|Yes|Success|&lt;blank&gt;|
|Business|Yes|Success|&lt;blank&gt;|
|&lt;blank&gt;|Yes|Success|&lt;blank&gt;|

When the status of work item that is selected in the automation is **Failed**, the auto-retry workflow is as follows:

-   If the **Exception Type** is Application, the **Attempts Count** field is incremented by 1, and the current value in the **Attempts Count** field is less than the value in the **Maximum Attempts** field, the status of the work item is updated to **In progress**. The **Exception Type** field is updated to Application, and the work item is available for auto-retry only after the duration that you set in the **Attempts Count** field.
-   If the **Exception Type** field is Application, the **Attempts Count** field is increment by 1, and the current value in the **Attempts Count** field is equal to the value in the **Maximum Attempts** field, the status of the work item is updated to **Failed**. The **Exception Type** field is updated to Application, and the work item isn’t available for auto-retry.
-   If the **Exception Type** is Business, the **Attempts Count** field is incremented by 1, the status of the work item is updated to **Failed**. The **Exception Type** field is updated to Business, and the work item isn’t available for auto-retry.
-   If there’s no **Exception Type** field and the **Attempts Count** field is incremented by 1, the status of the work item is updated as **Failed**. The **Exception Type** field isn’t updated, and the work item isn’t available for auto-retry.

The following table shows the auto-retry workflow when the **Failed** status is selected in the automation.

|Exception Type|Attempts Count \(Increment by 1\)|Condition|Status updated to|Exception Type updated to|
|--------------|---------------------------------|---------|-----------------|-------------------------|
|Application|Yes|If the current value in the **Attempts Count** field is less than the value in the **Maximum Attempts** field.|In progress|Application|
|Application|Yes|If the current value in the **Attempts Count** field is equal to the value in the **Maximum Attempts** field.|Failed|Application|
|Business|Yes|&lt;No condition&gt;|Failed|Business|
|&lt;empty&gt;|Yes|&lt;No condition&gt;|Failed|&lt;No update&gt;|

**Note:** The value in the **Deferred Till** field is obtained from the component. This field always takes precedence over the **Attempt Delay \(mins\)** field. The **Deferred Till** field is a read-only field on the work item form. For more information, see [Work item form in RPA Hub](../reference/work-queue-form.md).

**Related topics**  


[Queue implementation in RPA Hub](queues-implement-rpa.md)

