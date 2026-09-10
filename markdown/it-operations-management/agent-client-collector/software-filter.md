---
title: Software filter
description: The Software filter lets you define rules to automatically exclude irrelevant entries from your Software Asset Management \(SAM\) inventory. At the same time, it keeps a complete, auditable record of everything filtered so that nothing disappears silently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/software-filter.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Software Asset Management, SAM, inventory, filter, Agent Client Collector]
breadcrumb: [ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Software filter

The Software filter lets you define rules to automatically exclude irrelevant entries from your Software Asset Management \(SAM\) inventory. At the same time, it keeps a complete, auditable record of everything filtered so that nothing disappears silently.

Discovery and the Agent Client Collector regularly report every application installed on a device. However, not everything found is meaningful licensing or asset-management software. For example, Operating-system shortcuts, Progressive Web App \(PWA\) stubs, Citrix Receiver placeholder entries, browser-extension shortcuts, and similar artifacts are frequently reported as installed software. However, they aren't applications your organization is licensing, tracking, or reconciling.

## Software filter - Benefits

-   Cleaner license reconciliation. Irrelevant entries no longer inflate install counts or trigger false compliance findings.
-   Less manual clean-up. You no longer must search for and deactivate the same irrelevant software records after every discovery cycle.
-   Full transparency. Every exclusion is logged, so you can see what was filtered, when, and by which rule.

## How filtering works

Agent scans and background discovery runs produce software installs on devices in your network. Each item is checked against the set of currently active filter rules before it is written to your SAM software inventory.

-   If an item matches an active rule, it is excluded from the SAM inventory and a record of the exclusion is written to the review table instead.
-   If an item matches no active rule, it flows through to your SAM inventory as normal. Nothing changes for software that is relevant to you.
-   If the same software is reported again on a later scan, its existing review record is refreshed, not duplicated. The review table reflects the latest confirmation date rather than growing indefinitely.

A single malformed rule \(for example, an invalid pattern\) is skipped and logged rather than blocking the rest of the check. One bad rule doesn't accidentally exclude everything.

For details on the tables that determine which entries are labeled as irrelevant, see [Software filter tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/sw-filter-tables.md).

## Modifying rules

If you deactivate or edit a custom rule, the behavior of excluded software changes on the next discovery scan:

-   Software that no longer matches any active rule stops being excluded and flows into your SAM inventory as normal.
-   Entries for filtered software remain in the Software Install Filter Staging table as a historical record, but are no longer refreshed with new confirmation dates.
-   If you reactivate the rule or change it to match the software again, exclusion resumes on the next scan and the staging table entry is refreshed.

-   **[Create a custom filter rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/create-custom-filter-rule.md)**  
Create a custom filter rule in the Software Install Custom Filter table \(samp\_sw\_install\_custom\_filter\). Rules determine the criteria by which software is excluded from your Software Asset Management \(SAM\) workspace.
-   **[Review filtered software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/review-filtered-software.md)**  
Review the entries in the Software Install Filter Staging table \(samp\_sw\_install\_filter\_staging\) to confirm your rules are filtering only the software you expect.

**Parent Topic:**[Agent Client Collector deployment - shared between servers and endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-shared-deployment.md)

