---
title: Update company profile using the supplier catalog
description: Update the company profile when the details about your company change.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/update-supp-profile.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Raising requests, Using Supplier Collaboration Portal, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Update company profile using the supplier catalog

Update the company profile when the details about your company change.

## Before you begin

Role required: sn\_slm.contact

## Procedure

1.  Navigate to the Supplier Collaboration Portal home page by accessing your instance URL and adding a /supplier suffix.

    For example, `https://example.com/supplier`.

2.  Select the supplier from the **My Company** drop-down list of suppliers associated with your profile.

    **Important:** The list of suppliers under **My Company** is available from the Xanadu December 2024 release onwards, only if **M2M mapping between supplier contact and suppliers** is enabled.

3.  Do one of the following:

    -   In the portal header, select **Raise a request**, and then select the **Update profile details** catalog item under the General category.
    -   In the portal header, select **My Company**, and then select **Request Change** on the Company Profile page.
4.  On the Update profile details form, fill in the fields.

    For more information about the form fields and descriptions, see [Update profile details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/update-supp-profile-form.md).

5.  Select **Submit**.


## Result

The application creates a case and assigns it to the supplier manager for review and approval.

After the Supplier Manager approves the case, the company profile details are updated in the supplier record.

**Parent Topic:**[Raising requests from the Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/supp-catalog-req.md)

**Related topics**  


[Add or remove a supplier location using the supplier catalog]()

[Add a supplier contact using the supplier catalog]()

[Remove a supplier contact using the supplier catalog]()

[Ask a question using the supplier catalog]()

[Submit an idea using the supplier catalog]()

[Submit an issue using the supplier catalog]()

[Update banking details using the supplier catalog]()

[Request elevated access]()

[Update default supplier]()

[Request something else using the supplier catalog]()

[Raising requests from the Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/supp-catalog-req.md)

