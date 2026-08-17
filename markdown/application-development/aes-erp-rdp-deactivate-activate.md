---
title: Deactivate or activate a master data record
description: Submit a deactivation or activation request for an existing master data record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-deactivate-activate.html
release: australia
topic_type: task
last_updated: "2026-06-26"
reading_time_minutes: 1
keywords: [app, engine, erp, sap, rapid, deployment, pack, data, activate, deactivate, delete]
breadcrumb: [Use, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# Deactivate or activate a master data record

Submit a deactivation or activation request for an existing master data record.

## Before you begin

-   Requestor access to the domain is required.
-   The record must already exist in the system, either approved from an earlier create request or preloaded from your ERP system.
-   Only records that have been approved are available for deactivation or activation.

Role required: An MDM Orchestrator requestor role. \(For more information, see [Roles used in App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-components-installed.md).\)

## Procedure

1.  Navigate to **All** &gt; **MDM Orchestrator** &gt; **MDM Requestor Portal**.

2.  Select **+ Create New Request**.

3.  If you have access to more than one domain, select a domain.

    The domains available depend on your role. You may not see all of these domains. If you only have access to one domain, go to the next step.

    -   **Customer**

        Customer accounts for sales.

    -   **Business Partner**

        Supplier, vendor, or partner organizations.

    -   **Material**

        Inventory items, SKUs, or products.

    -   **Cost Center**

        Financial cost-allocation entities.

    -   **Location**

        Physical or geographic sites.

    -   **Bill of Materials**

        Product component hierarchies.

4.  Select **Deactivate/Activate**.

5.  Select **Proceed**.

6.  Find the record to deactivate or activate and select the check box in the row.

7.  Select **Submit Deactivation** or **Submit Activation**.

    \[Omitted image "aes-erp-rdp-deactivate-activate1.png"\] Alt text: Record list filtered to show active records with a sales organization of north american sales and one record selected.

8.  Add a **Batch Name**.

9.  Add **Supporting Documents**, such as an invoice or merger announcement.

    \[Omitted image "aes-erp-rdp-deactivate-activate2.png"\] Alt text: Confirmation record with batch name specified and one supporting document attached.

10. Select **Proceed &amp; Submit**.


## Result

The request is sent for approval.

**Parent Topic:**[Using App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-use.md)

