---
title: Update system property
description: Update the sn\_customerservice.consumer.allowed\_user\_types system property within the Customer Service Management \(CSM\) application to enable the association of consumer records with contact user records or with user records. This modification enables you to display the customer\_contact or sys\_user extension records in the reference list for the users in the csm\_consumer table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User management, Set up your environment, Configure, Customer Service Management]
---

# Update system property

Update the sn\_customerservice.consumer.allowed\_user\_types system property within the Customer Service Management \(CSM\) application to enable the association of consumer records with contact user records or with user records. This modification enables you to display the customer\_contact or sys\_user extension records in the reference list for the users in the csm\_consumer table.

## Before you begin

Role required: admin

## About this task

This property controls the reference qualifier on the user field in the consumer record, determining which user types appear in the lookup.

## Procedure

1.  In the workspace filter navigator, enter sys\_properties.LIST to access the system properties list.

2.  In the **Name** column, use the search field to locate the sn\_customerservice.consumer.allowed\_user\_types system property.

3.  Open the record.

4.  The default value is csm\_consumer\_user, which restricts consumer records to be linked only with consumer user records.

5.  In the **Value** field, add the required user type to the existing default value \( csm\_consumer\_user\).

    **Note:** Add the following based on the requirement:

    |System property|Description|
    |---------------|-----------|
    |customer\_contact|configures a contact as a consumer|
    |sys\_user|configures a user as a consumer|

    For example, value can be: csm\_consumer\_user, customer\_contact

6.  Select **Update**.


## Result

When you navigate to a consumer record and access the **User** field, the reference qualifier displays the following record types:

-   Consumer user records \(existing behavior\)
-   Contact user records \(new capability\), if included customer\_contact, or
-   User records, if included sys\_user

This configuration enables administrators to link a consumer record directly to a contact user record, enabling the unified login experience for users who function as both B2B contacts and B2C consumers.

