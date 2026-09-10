---
title: Create case exclusion rules
description: Create a case exclusion rule to stop Invoice Case Management from opening a case when an inbound email matches conditions that you define. You can also modify or delete existing rules to keep your email filtering current.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/create-case-exclusion-rules.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 1
breadcrumb: [Case exclusion rules, Work on an invoice processing case, Invoice processing cases, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Create case exclusion rules

Create a case exclusion rule to stop Invoice Case Management from opening a case when an inbound email matches conditions that you define. You can also modify or delete existing rules to keep your email filtering current.

## Before you begin

Role required: `sn_ap_cm.admin`

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Administration** &gt; **Invoice case exclusion rules**.

2.  Select **New**.

3.  Complete the exclusion rule fields.

    The **Rule ID** is generated automatically and **Rule Applies To** is set to **Invoice Inquiry Case**. For the full field list, see [Case exclusion reference fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/case-exclusion-reference-fields.md).

4.  In the condition builder, define the conditions that identify the emails to ignore.

    You can build conditions on the following inbound email fields:**Body text**, **Keywords**, **Recipients**, **Subject**, **User**, and **User ID**.

5.  Select **Submit**.


## Result

The rule is saved and the exclusion engine applies on the inbound emails immediately. Inbound emails that match the rule no longer create a case, while all other emails continue to create cases as usual.

## What to do next

To change how an email category is filtered, open the rule and update its conditions, then submit the change. To stop filtering an email category, delete the rule. Modifications and deletions also take effect immediately.

**Parent Topic:**[Case exclusion rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/case-exclusion-rules.md)

