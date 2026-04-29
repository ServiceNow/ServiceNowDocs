---
title: Transaction Manager: Personas
description: Personas let you customize user access according to users' business roles.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager: Personas

Personas let you customize user access according to users' business roles.

Transaction Manager uses personas to define distinct user types and roles that you find in your sales organization. Personas might include a sales rep persona or a sales manager persona.

Each persona has customized access to data, including what users with a persona can view and edit, and how the layout appears in each stage of a transaction’s life cycle. This lets an admin define how different users experience a transaction based on their roles in the sales organization.

**Note:** Because personas are not part of the Transaction Manager blueprint, they are not part of the blueprint export file. When a blueprint is migrated to a new system, personas must be recreated.

## Creating a persona

To create a persona, follow these steps:

1.  In Transaction Manager Admin, click **Personas**.

    ![Transaction Manager Admin UI](../images/cpq-txn-mgr-stages-persona-1.jpeg)

2.  Click **+ New Persona**.

    ![New persona](../images/cpq-txn-mgr-stages-persona-2.jpeg)

    To assign user accounts to a persona, they must have been created by means of the User Access function in Utilities. User accounts that are not listed in the User Access list cannot be assigned to a persona. For more information on granting user access in CPQ, see [User access](please_share_your_feedback_on_admin_assist_responses.md).

3.  A persona requires a name and a variable name. Enter the name of the new persona in the **Name** field.

    As the name is entered, it is mirrored in the **Variable Name** field. By default, the variable name is the same as the entered name, but in camel case with all spaces and special characters removed. For example, if you enter the name "Eastern Sales Manager", the automatically entered variable name is "easternSalesManager". To create a custom variable name, click the pencil icon to the right of the variable name field and enter your own value. When you're finished, click **Save**.

    ![New persona](../images/cpq-txn-mgr-stages-persona-3.jpeg)

4.  To assign one or more user accounts to the new persona, click **+ Associate User**.

    ![Sales Manager](../images/cpq-txn-mgr-stages-persona-4.jpeg)

    An **Associate Users** control appears and lists the user accounts that can be assigned to the new persona.

5.  Click the check box next to each user account that you want to assign to the new persona, and then click **Done**..

    **Note:** Each user account can be assigned to only one persona in Transaction Manager.

6.  When you are asked to confirm that you want to assign the selected user accounts to this persona, click **Confirm**.

    ![Associate confirmation](../images/cpq-txn-mgr-stages-persona-5.jpeg)


The assigned user accounts appear in the **Username** list for the new persona. To see your new persona on the Personas page, click **Personas** in the Admin menu.

![Persona](../images/cpq-txn-mgr-stages-persona-6.jpeg)

