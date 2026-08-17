---
title: Create a journal entry
description: Create, validate, and submit journal entries for month-end account closing. The workflow verifies that debit and credit amounts balance before entries reach governance and approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-use-journal-entry.html
release: australia
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 1
keywords: [app, engine, erp, sap, rapid, deployment, pack, approval, hub]
breadcrumb: [Use, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# Create a journal entry

Create, validate, and submit journal entries for month-end account closing. The workflow verifies that debit and credit amounts balance before entries reach governance and approval.

## Before you begin

-   You must have access to create journal entries.
-   Prepare a general ledger \(GL\) entry file containing the journal lines. The file typically includes the account code, debit amount, credit amount, description, and optional reference fields.

Role required: An MDM Orchestrator journal entry role. \(For more information, see [Roles used in App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-components-installed.md).\)

## Procedure

1.  Navigate to **All** &gt; **Journal Entry**.

2.  Select **New Journal entry**.

3.  Select a **Journal Type**.

4.  In **Attachments**, select **Select file** and upload the prepared journal entry file.

    After upload, individual fields are filled in with information from the file.

    \[Omitted image "aes-erp-rdp-journal-entry2.png"\] Alt text: Journal entry task records with fields containing information from attached file.

    A validation is performed automatically to check that total debits equal total credits. If they match, validation passes. If they don't, the system shows the sum of debits, the sum of credits, and the difference. Correct the journal lines by adjusting individual amounts until the totals match.

    When balanced, the journal task status changes to **Validated**. An approval task is created automatically and assigned to an approver. The journal task status changes to **Submitted for Approval**.


## Result

The approver reviews the request. For the approval steps, see [Approve or reject requests in Approval Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-approve-request.md). After approval, the journal entry is posted to the GL in the connected ERP system. If rejected, the task returns to the creator with a rejection reason for correction and resubmission.

**Parent Topic:**[Using App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-use.md)

