---
title: Create confidentiality inheritance
description: Create confidentiality inheritance in the tables that are already configured in the confidentiality configuration module. In the GRC application, whenever a parent record is marked or unmarked as confidential, its related table records are also marked or unmarked as confidential, if an inheritance record is also set up.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure confidential inheritance, Confidential records, Common GRC features, Governance, Risk, and Compliance]
---

# Create confidentiality inheritance

Create confidentiality inheritance in the tables that are already configured in the confidentiality configuration module. In the GRC application, whenever a parent record is marked or unmarked as confidential, its related table records are also marked or unmarked as confidential, if an inheritance record is also set up.

## Before you begin

Role required: sn\_grc.admin

## Procedure

1.  Navigate to **All** &gt; **GRC Administration** &gt; **Confidentiality Configuration**.

2.  Select the table that you want to configure the inheritance in.

3.  In the Confidentiality inheritance configurations related list, select **New**.

4.  On the form, fill in the fields.

    The following example shows how to configure the confidentiality inheritance. For more information about the fields, see [Confidentiality Inheritance Configuration form](../reference/confidentiality-inheritance-configuration-record.md).

    ![Confidentiality inheritance configuration.](../image/confidentiality-inheritance-configuration.png "Confidentiality inheritance configuration")

5.  Select **Submit**.

    **Note:**

    This configuration doesn't affect the existing confidentiality of the records in the parent and inheriting tables.

    Only records that are marked as **Active** support the inheritance.


## Result

A new inheritance configuration record is created under the confidentiality inheritance configuration related list.

