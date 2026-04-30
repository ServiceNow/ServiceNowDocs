---
title: Add or remove a supplier location using the supplier catalog
description: Submit a request to add a new supplier location or remove an existing one to keep the supplier information up to date.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Raising requests, Using Supplier Collaboration Portal, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Add or remove a supplier location using the supplier catalog

Submit a request to add a new supplier location or remove an existing one to keep the supplier information up to date.

## Before you begin

Role required: sn\_slm.contact

## About this task

-   If a supplier has multiple locations, at least one location should be set as headquarters.
-   If a new supplier location is set as headquarters \(HQ\) or if any updates are made to the existing HQ supplier location, the location details of the HQ supplier location are updated in the supplier record.
-   When you update the supplier location details in a supplier record, the location details are updated in the supplier location record as well.

## Procedure

1.  Navigate to the Supplier Collaboration Portal home page by accessing your instance URL and adding a /supplier suffix.

    For example, `https://example.com/supplier`.

2.  Select the supplier from the **My Company** drop-down list of suppliers associated with your profile.

    **Important:** The list of suppliers under **My Company** is available from the Xanadu December 2024 release onwards, only if **M2M mapping between supplier contact and suppliers** is enabled.

3.  In the portal header, select **Raise a request**.

4.  Under the General category, select the **Update location details** catalog item.

    The **Supplier** field is auto-populated with the supplier you have currently selected. This field is available from the Xanadu December 2024 release onwards.

5.  In the Add new or remove drop-down list, select one of the following:

    -   **Add location**
    -   **Remove location**
6.  In the **Select a location** search field, search for and select a supplier location.

    **Note:** You cannot remove a location whose category is set to **Headquarters**.

7.  From the **Category** drop-down list, select a category for the supplier location.

    -   **Contracting address**
    -   **Delivery address**
    -   **Facility \(default\)**
    -   **Headquarters**
    -   **Invoice address**
    -   **Service center**
    You can select multiple values from the drop-down list.

8.  If you do not find the required supplier location in the **Search a location** search field, select the **Add new** check box.

9.  On the Supplier Location form, fill in the fields.![Filled-in form for updating location details.](../image/add-location-supplier-collaboration.png)

    For a description of the field values, see [Add New Location form](../reference/supplier-location-form.md).

10. Select **Submit**.


## Result

The application creates a case and assigns it to the supplier manager for review and approval.

After the supplier manager approves the case, the supplier record is updated accordingly.

**Parent Topic:**[Raising requests from the Supplier Collaboration Portal](../concept/supp-catalog-req.md)

**Related topics**  


[Add a supplier contact using the supplier catalog](enroll-contact-catalog.md)

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

