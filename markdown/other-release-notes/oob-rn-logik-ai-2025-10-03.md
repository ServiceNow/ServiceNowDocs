---
title: Logik.ai 2025/10/03 release notes
description: Logik.ai 2025/10/03 release notes include new enhancements and bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-10-03.html
release: other
topic_type: reference
last_updated: "2026-06-02"
reading_time_minutes: 2
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/10/03 release notes

Logik.ai 2025/10/03 release notes include new enhancements and bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, October 02, 2025, 8 pm CT|
|Test|Thursday, October 16, 2025, 8 pm CT|
|Prod|Friday, November 07, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Friday, November 07, 2025.

## Release notes

This release version includes the following new enhancements and fixes.

## Transaction Manager: Dynamic picklists - uses values from a Managed Table

A Managed Table can be set up and updated in real time to power the values available in the Picklist UI element. This enables picklists to always show the latest options and is suitable for data that changes often. Any static picklist can be swapped to dynamic through a simple setting change in the admin.

## Transaction Manager: Transaction Statistics API - sessions and views by user, average time per stage

A new endpoint returns bulk or individual statistics on transactions within a date range, enabling admins to measure performance of their Transaction Manager experience.

The date range parameters specify a `toDate` and `days` value, which retrieves statistics from `(toDate - days)` to `toDate`.

Example call:

```
{{baseUrl}}/api/txn/metrics/v1/overview?txnId={{transactionId}}&days=30&toDate=2025-09-18T15:28:04Z
```

## Salesforce RCA

Salesforce deprecated the PlaceQuote API, which allowed users to create and update quote lines from Logik.ai in newer Salesforce release versions. The PlaceQuote API is now refactored into the Revenue Sales Transaction API, which is supported for newer versions of Salesforce.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-18542|Fixed error where set size changes during On Configure/Reconfigure Enrichment were not taking effect at runtime|
|LGK-18757|Fixed issue with Set CSV Upload where a BOM item was not removed after the CSV upload|
|LGK-19000|Fixed issue where rapid patch calls to change field values led to inaccurate BOM responses in some scenarios|
|LGK-19002|Fixed issue where the logo and buttons were shown before the layout loaded when launching the configurator from ServiceNow|
|LGK-19031|Fixed issue where Available mode in Transaction Manager did not work intermittently|
|LGK-19069|Resolved integration issue with Threekit Visualizer that caused failure to load on initialization|
|LGK-19085|Fixed issue where the magnifier glass button for the image viewer was not displaying appropriately|
|LGK-19221|Fixed issue where certain buttons were not responsive in mobile view for embedded layouts in a web component|
|LGK-19259|Added capability to allow tagging via Admin API|
|LGK-19291|Added ability for Solution Config to stay active while any child blueprint is being configured, even if other blueprints have passed the timeout|
|LGK-19434|Fixed issue where rules search blueprint ingestion was failing due to data inconsistencies|
|LGK-19440|Fixed issue where Flightpath UI was missing in the Config header under some scenarios|
|LGK-19450|Fixed issue where the validation button on transaction configuration was missing|
|LGK-19460|Fixed issue causing Connection Pool Shut Down errors during high load|
|LGK-19652|Fixed error where enabling AI rule search in config blueprint caused an initialization error|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

