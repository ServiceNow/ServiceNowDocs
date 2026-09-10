---
title: Meter-based guardrails and controls
description: Meter-based guardrails and controls help you in identifying situations when you unexpectedly exceed your entitled record count.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/meter-based-guardrails.html
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-08-18"
reading_time_minutes: 2
keywords: [process mining, guardrails, entitlement, meter-based]
breadcrumb: [Use, Process Mining, Platform Analytics]
---

# Meter-based guardrails and controls

Meter-based guardrails and controls help you in identifying situations when you unexpectedly exceed your entitled record count.

## How it works

There are two types of guardrails:

-   Table-level guardrails: An administrator can define one mandatory filter condition per table \(for example, "only cases resolved in the last 12 months"\). Once active, this condition is automatically applied to every project built on that table. The person creating the project can add their own filters on top, but can't remove or edit the administrator's condition.
-   Entitlement enforcement: This only applies if your subscription uses a meter-based or AI Native SKU. If you're on a different license type, the platform's existing licensing checks apply instead.

    When you mine a project, the system checks your project's scope against your remaining entitlement:

    -   If the project's total record count already exceeds your entitlement, mining is blocked.
    -   If you've already used your full entitlement for the current contract period, mining is blocked, regardless of project size.
    -   If your project uses a crop or transition condition and its record count is more than 5 times your entitlement, mining is blocked.
    -   In every other case, mining is allowed.

## How your usage is measured and reported

An administrator can override the block entirely using the system property \(promin.metered\_usage.allow\_unrestricted\). This disables entitlement checks and allows unrestricted mining \(with the understanding that overages will be billed at the end of the contract period\). For more information on promin.metered\_usage.allow\_unrestricted, see [Process Mining properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/components-installed.md).

If mining is allowed but the results would put you over your entitlement for the first time, the system doesn't charge you for the overage. It counts records toward your usage only up to your remaining entitlement, and quietly discards the rest. The next time you try to mine, you will have 0 remaining records and will be blocked.

If you're on the AI Native SKU, your consumption is tracked per table, per day; not just as a single monthly total. This gives you visibility into which tables \(and by extension, which departments or use cases\) are driving your consumption. This is useful if your organization mines records across multiple areas, such as ITSM and HR, at the same time.

Your usage resets on your contract anniversary date. The date your current contract term began, recalculated each year your contract renews, rather than on a rolling 365-day lookback. This is the same anniversary date used to determine your remaining entitlement when you mine a project.

If your project uses a crop or transition condition, only the records that remain after that condition is applied count toward your usage.

-   **[Create a table-level guardrail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/create-guardrail.md)**  
Define a mandatory filter condition for a table to prevent projects from being configured in ways that consume more mining capacity than necessary.

**Parent Topic:**[Using Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/use-process-mining.md)

**Related topics**  


[Create a table-level guardrail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/create-guardrail.md)

