---
title: Configure a characteristic for a dosage specification
description: Configure a characteristic for a dosage so that you can define the dosages for a medication product in Healthcare and Life Sciences workflows.
locale: en-US
release: zurich
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure dosage specifications, Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure a characteristic for a dosage specification

Configure a characteristic for a dosage so that you can define the dosages for a medication product in Healthcare and Life Sciences workflows.

## Before you begin

To add a specification characteristic, ensure that the dosage specification is in the **Draft** state.

Role required: sn.hcls\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Dosage specifications**.

2.  In the Dosage specifications list, click the link to a dosage specification from the **Name** column.

3.  In the Specification Characteristics related list, click **New**.

4.  In the **Characteristic** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and select a characteristic from the **Name** column of the Characteristics list.

    By default, the application provides the following dosage characteristics for use a reference:

    -   Dosage
    -   Instructions for patient
    -   Max dose per day
    -   Number of authorized refills
    -   Number of authorized refills \(choice\)
    -   Quantity
    -   Quantity \(per month supply\)
    -   Quantity \(per week supply\)
    To create a new characteristic, click **New** in the Characteristics list and fill in the characteristic details.

5.  Add characteristic options for a characteristic of the Choice input type by clicking the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) in the **Characteristic Option** field and selecting a characteristic option from the **Option** column of the Characteristic Options list.

    To create a new characteristic option, click **New** in the Characteristic Options list and fill in the characteristic option details.

6.  Click **Submit**.

    **Note:** You can ignore the Activities section, which is not used.

7.  To associate a characteristic with a dosage specification, add the characteristic to a characteristic group included in the Dosage characteristic group.


