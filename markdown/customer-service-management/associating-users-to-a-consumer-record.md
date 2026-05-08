---
title: Creating and associating a Unified Consumer user to a consumer record
description: Create and associate a Unified Consumer user with a consumer record so that your user can access the Customer Service Portal \(CSP\). This process involves creating a Unified Consumer user through a consumer form and then associating the user to a consumer record.Create a Consumer User through the User lookup list on the consumer form.Associate a user with a consumer record in the Customer Service Management \(CSM\) application. After the association is done, you can access the Consumer Service Portal \(CSP\) as a consumer to search for information, create cases, and more.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up a user as a Unified Consumer, Configuring a user as a Unified Consumer, Configuring a Unified User, User management, Set up your environment, Configure, Customer Service Management]
---

# Creating and associating a Unified Consumer user to a consumer record

Create and associate a Unified Consumer user with a consumer record so that your user can access the Customer Service Portal \(CSP\). This process involves creating a Unified Consumer user through a consumer form and then associating the user to a consumer record.

## Create a Consumer User through a consumer form

Create a Consumer User through the User lookup list on the consumer form.

### Before you begin

Role required: sn\_crm\_consumer\_data\_manager, sn\_crm\_consumer\_relationship\_data\_manager, sn\_crm\_household\_data\_manager or sn\_crm\_household\_relationship\_data\_manager or sn\_crm\_foundation\_data\_manager, sn\_crm\_foundation\_admin or admin

### About this task

You can create both the internal \(snc\_internal\) and external \(snc\_external\) users.

**Note:** Only administrators can associate a sys\_user with a consumer, and each user can be associated with only one consumer.

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Consumers**.

2.  Select the consumer from the consumer record.

3.  In the Login Details related list, select the User lookup icon ![Lookup icon.](../image/lookup-list.jpg) to open the list of sys\_users.

4.  On the Users list, select **New**.

    **Note:** If the unified consumer isn’t configured, the system redirects to the consumer user form. If other user extensions are configured, it redirects to the interceptor, enabling you to select the user type.

5.  On the form, fill in the fields.

    For a description of the field values, see Create a user.

6.  Select **Submit**.


### What to do next

Associate an existing user with a consumer record. For more information, see [Associate an existing user with a consumer record](associating-users-to-a-consumer-record.md#).

## Associate an existing user with a consumer record

Associate a user with a consumer record in the Customer Service Management \(CSM\) application. After the association is done, you can access the Consumer Service Portal \(CSP\) as a consumer to search for information, create cases, and more.

### Before you begin

Role required: sn\_crm\_consumer\_data\_manager, sn\_crm\_consumer\_relationship\_data\_manager, sn\_crm\_household\_data\_manager or sn\_crm\_household\_relationship\_data\_manager or sn\_crm\_foundation\_data\_manager, sn\_crm\_foundation\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Consumers**.

2.  Select the consumer from the consumer record.

3.  In the Login Details related list, select the User lookup icon ![Lookup icon.](../image/lookup-list.jpg) to open the list of sys\_users.

4.  On the Users form, select the user to associate with the consumer record.

    **Note:** If the unified consumer is activated, you can select the user type from the interceptor form.

5.  Select **Save**.


### Result

The sys\_user is associated with the consumer record. You can access the Consumer Service Portal \(CSP\) as a consumer.

