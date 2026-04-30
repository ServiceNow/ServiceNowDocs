---
title: Customer service email properties
description: If you have the administrator role, you can set several properties for the Customer Service Management email communication channel.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the email channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Customer service email properties

If you have the administrator role, you can set several properties for the Customer Service Management email communication channel.

After creating the incoming and outgoing email addresses that customers use to communicate with customer service agents, the administrator can set the following email-specific properties. Navigate to **Customer Service** &gt; **Administration** &gt; **Properties** to access these properties.

<table id="table_ek3_ndy_nr"><thead><tr><th>

Property

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Case email address\[glide.cs.email.case\_queue\_address\]

</td><td>

One of the incoming email addresses that automatically creates a customer service case.For incoming email, the system checks the address to see if it matches the address in the **Case email address** property. If yes, the system creates a customer service case. If it doesn't match, or if this property isn't set, the system then checks the **Email subject prefix format for new case** property.

</td></tr><tr><td>

Email subject prefix format for new case \[glide.cs.email.new\_case\_prefix\]

</td><td>

The prefix included in the subject line of an email to any of the incoming email addresses that automatically creates a customer service case. **Case:** is the default prefix.

</td></tr><tr><td>

Create a case for a non-matched user\[sn\_customerservice.email.create\_case\_for\_non\_matched\_user\]

</td><td>

Enable the creation of new customer service cases when emails are received from users with email addresses that don't currently exist in the system.

</td></tr><tr><td>

Number of activities\[number\_of\_activities\_in\_notification\]

</td><td>

Indicates the number of activities \(emails and comments\) in the activity history that are included in the email notifications and replies. The default value is 3.

</td></tr><tr><td>

Include system emails in email notifications\[include\_system\_emails\_in\_notification\]

</td><td>

Indicates whether system emails are included in email notifications. The default value is false.

</td></tr><tr><td>

Number of activities in replynumber\_of\_activities\_in\_reply

</td><td>

Number of additional comments and emails included in Reply/Reply-All templates \(-1 means all\)

</td></tr><tr><td>

Email history notifications

</td><td>

By default, the email history shows the last three comments in the case record. To customize the number of notifications \(emails and comments\) on a case record in email replies and email notifications, add this script `${mail_script:get_emails_comments_activity_history}` to the template. Two examples of templates you can use the script to update are email reply template \(reply-received\) and the case commented template \(case.commented.for.customer\). For more information, refer to [Configure email and comment notifications](../concept/config-email-notifications.md).

</td></tr></tbody>
</table>