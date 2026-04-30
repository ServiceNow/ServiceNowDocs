---
title: Associate a decision table with a License &amp; Permit case type​​
description: After you configure a pricing configuration decision table, associate it with the License &amp; Permit case type to append pricing configurations to that case type table.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure decision tables for License and Permit Playbook, License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Associate a decision table with a License &amp; Permit case type​​

After you configure a pricing configuration decision table, associate it with the License &amp; Permit case type to append pricing configurations to that case type table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables​**.

2.  Locate the pricing configuration decision table for the License and Permit case type, and right-click.

3.  In the context menu, select **Copy sys\_id**.​

4.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

5.  Locate the entry with **sn\_gsm\_license\_permit\_case** as the Table name, and **attribute\_pricing\_config** as the Column name.

6.  Select the record to open it.

7.  Under the Dictionary Overrides tab, select **New**.

8.  Set the Table field to the License and Permit case type table that you wish to associate with the decision table.​

9.  Select the checkbox for **Override default value**.

10. Paste the copied sys\_id value into the **Default value** field.

11. Select **Submit**.


## Result

The decision table is now associated with the License &amp; Permit case type.​​

