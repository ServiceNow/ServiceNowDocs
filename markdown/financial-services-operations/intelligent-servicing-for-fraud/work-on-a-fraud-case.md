---
title: Work on a fraud case for card fraud by alert
description: Use card fraud by alert to work on a fraud case that is created for processing alerts that are received from an external fraud detection system, ensure that any outstanding tasks are completed, and the cases are investigated and resolved.
locale: en-US
release: zurich
product: Intelligent Servicing for Fraud
classification: intelligent-servicing-for-fraud
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Intelligent Servicing for Fraud, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a fraud case for card fraud by alert

Use card fraud by alert to work on a fraud case that is created for processing alerts that are received from an external fraud detection system, ensure that any outstanding tasks are completed, and the cases are investigated and resolved.

## Before you begin

Role required: sn\_bom\_fraud.agent or sn\_bom\_fraud.agent\_connector

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Fraud cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all fraud cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Use the activities and tasks under the following playbook stages to fulfill the request and resolve the case:

    -   **Initiate**- This stage enables you to enter fraud information, verify fraud transactions, and submit the case.
    -   **Process alert** - This stage enables you to evaluate the fraud risk using the Decision Builder capabilities. Based on the business rules configured in the Card fraud risk evaluation rules, the card fraud is evaluated as Low risk or High risk.
    -   **Investigate**- This stage enables you to investigate the fraud case and request for manager approval to review the fraud investigation.

        **Note:** To resolve cases, agents can also request documents until the closure of the case. The case can also be routed for approval to a fraud manager.​

    -   **Case disposition** - This stage enables you to capture case outcome, notify the customer, update fraud management system, request write-off, and complete all the fulfilment fraud tasks.
    Any tasks generated during playbook activities appear in the **Tasks** tab of the case.

7.  Close the task from the task form.

    |Activity|Action|
    |--------|------|
    |**To update/complete fraud information**|In the case playbook, select **Mark complete**.|
    |**To submit a fraud case**|In the case playbook, select **Submit**.|
    |**To close investigation tasks**|In the task form, select **Close** to close the task.|


