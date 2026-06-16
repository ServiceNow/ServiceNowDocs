---
title: Logik.ai 2025/10/31 release notes
description: Logik.ai 2025/10/31 release notes include new enhancements and bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-10-31.html
release: other
topic_type: reference
last_updated: "2026-06-02"
reading_time_minutes: 2
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/10/31 release notes

Logik.ai 2025/10/31 release notes include new enhancements and bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, October 30, 2025, 8 pm CT|
|Test|Thursday, November 06, 2025, 8 pm CT|
|Prod|Friday, December 05, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Friday, December 05, 2025.

## Release notes

This release version includes the following new enhancements and fixes.

## Tagging and filtering tags in tables

Tagging is now available for Blueprints, Fields, Rules, Managed Tables, and Library Functions. This feature is available and can be enabled through a feature flag. Contact Support to request access.

Key capabilities include:

-   Tag API: Create, view, associate, and de-associate tags.
-   Add tags directly on lines in Field, Rule, and other object table views by double-clicking the tag column on the row.
-   Tag suggestions.
-   Tag-based filtering: Click the header of the tags column to start filtering.

Limitations:

-   Updating existing tag names is not supported.
-   Tags are limited to 80 characters, are case-sensitive, and follow restricted character rules.
-   Filtering is object-type specific; global tag search is not available.

## New line field: txn.line.isNew

A new Boolean system field, `txn.line.isNew`, indicates whether a line is new \(`true`\) or existing \(`false`\). The value is `true` during the operation of the event that created the new line. Use the field in Rule and Rule Groupings associated to Events or Stages to take actions on new lines \(for example, clear discounts on copied lines\). For Reconfigure, only net-new lines return as `true`; existing lines return as `false`.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-19221|Improved UI responsiveness in mobile format|
|LGK-19563|Fixed issue in Transaction Manager with automatically identifying rules associated to a blueprint that referenced fields not associated to the blueprint|
|LGK-19579|Improved performance of copying a Transaction|
|LGK-19610|Fixed issue where reserved words in Data Tables caused problems with queries|
|LGK-19652|Improved data ingestion pipeline for AI Rule Search to handle null fields|
|LGK-19752|Resolved UI misalignment issue on legacy Admin UI|
|LGK-19791|Fixed issue where the BOM did not render in the sidebar for solution config when the Card View type is used|
|LGK-19854/19857|Improved scalability of AI Rule Search for XL blueprints|
|LGK-19923|Fixed issue that prevented seeing certain fields when the layout for Transaction Manager is themed but the layout for the associated configurator is unthemed|
|LGK-19958|Resolved issue with displaying correct picklist values in Transaction Manager|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

