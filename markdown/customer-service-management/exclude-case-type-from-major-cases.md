---
title: Exclude a case type from major cases
description: Edit the CSUIActionsImpl script include to exclude specific case types from major case support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/exclude-case-type-from-major-cases.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 1
breadcrumb: [Configure major issue management, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Exclude a case type from major cases

Edit the CSUIActionsImpl script include to exclude specific case types from major case support.

## Before you begin

Role required: admin

## About this task

Onboarding and order cases are excluded by default.

**Important:** Test this change on a subprod instance to verify that it functions correctly. Since this is a customization to a file, your instance can't get future upgrades on the CSUIActionsImpl script include.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Script Includes**.

2.  In the **Script Includes** list, search for **CSUIActions**, and open the **CSUIActions script include**.

3.  In the **Script** section, copy the `//Propose Major Case _145b017f3b230300b5c42479b3efc4f5 : ['csm_order_case', 'sn_onboarding_case'],` code.

    \[Omitted image "proposemajorcase\_script\_include.png"\] Alt text: CSUIActions script include record

4.  Go back to the **Script Includes** list, search for **CSUIActionsImpl**, and open the **CSUIActionsImpl script include**.

5.  Paste the code you copied from the **CSUIActions** script include, and add the case type that you want to exclude.

    \[Omitted image "csuiactionsimpl.png"\] Alt text: CSUIActions script include record

6.  Save the record.

    The case type you added can no longer be proposed as a major case.


