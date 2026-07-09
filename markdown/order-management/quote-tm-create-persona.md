---
title: Create a transaction persona
description: Create a persona in ServiceNow Quote Experience to define a user type and assign user accounts to it in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-create-persona.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Personas, Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a transaction persona

Create a persona in ServiceNow Quote Experience to define a user type and assign user accounts to it in ServiceNow CPQ.

## Before you begin

User accounts to assign to the persona must be created in the User Access function in Utilities before they can be assigned to a persona.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** &gt; **Personas**.

2.  Select **+ New Persona**.

3.  In the **Name** field, enter the name of the new persona.

    The name is mirrored in the **Variable Name** field in camel case with spaces and special characters removed. For example, entering `Eastern Sales Manager` produces the variable name **easternSalesManager**. To use a custom variable name, select the pencil icon to the right of the **Variable Name** field.

4.  Select **Save**.

5.  Select **+ Associate User** to assign user accounts to the persona.

    The **Associate Users** control appears, listing user accounts eligible for assignment.

6.  Select the check box next to each user account to assign, then select **Done**.

    Each user account can be assigned to only one persona in ServiceNow Quote Experience.

7.  When prompted to confirm the assignment, select **Confirm**.

    The assigned user accounts appear in the **Username** list for the persona. To see the new persona in the Personas list, select **Personas** in the admin menu.


## What to do next

Assign the persona to a view to define its field and event access at each stage. For more information, see [Create a transaction view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-configure-view.md).

