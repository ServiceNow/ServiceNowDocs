---
title: Update a master data record
description: Submit an update request for an existing master data record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-update-record.html
release: australia
topic_type: task
last_updated: "2026-06-26"
reading_time_minutes: 1
keywords: [app, engine, erp, sap, rapid, deployment, pack, data, edit, update]
breadcrumb: [Use, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# Update a master data record

Submit an update request for an existing master data record.

## Before you begin

-   Requestor access to the domain is required.
-   The record must already exist in the system, either approved from an earlier create request or preloaded from your ERP system.
-   Only records that have been approved are available for update.

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

4.  Select **Update Record**.

5.  Select **Proceed**.

6.  Search for the record to change.

    Use the lookup interface to search by a record parameter, such as customer name, copy code, or distribution status.

7.  Find the record to edit and in the **Action** column select **Update**.

    \[Omitted image "aes-erp-rdp-update-record.png"\] Alt text: Update customer record list with action column highlighted.

8.  Modify the record information.

    The system tracks each change so that approvers see the old and new values.

9.  When finished, select **Submit request**.


## Result

The request flows through the enrichment, governance, and approval stages.

**Parent Topic:**[Using App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-use.md)

