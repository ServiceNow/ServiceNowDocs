---
title: Suspend and resume an HR case
description: If you are unable to close the HR case within the duration specified in the service level agreement \(SLA\), you can suspend the case.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [HR Case Management, Explore and use HR Case and Knowledge Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Suspend and resume an HR case

If you are unable to close the HR case within the duration specified in the service level agreement \(SLA\), you can suspend the case.

## Before you begin

Role required: sn\_hr\_core.basic or sn\_hr\_core.case\_writer

## About this task

For example, to contact a vendor, such as the insurance administrator or payroll processing company, to obtain the required information to close the case. After beginning work on the case, you can suspend it until the information is received. This way the HR case does not show that the SLA is breached. When the information is received, you enter it into the case and resume SLA tracking.

## Procedure

1.  Open the HR case to suspend.

    Begin work on the case before suspending it.

2.  From the **State** field, click and select **Suspended**.

    The **Suspend Reason** pop-up window opens.

3.  Select one of the following suspension reasons and enter the information you are waiting for.

    -   **User**: If you need more information from the employee before proceeding.
    -   **Company**: If you are waiting for a reply from a vendor or other outside company.
    -   **Group**: If you are waiting for a reply from an internal group.
    -   **Other**: If you suspend the case for any other reason.
    For example, if you are waiting for the health insurance administrator to investigate an employee claim, select **Company** for the reason and enter `Results of investigation` or something similar.

4.  In the **Work Note** field, enter information about why the case is suspended.

    **Note:** Translate the text in your preferred language using the **Translate** option. For configuring the dynamic translation framework, see [Dynamic translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

5.  Click **Suspend**.

    The SLA stops progressing and the suspension notes appear in the activity stream as work notes. You can continue to add work notes to a suspended case.

6.  To resume a suspended HR case, open the case and click **Resume**.

    The SLA progress is resumed.


**Parent Topic:**[HR Case Management](../concept/c_HRCaseManagement.md)

