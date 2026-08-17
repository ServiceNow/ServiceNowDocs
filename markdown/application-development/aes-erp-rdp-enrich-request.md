---
title: Enrich a master data request
description: Add supplementary details to master data requests to prepare each record for governance review and approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-enrich-request.html
release: australia
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
keywords: [app, engine, erp, sap, rapid, deployment, pack, add, data]
breadcrumb: [Use, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# Enrich a master data request

Add supplementary details to master data requests to prepare each record for governance review and approval.

## Before you begin

Domain access is determined by your administrator.

Role required: An MDM Orchestrator enricher role. \(For more information, see [Roles used in App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-components-installed.md).\)

## Procedure

1.  In the menu bar, select **Workspaces** &gt; **MDM Orchestrator Dashboard**.

    The dashboard displays pending enrichment requests, SLA breach indicators, in-progress tasks, and a list of the enrichment records assigned to you.

2.  In **My Team Recent Requests**, select a request.

    \[Omitted image "aes-erp-rdp-enrich1.png"\] Alt text: MDM Orchestrator dashboard with my team recent requests list highlighted.

    The record displays the details submitted by the requestor, any attachments, the duplicate-check result, and the fields designated for enrichment.

3.  Add the enrichment data.

    Enrichers typically add data from external or supplementary sources. For a customer record, this might include a company code, a credit score, the legal entity, or an industry classification.

    \[Omitted image "aes-erp-rdp-enrich2.png"\] Alt text: Single record with fields for enricher to add information.

4.  Select **Save**.

    Saving does not advance the request. You can return and edit the enrichment fields.

5.  When finished, select **Complete Request**.


## Result

A governance user performs compliance checks before the record is sent to the approver. For information about the governance stage, see [Governance review](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-governance-review.md).

**Parent Topic:**[Using App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-use.md)

