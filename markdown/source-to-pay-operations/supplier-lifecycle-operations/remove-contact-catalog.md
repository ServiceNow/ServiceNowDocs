---
title: Remove a supplier contact using the supplier catalog
description: Remove a supplier contact that you no longer require.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Raising requests from the Supplier Collaboration Portal, Using Supplier Collaboration Portal, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Remove a supplier contact using the supplier catalog

Remove a supplier contact that you no longer require.

## Before you begin

Role required: sn\_slm.contact or sn\_slm.admin

## Procedure

1.  Navigate to the Supplier Collaboration Portal home page by accessing your instance URL and adding a /supplier suffix.

    For example, `https://example.com/supplier`.

2.  Select the supplier from the **My Company** drop-down list of suppliers associated with your profile.

    **Important:** The list of suppliers under **My Company** is available from the Xanadu December 2024 release onwards, only if **M2M mapping between supplier contact and suppliers** is enabled.

3.  In the portal header, select **Raise a request**.

4.  Under the General category, select the **Deactivate user account** catalog item.

    The **Supplier** field is auto-populated with the supplier you have currently selected. This field is available from the Xanadu December 2024 release onwards.

5.  In the **Contact** field, search for and select the contact you want to remove.

6.  In the **Delegate tasks to** field, search for and select a contact to whom you want to reassign the tasks that are currently assigned to the contact being removed.

7.  In the **Reason for offboarding** field, enter the reason for removing the contact.

8.  Select **Submit**.

    The application creates a case of type Offboard supplier contact and assigns it to the supplier manager to take the appropriate action.


**Parent Topic:**[Raising requests from the Supplier Collaboration Portal](../concept/supp-catalog-req.md)

**Related topics**  


[Add or remove a supplier location using the supplier catalog](submit-add-remove-supploc.md)

[Add a supplier contact using the supplier catalog](enroll-contact-catalog.md)

[Ask a question using the supplier catalog](submit-question.md)

[Submit an idea using the supplier catalog](submit-idea.md)

[Submit an issue using the supplier catalog](submit-issue.md)

[Update banking details using the supplier catalog](update-supp-banking-info.md)

[Update company profile using the supplier catalog](update-supp-profile.md)

[Request elevated access](request-elevated-access.md)

[Update default supplier](update-default-supplier.md)

[Request something else using the supplier catalog](submit-general-request.md)

