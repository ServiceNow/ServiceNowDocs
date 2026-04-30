---
title: Transaction Manager: Personas
description: Personas let you customize user access according to the user's business role.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-14"
reading_time_minutes: 2
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Personas

Personas let you customize user access according to the user's business role.

Transaction Manager uses personas to define distinct user types and roles that you find in your Sales organization. Examples of personas might be a sales rep persona or a sales manager persona.

Each persona has customized access to data, including what they can view, edit, and how the layout appears to that user type in each Stage of the transaction’s lifecycle. This lets the administrator define how different users experience the transaction based on their roles in the Sales organization.

**Note:** Personas are not part of the Transaction Manager Blueprint. Therefore, they are not part of a Blueprint export file. Personas would need to be recreated, when a Blueprint is migrated from system to system.

## Creating a persona

To create a persona, follow these steps:

1.  In the Transaction Manager Admin UI click **Personas**.

    ![Transaction Manager Admin UI](../images/cpq-txn-mgr-stages-persona-1.jpeg)

2.  Click **+ New Persona**.

    ![New persona](../images/cpq-txn-mgr-stages-persona-2.jpeg)

    .

    Now that the persona has been created, we need to assign Transaction Manager user accounts to the new persona. In order to assign user accounts to the persona, the user accounts must have previously been created in ServiceNow CPQ via the User Access function in the Utilities area of the Admin UI. If the user accounts are not listed in the User Access list in Utilities then the user accounts will not show up as available to be assigned to a persona. For more information on granting user access in ServiceNow CPQ, see [User access](please_share_your_feedback_on_admin_assist_responses.md).

3.  The persona requires a name and a variable name. Click in the Name field and enter the name of the new persona. As the Name value is being entered in the Name field, the same value is being mirrored in the Variable Name field. By default, Transaction Manager makes the Variable Name the same as the Name value that the Admin enters. The Variable Name however in created using “camel case” and all spaces and special characters are removed from the name. For example, If you type “Eastern Sales Manager” for the Name field, the Variable Name field will contain “easternSalesManager”. If you want to create your own custom Variable Names, click the pencil icon at the right end of the Variable Name field and enter your own value for Variable Name. Once the The Name and Variable Name are set, click **Save**.

    ![New persona](../images/cpq-txn-mgr-stages-persona-3.jpeg)

4.  To assign one or more user accounts to the new persona, click **+ Associate User**.

    ![Sales Manager](../images/cpq-txn-mgr-stages-persona-4.jpeg)

    An Associate Users control slides out from the right of the UI page and lists the available user accounts that can be assigned to the new persona.

5.  Click the checkbox next to each user account you want to assign to the new persona, and when all user accounts are selected, click **Done**..

    **Note:** A user account can be assigned to one and only one persona in Transaction Manager.

6.  When you are asked to confirm that you want to assign the selected user accounts to this persona, Click **Confirm**.

    ![Associate confirmation](../images/cpq-txn-mgr-stages-persona-5.jpeg)


The assigned user accounts will now appear in the Username list for the new persona. To see your new persona listed on the Personas page, click **Personas** in the Admin menu.

![Persona](../images/cpq-txn-mgr-stages-persona-6.jpeg)

