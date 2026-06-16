---
title: Logik.io 2024/11/29 release notes
description: Logik.io 2024/11/29 release notes include new enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-io-2024-11-29.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.io 2024/11/29 release notes

Logik.io 2024/11/29 release notes include new enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Wednesday, Nov 27, 2024, 8 pm CT|
|Test|Thursday, Dec 05, 2024, 8 pm CT|
|Prod|Friday, Dec 20, 2024, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Dec 20, 2024.

## Release notes

This release version includes the following new enhancements and fixes.

## New enhancement: Administration behavior change

When the administrator starts an activity, such as a Blueprint deployment, the Notification Center \(accessible via the bell icon\) logs the activity. A red badge has been added to the bell icon when the activity completes. This change simplifies administration by removing unnecessary requests for attention.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-12032|In certain scenarios, the user's input in the UI was overridden by the enrichment script execution and lost, although it was retained in the back end. This has been resolved.|
|LGK-13629|Full blueprint uploads were taking significantly more time than typical in specific scenarios. This issue was exacerbated with larger blueprints with many fields, field options, and references in scripts. This has been optimized to perform better.|
|LGK-13845|Selecting a valid option when using table-based picklists was throwing an “invalid option selected” error in specific scenarios. This has been fixed.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

