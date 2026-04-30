---
title: Create contact import rules
description: Create a contact import rule to apply on the User table and filter out users as contacts for emergency notifications.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create contacts for emergency notifications, Setup steps for emergency notification, Integrating Crisis Management with Everbridge, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create contact import rules

Create a contact import rule to apply on the User table and filter out users as contacts for emergency notifications.

## Before you begin

Role required: BCM admin \(sn\_bcm.admin\)

## About this task

The contact import rule is applied on the default table that is the User table \[sys\_user\]. The unique user reference that is the sys\_id of the user table and the unique contact ID of the Contacts table that is synced with Everbridge are mapped.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Everbridge Contact Configuration** &gt; **Contact Import Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the import rule.|
    |Table|Defaults to the User table \[sys\_user\]|
    |Filter condition|Condition applied on the User table to filter records.|
    |Record type|Default category of the record type.|
    |User mapping|Unique user reference from the Users table.|
    |Contact ID mapping|Unique ID of each contact used to sync with Everbridge.|

4.  Click **Submit**.


