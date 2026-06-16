---
title: Logik.ai 2026/02/13 release notes
description: Logik.ai 2026/02/13 release notes include new enhancements and bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2026-02-13.html
release: other
topic_type: reference
last_updated: "2026-06-02"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2026/02/13 release notes

Logik.ai 2026/02/13 release notes include new enhancements and bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Feb 12, 2026, 8 pm CT|
|Test|Thursday, Mar 12, 2026, 8 pm CT|
|Prod|Friday, Apr 10, 2026, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Friday, Apr 10, 2026.

## Release notes

This release version includes the following new enhancements and fixes.

## Transaction Manager: Hierarchical line numbering

This release includes a new option for line numbering: hierarchical numbers \(1, 1.1, 2, 2.1, 2.1.1, etc\). For more information, see [https://www.servicenow.com/docs/r/order-management/transaction-manager-layouts.html](https://www.servicenow.com/docs/r/order-management/transaction-manager-layouts.html).

## Bug fixes

|Fix|Short description|
|---|-----------------|
|DEF0779414|Addressed UI refresh issue after adding lines via Transaction AI Bulk Upload function|
|DEF0781917|Improved field name recognition in prompts for Transaction AI|
|DEF0786613|Prevented stale UUID from being used in BOM calls|
|DEF0786681|Fixed null pointer exception when navigating condition hierarchy|
|DEF0787090|Updated scripting library version for query-level session tracking|
|DEF0790304|Fixed styling issues with shared library|
|DEF0791431|Added case insensitivity for ServiceNow BomType usage|
|DEF0792923|Display option labels instead of values in Smart Predict|
|DEF0797501|Fixed null error when number type dynamic picklists are cleared|
|DEF0801296|Added initialization cache for dynamic option set table definition; blocked warmer threads from growing without bounds; reduced memory utilization for sessions that start with many field options; improved scalability of dynamic option sets|
|DEF0802441|Fixed issue with number data type in Transaction Manager Dynamic Picklists|
|DEF0802786|Fixed invalid error with YAML columnset schema validation|
|DEF0805048|Fixed issue where translated strings were used to compare enums|
|DEF0805084|Fixed loading of duplicate fields in FunctionDefinition|
|DEF0806376|Enabled using the same Transaction Manager field in a Config blueprint script and rule|
|DEF0807004|Improved max height determination of Transaction AI UI|
|DEF0808320|Fixed web socket connection in web components|
|DEF0808435|Updated Shopify commit logic to ensure submitted quantities are integers|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

