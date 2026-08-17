---
title: Perform a governance review
description: Perform compliance and governance checks on enriched master data records to meet organizational policies before the record reaches the approver.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-governance-review.html
release: australia
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
keywords: [app, engine, erp, sap, rapid, deployment, pack, compliance, conformance]
breadcrumb: [Use, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# Perform a governance review

Perform compliance and governance checks on enriched master data records to meet organizational policies before the record reaches the approver.

## Before you begin

Role required: An MDM Orchestrator governance role. \(For more information, see [Roles used in App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-components-installed.md).\)

## About this task

Review enriched requests that are waiting for governance validation.

## Procedure

1.  In the menu bar, select **Workspaces** &gt; **MDM Orchestrator Dashboard**.

    The dashboard displays pending governance reviews, SLA indicators, in-progress tasks, and a list of enriched records ready for review.

2.  In **My Team Recent Requests**, select a request.

    \[Omitted image "aes-erp-rdp-governance1.png"\] Alt text: MDM Orchestrator dashboard with my team recent requests list highlighted.

    The record displays the original details from the requestor, the data added by the enricher, and the fields designated for governance review.

3.  Review and add governance data.

    Verify that the record meets organizational policies. Governance fields vary by domain but typically include the plant location, an authorization group, a compliance flag, and internal notes for the approver. Governance users typically add one or two fields rather than many data points.

    \[Omitted image "aes-erp-rdp-governance2.png"\] Alt text: Single record with fields for governance user to add information.

4.  Select **Save**.

    Saving does not advance the request. You can return and edit the governance fields.

5.  When finished, select **Complete Request**.


## Result

The request is sent to an approver. The approver can see all information added and edited by the requestor, enricher, and governance reviewer. For the approval steps, see [Approve or reject requests in Approval Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-approve-request.md).

**Parent Topic:**[Using App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-use.md)

