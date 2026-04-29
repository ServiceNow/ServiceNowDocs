---
title: Configure tables to work with guests
description: If you want guest users to be able to interact with data within a table on your ServiceNow instance, you must configure the table to be guest accessible.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Interact with table data in a ServiceNow instance, Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Configure tables to work with guests

If you want guest users to be able to interact with data within a table on your ServiceNow instance, you must configure the table to be guest accessible.

## Before you begin

Role required: admin

## Procedure

1.  Create a Public Pages \(sys\_public\) record for the table that you want to enable public access for.

    1.  In the **All** tab search bar, enter `sys_public.do`.

    2.  In the **Page** field, enter the name of the table for which to add public access.

        ![Public Page record](../../image/mob_sdk-set-public-page.png)

    1.  Select **Submit.**

2.  Ensure the public role is enabled for the table.

    1.  Navigate to the table for which you want to allow guest \(public\) access, **All → System Definition → Tables**, select the table.

    2.  Select the **Controls** tab.

    3.  Under the **Security Rules \(ACLs\)** section, ensure **Create access controls** is selected and that **User role** contains `public`, if not, add them.

3.  Create the public ACL for each of the CRUD operations that you want to enable guest access for.

    There must already be ACLs specified for each of the CRUD operations for which you are adding public access. If not, you need to create these ACLs also. To do this, follow the instructions below, but don't add the "\*" in the second part of the **Name** field and don't add the public role to the required roles.

    1.  Select the **Access Controls** tab.

    2.  Select **New**.

    3.  Enter the following values:

        |Field|Value|
        |-----|-----|
        |Type|record|
        |Application|Global|
        |Operation|&lt;Operation for which you want to allow guest access, such as read or write&gt;|
        |Name \(first part\)|&lt;Name of the table that you want to provide guest access for&gt;|
        |Name \(second part\)|\*|

    4.  In **Requires role**, insert a new row and select the `public` role.

        ![Adding guest user ACLs](../../image/modsdk-table-guest-user-access.png)

4.  Select **Submit** to save your changes.

    When complete, there should be two ACLs for each guest user \(public\) CRUD operation. One with a ".\*" at the end of the table name and one without. ![Successful guest CRUD operations](../../image/mob_sdk-public-CRUD-ops.png)


