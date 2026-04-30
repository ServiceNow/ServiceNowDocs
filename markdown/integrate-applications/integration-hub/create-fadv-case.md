---
title: Create a case in First Advantage from ServiceNow
description: Initiate the background check of the required candidate using invite or order from ServiceNow.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [First Advantage Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Create a case in First Advantage from ServiceNow

Initiate the background check of the required candidate using invite or order from ServiceNow.

## Before you begin

-   [Set up the First Advantage spoke](setup-first-adv.md#)
-   [Synchronise First Advantage accounts and packages with ServiceNow](setup-first-adv.md#)
-   Create users in the User \[sys\_user\] table. Background check can be performed only for these users.
-   Role required: First Advantage admin or First Advantage user

## Procedure

1.  Navigate to **All** &gt; **First Advantage Spoke** &gt; **Create New First Advantage Case**.

    Form to provide the First Advantage case details is displayed.

2.  On the form, fill these values.

<table id="table_yqb_5nf_5kb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use Distribution Email for getting invite email from First Advantage

</td><td>

Option to send invitation email to all users in the distribution email.

</td></tr><tr><td>

Select User

</td><td>

User in the User \[sys\_user\] table.

</td></tr><tr><td>

First Name

</td><td>

First name of the selected user. The value is auto-populated based on the user selected in **Select User**.

</td></tr><tr><td>

Last Name

</td><td>

Last name of the selected user. The value is auto-populated based on the user selected in **Select User**.

</td></tr><tr><td>

Email

</td><td>

Email address of the selected user. The value is auto-populated based on the user selected in **Select User**.

</td></tr><tr><td>

Select An Account

</td><td>

First Advantage account to perform the background check.

</td></tr><tr><td>

Select A Package

</td><td>

First Advantage package to perform the background check.

</td></tr><tr><td>

Short Description

</td><td>

Brief description about the background check.

</td></tr><tr><td>

Agent Name

</td><td>

Agent to perform the background check.

</td></tr><tr><td>

Send Invite link

</td><td>

Option to send an invite email. When selected, a request to complete an application is sent to the candidate through an invite email. If this option isn't selected, an order email is sent to the user. An order record is created and request to provide essential details is sent to the candidate.

**Note:**

-   When the **Send Invite link** option is selected, an order is created only after the candidate has filled the application form.
-   When the **Send Invite link** option isn't selected, an order is immediately created.
Events updates can be accessed in your ServiceNow instance .

</td></tr><tr><td>

Use "Order As"

</td><td>

Option to place order on behalf of the required user.

</td></tr><tr><td>

Email \(Order As\)

</td><td>

Email ID of the required user. This field is available only when the **Use "Order As"** check box is selected.

</td></tr><tr><td>

Account ID \(Order As\)

</td><td>

Account ID of the required user. This field is available only when the **Use "Order As"** check box is selected.

</td></tr><tr><td>

User ID \(Order As\)

</td><td>

User ID of the required user. This field is available only when the **Use "Order As"** check box is selected.

</td></tr></tbody>
</table>3.  Click **Submit**.

    A First Advantage task is created in your ServiceNow instance with **State** as **Draft**. The case can be accessed by navigating to **First Advantage Spoke** &gt; **First Advantage Cases**.


