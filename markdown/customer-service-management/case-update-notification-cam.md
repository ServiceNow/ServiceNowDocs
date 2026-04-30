---
title: Case update notifications
description: Contacts, consumers, and contributor users added to a case with the authorized representative responsibility can receive all email notifications that are also received by the primary contact of the case.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2026-03-11"
reading_time_minutes: 1
breadcrumb: [Adding related parties to a case, Using customer access management, Customer management, Using Customer Service Management, Customer Service Management]
---

# Case update notifications

Contacts, consumers, and contributor users added to a case with the authorized representative responsibility can receive all email notifications that are also received by the primary contact of the case.

Contacts added as additional contacts to the sold product with the Authorized Representative responsibility can receive all email notifications that are received by the primary contact of the case.

Consumers added as an additional consumer to the sold product with the Authorized Representative responsibility can receive all email notifications that are received by the primary consumer of the case.

Internal users added as related parties to the case with the Authorized Representative responsibility can receive all email notifications that are received by the primary contact or consumer of the case.

For case resolved emails, related parties with the Authorized Representative responsibility can accept or reject the proposed solution. The responses of emails from related parties are treated similarly to the primary contact or consumer on the case. For more information, see [Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Role assignments for authorized representatives

Related parties that are added to cases must also be assigned one of the Customer Access Management \(CAM\) roles, such as the sn\_customerservice.case\_authorized\_contributor role. For more information, see [Roles installed with Customer Access Management](../reference/r_rolesinstalledwithcustaccessmgmt.md).

## Adding related parties to notifications

Related parties that are added to cases can receive notifications on case updates. To ensure related parties receive email notifications, add them to the email notification configuration.

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.
2.  Select a notification.
3.  In the Who will receive related list, select the lock icon next to **Users/Groups in fields**.
4.  In the Available column, select **Related Party Users** and/or **Related Party Consumers** and move them to the Selected column.
5.  Select the lock icon again and update the record.
6.  Repeat these steps for each of the desired notifications.

