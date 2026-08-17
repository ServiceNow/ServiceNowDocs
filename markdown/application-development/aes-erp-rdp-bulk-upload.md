---
title: Bulk upload master data records
description: Submit multiple master data requests in a single batch by importing a spreadsheet.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-bulk-upload.html
release: australia
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
keywords: [app, engine, erp, sap, rapid, deployment, pack, upload, multiple]
breadcrumb: [Use, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# Bulk upload master data records

Submit multiple master data requests in a single batch by importing a spreadsheet.

## Before you begin

Requestor access to the domain is required. A spreadsheet with record data in the format provided by the template must be prepared.

Role required: An MDM Orchestrator bulk upload requestor role. \(For more information, see [Roles used in App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-components-installed.md).\)

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

4.  Select **Bulk Upload**.

5.  Select **Proceed**.

6.  Select **Download Template** to get a spreadsheet with the correct column headers for your domain.

    \[Omitted image "aes-erp-rdp-bulk-upload1.png"\] Alt text: Download template option.

7.  Find and open the downloaded spreadsheet.

8.  For each record to create:

    -   Use one row.
    -   Complete the required fields.
    -   Leave optional fields empty.
    \[Omitted image "aes-erp-rdp-bulk-upload2.png"\] Alt text: Sample spreadsheet showing information in two rows and several columns.

9.  Save the spreadsheet with an appropriate name.

10. Return to the MDM Orchestrator in your instance.

11. Upload the completed file.

12. Select **Process Upload**.

    \[Omitted image "aes-erp-rdp-bulk-upload3.png"\] Alt text: Upload data option.

13. Select **Proceed**.

    Each record in the file is validated.

14. Review the validation results.

    -   Valid records are accepted and continue through the workflow.
    -   Invalid records \(missing required fields or incorrect formatting\) are rejected and removed from the batch. Valid records in the same file are unaffected.
15. Select **Proceed** to submit all valid records.


## Result

The records flow through the same enrichment, governance, and approval stages as individual create requests.

## What to do next

If records were rejected, correct the file and upload it again as a new bulk request. Each upload is treated as a separate request.

**Parent Topic:**[Using App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-use.md)

