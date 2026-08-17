---
title: Logik.ai 2026/07/10 release notes
description: Logik.ai 2026/07/10 release notes include new enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2026-07-10-.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 2
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2026/07/10 release notes

Logik.ai 2026/07/10 release notes include new enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Jul 09, 2026, 8 pm CT|
|Test|Thursday, Jul 09, 2026, 8 pm CT|
|Prod|Friday, Jul 17, 2026, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Jul 17, 2026.

## Release notes

This release version includes the following new enhancements and fixes.

## Transaction Manager: Headless API for Custom UIs

Transaction Manager now exposes a buyside API for retrieving transaction line data — including field visibility and editability — so you can build custom, composable user interfaces on top of Transaction Manager that respect runtime personas.

## ServiceNow Web Component: No Hard Refresh Required

When the Logik.ai web component is updated in the ServiceNow embedded experience, the latest version is now loaded automatically. Users no longer need to perform a hard refresh to pick up the newest build.

## Early Renewal of Ramped Subscriptions

You can now perform early renewals of ramped subscriptions, giving greater flexibility when managing subscription lifecycles.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|PRB1976997|Fixed a UI display issue when viewing configurations within Transaction Manager.|
|PRB1984033|Resolved issue where exporting individually selected fields could fail.|
|PRB1994491|Fixed a crash that occurred when importing a Set CSV containing fewer columns than expected.|
|PRB1997355|Fixed error when adding a new entry in a determination bulk action.|
|PRB1997884|Fixed issue in the Logik Shopify app where integers divisible by ten were converted to floats, causing errors|
|PRB2011990|Improved text entry responsiveness in Product Pickers.|
|PRB2012081|Fixed issue where Currency-type ProductList columns did not render for advanced ProductLists.|
|PRB2013973|Resolved page-unresponsive error that some users encountered when configuring from Transaction Manager.|
|PRB2019719|Fixed Blueprint Migration and Field Upload skipping product picker bulk-action columns that shared the same name.|
|PRB2030710|Improved validation messaging for incorrectly structured product picker imports.|
|PRB2034523|Fixed issue where quantity was not updated on recall.|
|PRB2035132|Resolved inconsistent aggregate behavior across environments.|
|PRB2035440|Fixed alignment issue when cloning a transaction.|
|PRB2035515|Fixed display issue with the UI layout header logo.|
|PRB2039461|Fixed an issue preventing a class from being saved via the Transaction Manager layout editor.|
|PRB2040660|Fixed alignment of toggle inputs.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

