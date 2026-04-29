---
title: Associate a decision table with a License &amp; Permit case type​​
description: After you configure a pricing configuration decision table, associate it with the License &amp; Permit case type to append pricing configurations to that case type table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure decision tables, License and Permit Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Associate a decision table with a License &amp; Permit case type​​

After you configure a pricing configuration decision table, associate it with the License &amp; Permit case type to append pricing configurations to that case type table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables​**.

    You should be brought to Workflow Studio.

2.  Locate the pricing configuration decision table for the License and Permit case type, and right-click.

3.  In the context menu, select **Copy sys\_id**.​

4.  Open the **Public Sector Digital Service Endorsements Configuration** decision table and select **Create Draft**.

5.  Select **Add new decision row** to add an entry for the pricing decision table.

6.  On the form, fill in the fields with the following information:

<table id="table_ott_1wz_gdc"><thead><tr><th>

Field

</th><th>

Entry

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Child Table of License Permit

</td><td>

 

</td></tr><tr><td>

Product Model

</td><td>

Product model for the particular license/permit.

</td><td>

 

</td></tr><tr><td>

Endorsements Price Config Decision Table Sys Id

</td><td>

Paste the Sys Id of newly created pricing decision table.

</td><td>

 

</td></tr><tr><td>

Endorsements Fields

</td><td>

Table Fields used as endorsements \(separated by comma\)

</td><td>

Shows a form header above the eligibility questions. Leave this field empty.

</td></tr><tr><td>

Benefit Summary Field

</td><td>

benefit\_summary

</td><td>

This field is a column in License Permit Table that stores the endorsements and it's pricing in JSON format.

</td></tr><tr><td>

Endorsements Description

</td><td>

Description of the endorsement options available with the license/permit request.

</td><td>

This text will be displayed to the user in the **Select endorsements** playbook activity.

</td></tr><tr><td>

Fees Description

</td><td>

Description of the fee options associated with the license/permit request.

</td><td>

This text will be displayed to the user in the **Select endorsements** playbook activity.

</td></tr><tr><td>

Options Text

</td><td>

Text to be displayed for Options.

</td><td>

This text will be displayed to the user in the **Select endorsements** playbook activity.

</td></tr><tr><td>

Fees Text

</td><td>

Text to be displayed for Fees.

</td><td>

This text will be displayed to the user in the **Select endorsements** playbook activity.

</td></tr></tbody>
</table>7.  Select **Save**, then **Publish**.

8.  Select **Publish** when prompted.


## Result

The decision table is now associated with the License &amp; Permit case type.​​

