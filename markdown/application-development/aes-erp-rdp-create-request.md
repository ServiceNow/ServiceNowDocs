---
title: Create master data requests
description: Submit a request to create a master data record, such as a customer, business partner, material, cost center, location, or bill of materials record, in MDM Orchestrator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-create-request.html
release: australia
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
keywords: [app, engine, erp, sap, rapid, deployment, pack, request]
breadcrumb: [Use, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# Create master data requests

Submit a request to create a master data record, such as a customer, business partner, material, cost center, location, or bill of materials record, in MDM Orchestrator.

## Before you begin

Role required: An MDM Orchestrator requestor role. \(For more information, see [Roles used in App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-components-installed.md).\)

## Procedure

1.  Navigate to **All** &gt; **MDM Orchestrator** &gt; **MDM Requestor Portal**.

    \[Omitted image "aes-erp-rdp-requestor-dashboard.png"\] Alt text: Requestor dashboard showing charts and graphs with request information.

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

4.  Select **Create Record**.

5.  Select **Proceed**.

    The form displays the fields for the selected domain, organized into persona-specific sections.

6.  Complete the request form.

    Fill in only the required fields to submit the request. Enrichers and governance users add further detail in later stages.

    \[Omitted image "aes-erp-rdp-create1.png"\] Alt text: New customer request form filled in with information including customer name, division, and payment terms.

7.  Attach supporting documents, for example, proof of incorporation or tax documents.

8.  Save or submit the record.

    -   Select **Save as Draft**, enter a name, and select **Save**.
    -   Select **Submit** to send the request to the next stage.

## Result

If you saved the draft and want to edit the information, navigate to **All** &gt; **MDM Orchestrator** &gt; **MDM Requestor Portal** and select the my requests icon \[Omitted image "aes-erp-rdp-my-requests.png"\].

If you submitted the request, a deduplication agent runs automatically to find potential duplicates before the request advances. Request details are displayed, including a progress indicator, activity stream, attachments, the duplicate check result, and creation information. For more information, select **View full details**. Depending on the domain configuration, the request routes to an enricher, then to a governance user, and finally to an approver in Approval Hub. Track progress by navigating to **All** &gt; **MDM Orchestrator** &gt; **MDM Requestor Portal** and selecting the my requests icon \[Omitted image "aes-erp-rdp-my-requests.png"\].

**Parent Topic:**[Using App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-use.md)

