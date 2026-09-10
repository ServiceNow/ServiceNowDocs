---
title: Case exclusion rules
description: Case exclusion rules let an AP admin define conditions that stop Invoice Case Management from creating a case from an inbound email. Use exclusion rules to filter out emails that don't need agent attention, so that AP agents focus on genuine invoice inquiries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/case-exclusion-rules.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 1
breadcrumb: [Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Case exclusion rules

Case exclusion rules let an AP admin define conditions that stop Invoice Case Management from creating a case from an inbound email. Use exclusion rules to filter out emails that don't need agent attention, so that AP agents focus on genuine invoice inquiries.

## Key benefits

Case exclusion rules provide the following benefits:

-   Reduce email traffic and redundant work by preventing cases for emails that don't require agent action.
-   Keep AP agents focused on the real, necessary invoice inquiry cases.

## How it works

The following points describe how case exclusion rules work:

-   An AP admin defines each rule with a condition builder that evaluates inbound email fields: **Subject**, **Recipients**, **User**, **User ID**, and **Body Text**.
-   When an inbound email matches any active rule, the exclusion engine ignores the email and does not create a case.
-   Exclusion rules apply only to invoice inquiry cases. They don't affect processing cases.

-   **[Create case exclusion rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-case-exclusion-rules.md)**  
Create a case exclusion rule to stop Invoice Case Management from opening a case when an inbound email matches conditions that you define. You can also modify or delete existing rules to keep your email filtering current.

**Parent Topic:**[Work on an invoice processing case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-manual-invoice-ingestion-case.md)

