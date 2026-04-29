---
title: Use software counters with the legacy IBM PVU Process Pack
description: To calculate IBM PVU licenses through the legacy IBM PVU Process Pack, you can create a software counter with the IBM PVU license type. For a given PVU software package, you only need to create the counter once and then it can be reused.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy IBM PVU Process Pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Use software counters with the legacy IBM PVU Process Pack

To calculate IBM PVU licenses through the legacy IBM PVU Process Pack, you can create a software counter with the IBM PVU license type. For a given PVU software package, you only need to create the counter once and then it can be reused.

## Before you begin

Role required: sam

## About this task

Processor definitions are searched as licenses are counted. If a processor definition is found, but no PVU mapping link exists for the processor, the system automatically does the following to obtain a PVU mapping link.

-   Pre-filtering based on processor name.
-   Advanced filtering based on PVU mapping records' condition field.
-   If no exact match is found, the most expensive mapping is used to increase the chance of being compliant.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **Software Counters**.

2.  Click **New**.

3.  Enter a **Name**.

4.  Select a **Software Model**.

5.  Select a level of adherence to the license in the **Enforce to** field.

6.  For **License type**, select **Per Installation - IBM PVU**.

    ![PVU software counter](../image/PVUSoftwareCounter.png)

7.  Add information to other fields as necessary.

8.  Right-click the header bar and select **Save**.

9.  Click **Count licenses**.

    ![SAM software counter PVU results](../image/SAMSoftwareCounterPVUResults.png)

10. In the **Software Counter Results** list, drill down to obtain summary and detailed information.

    ![SAM software counter PVU results](../image/SAMSoftwareCounterPVUResults2.png)


**Parent Topic:**[Legacy IBM PVU Process Pack](../concept/c_IBMPVUProcessPack.md)

