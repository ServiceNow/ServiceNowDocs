---
title: Automated Sharing of Outbound Intelligence Records
description: Automated Outbound Intelligence Sharing enables the seamless and automatic distribution of intelligence records to external systems.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Threat Intelligence Security Center, Security Operations]
---

# Automated Sharing of Outbound Intelligence Records

Automated Outbound Intelligence Sharing enables the seamless and automatic distribution of intelligence records to external systems.

## Before you begin

Role required:

-   System Administrator \(view, create or edit\)
-   sn\_sec\_tisc.admin \(view\)

## About this task

The automated flow action creates an outbound intelligence sharing record with the specified records and processes them accordingly.

Creating an outbound intelligence share record via automated process:

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select **Automated sharing of high-risk IOC's with trusted partners** action link to view the respective rule details in the flow designer.

4.  View the flow designer action for the following triggers:

    ```
    Daily at 12.00.00
    Run every day once
    ```

5.  Go to **Actions**

    |Action|Description|
    |------|-----------|
    |**Select the Sharing Template**|Templates with a usage mode of both **On-Demand and Automated Sharing**, and **Automated Sharing** can be selected for Automated Sharing.|
    |**List of Observables**|Select the type of observables record to add to an outbound intelligence record.|
    |**List of Indicators**|Select the type of indicators to add to an outbound intelligence record.|
    |**List of Objects**|Select the type of objects to add to an outbound intelligence record.|
    |**Include Related Records**|Add the related records of the selected observables, including indicators and objects.|
    |**Requires approval**|Select the check box that requires approval for the outbound intelligence record. [Defining Approval Rule for Outbound Intel](../task/tisc-approval-outbound-intel.md).|
    |**Users assigned to approve requests**|Select the users responsible for reviewing and approving outbound intelligence sharing record. For more information, see [Defining Approval Rule for Outbound Intel](../task/tisc-approval-outbound-intel.md).|
    |**Groups assigned to approve requests**|Select the groups responsible for reviewing and approving outbound intelligence sharing record. [Defining Approval Rule for Outbound Intel](../task/tisc-approval-outbound-intel.md).|

6.  Select **Done**.


## What to do next

Activate the flow. For more information on automated flows, see [Automated sharing of high-risk IOC's with trusted partners](../task/tisc-automated-sharing-flow.md).

**Related topics**  


[Configuring Outbound Intel Sharing Controls](../task/tisc-outbound-sharing.md)

[Sharing of Outbound Intelligence Records from GUI](tisc-create-intel-records-lib.md)

