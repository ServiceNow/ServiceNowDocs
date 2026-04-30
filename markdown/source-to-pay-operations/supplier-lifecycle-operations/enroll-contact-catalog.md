---
title: Add a supplier contact using the supplier catalog
description: Add the supplier contacts so that they can access the Supplier Collaboration Portal and start working on the assigned tasks.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Raising requests, Using Supplier Collaboration Portal, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Add a supplier contact using the supplier catalog

Add the supplier contacts so that they can access the Supplier Collaboration Portal and start working on the assigned tasks.

## Before you begin

Role required: sn\_slm.contact or sn\_slm.admin

Only primary contacts can enroll a new user from the supplier catalog.

## Procedure

1.  Navigate to the Supplier Collaboration Portal home page by accessing your instance URL and adding a /supplier suffix.

    For example, `https://example.com/supplier`.

2.  Select the supplier from the **My Company** drop-down list of suppliers associated with your profile.

    **Important:** The list of suppliers under **My Company** is available from the Xanadu December 2024 release onwards, only if **M2M mapping between supplier contact and suppliers** is enabled.

3.  In the portal header, select **Raise a request**.

4.  Under the General category, select the **Enroll a new user** catalog item.

    The **Supplier** field is auto-populated with the supplier you have currently selected. This field is available from the Xanadu December 2024 release onwards.

5.  Select **Add**.![Selected button for adding a new row that contains details of the supplier contact.](../image/add-supplier-contact-supplier-collaboration-portal.png)

    The Add Row dialog box is displayed.

6.  In the **Email** field, enter the email address of the contact.

7.  From the Primary contact list, select one of the following:

    -   **Yes**: Select this option to specify that the contact you’re adding is a primary contact.
    -   **No**: Select this option to specify that the contact you’re adding is not a primary contact.
8.  Select **Add**.

9.  Repeat steps 4 through 8 to add additional contacts in multiple rows.

10. To remove all the added rows for contacts, select **Remove All**.

    A confirmation message is displayed.

11. Select **Remove**.

    All the supplier contact rows are removed.

12. Select **Submit**.


## Result

The application creates a case of type Enroll new supplier user and assigns it to the supplier manager to take the appropriate action.

**Parent Topic:**[Raising requests from the Supplier Collaboration Portal](../concept/supp-catalog-req.md)

**Related topics**  


[Add or remove a supplier location using the supplier catalog](submit-add-remove-supploc.md)

[Remove a supplier contact using the supplier catalog](remove-contact-catalog.md)

[Ask a question using the supplier catalog](submit-question.md)

[Submit an idea using the supplier catalog](submit-idea.md)

[Submit an issue using the supplier catalog](submit-issue.md)

[Update banking details using the supplier catalog](update-supp-banking-info.md)

[Update company profile using the supplier catalog](update-supp-profile.md)

[Request elevated access](request-elevated-access.md)

[Update default supplier](update-default-supplier.md)

[Request something else using the supplier catalog](submit-general-request.md)

[Raising requests from the Supplier Collaboration Portal](../concept/supp-catalog-req.md)

