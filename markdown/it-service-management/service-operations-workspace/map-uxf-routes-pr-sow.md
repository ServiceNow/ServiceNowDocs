---
title: Map the UXF routes
description: Create a route for the verification method to map the verification process.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure verification methods, Setting up Service Desk assisted Password Reset in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Map the UXF routes

Create a route for the verification method to map the verification process.

## About this task

The administrator can customize the verification page at the specified route. The UI page should be configured with a verification type that allows the service desk agent to verify the identity of the user requesting a password reset.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Overview**.

2.  On the **Admin Center** page, do one of the following:

    -   In the **Overview** tab, select the **Configure** button in the **Service Desk Assisted Password Reset** card.
    -   In the **Configurations** tab, select **Service Desk Assisted Password Reset** card.
3.  On the **Verification Settings** card, select **UXF routes mapping**.

    The default UXF routes are displayed.

4.  Select **New** to create a new UXF route.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Order|Order of the UXF route|
    |Workspace|Option where the UXF route will be applicable to. If there is no value in this field, the system picks the Workspace as Service Operations Workspace.|
    |Verification type|Verification type to authenticate the user during the password reset process.|
    |Route|Path for the code to reach the destination.|

6.  Select **Submit**.


**Parent Topic:**[Configure the verification methods for service desk process in Service Operations Workspace](../concept/configuring-verification-methods-pr-sow.md)

