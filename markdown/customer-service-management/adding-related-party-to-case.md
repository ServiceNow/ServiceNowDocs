---
title: Adding related parties to a case
description: Add related parties to a case to help provide the access level to the related parties, such as contacts or consumers on a case.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-02-05"
reading_time_minutes: 2
breadcrumb: [Using customer access management, Customer management, Using Customer Service Management, Customer Service Management]
---

# Adding related parties to a case

Add related parties to a case to help provide the access level to the related parties, such as contacts or consumers on a case.

## Before you begin

Role required: sn\_customerservice\_agent

## About this task

Related parties and their assigned responsibilities are part of the Customer Access Management feature. Customer access management enables you to support multiple contacts and consumers on cases and sold products, providing them with varying levels of access to the case. For more information, see [Configuring Customer Access Management](../concept/configuring-cam.md).

Related parties that are added to cases must also be assigned the sn\_customerservice.case\_authorized\_contributor role.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Cases** &gt; **All**.

2.  Select the case where you want to add related parties.

3.  From the Related Parties related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_esz_qdw_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Related party type. The related party type can be a contact, consumer, or a contributor user.You can select from the list of related party configurations for the cases that are provided with the base system.

-   Authorized Contact
-   Authorized Consumer
-   Authorized Contributor
-   Listed Contact
-   Listed Consumer


</td></tr><tr><td>

Case

</td><td>

Case number.

</td></tr><tr><td>

User or Consumer

</td><td>

Contact or consumer responsible for the case.

</td></tr><tr><td>

Responsibility

</td><td>

Provides access level to case information.On selection of the related party type, the associated responsibility gets added by default. If the related party type is changed, the responsibility associated to the related party type gets updated accordingly.

 **Note:** If the responsibility field is empty, contacts do not have access to the sold product and associated case.

</td></tr></tbody>
</table>5.  Select **Submit**.

    Related parties are added to the case.

6.  Ensure that the contact or consumer selected in step 4 is assigned the sn\_customerservice.case\_authorized\_contributor role.


## Result

Once related parties are added to the case with a proper functional role having Authorized Representative responsibility, they can perform the following actions.

-   Close a case.
-   Update customer-visible case tasks.
-   Add additional comments and attachments.
-   Accept or reject a solution.
-   Receive notifications on case updates. To ensure related parties receive email notifications, add them to the email notification configuration.
    1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.
    2.  Select a notification.
    3.  In the Who will receive related list, select the lock icon next to **Users/Groups in fields**.
    4.  In the Available column, select **Related Party Users** and/or **Related Party Consumers** and move them to the Selected column.
    5.  Select the lock icon again and update the record.
    6.  Repeat these steps for each of the desired notifications.

**Related topics**  


[Case update notifications](../concept/case-update-notification-cam.md)

