---
title: Request elevated access
description: Submit a request to gain access to the privileges of the primary contact role.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Raising requests from the Supplier Collaboration Portal, Using Supplier Collaboration Portal, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Request elevated access

Submit a request to gain access to the privileges of the primary contact role.

## Before you begin

Role required: sn\_slm.contact

## About this task

The Request elevated access catalog item is available only to the secondary contact role. A secondary contact is a user that has the Primary contact column set to **false** on the Vendor Contacts page.

## Procedure

1.  Navigate to the Supplier Collaboration Portal home page by accessing your instance URL and adding a /supplier suffix.

    For example, `https://example.com/supplier`.

2.  Select the supplier from the **My Company** drop-down list of suppliers associated with your profile.

    **Important:** The list of suppliers under **My Company** is available from the Xanadu December 2024 release onwards, only if **M2M mapping between supplier contact and suppliers** is enabled.

3.  In the portal header, select **Raise a request**.

4.  Select the **Request an access change request** catalog item under the General category.

5.  In the **Supplier** field, search for and select the supplier.

    The **Supplier** field is auto-populated with the supplier name, but you can change its value, if required.

6.  From the Urgency drop-down list, specify how soon you want the request to completed.

    -   **High**
    -   **Medium**
    -   **Low**
7.  In the **Reason for requesting elevation** field, enter the reason for making this request.

8.  Select the add attachments icon \(![Add attachments icon.](../image/attachments-icon.png)\) to add attachments, such as documents and image files, to the request.

9.  Select **Submit**.

    If more than one primary contact exists for a supplier, then approval tasks are created and assigned to all the primary contacts. When any one of the primary contacts approves or rejects the approval task from the My To-dos page, the approval tasks assigned to the other primary contacts are automatically canceled.

    The secondary contact receives an email notification, regardless of whether the request is approved or rejected.

    After the primary contact approves the request, the secondary contact role is elevated to that of the primary contact.


**Parent Topic:**[Raising requests from the Supplier Collaboration Portal](../concept/supp-catalog-req.md)

**Related topics**  


[Add or remove a supplier location using the supplier catalog](submit-add-remove-supploc.md)

[Add a supplier contact using the supplier catalog](enroll-contact-catalog.md)

[Remove a supplier contact using the supplier catalog](remove-contact-catalog.md)

[Ask a question using the supplier catalog](submit-question.md)

[Submit an idea using the supplier catalog](submit-idea.md)

[Submit an issue using the supplier catalog](submit-issue.md)

[Update banking details using the supplier catalog](update-supp-banking-info.md)

[Update company profile using the supplier catalog](update-supp-profile.md)

[Update default supplier](update-default-supplier.md)

[Request something else using the supplier catalog](submit-general-request.md)

