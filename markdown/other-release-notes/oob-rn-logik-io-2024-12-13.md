---
title: Logik.io 2024/12/13 release notes
description: Logik.io 2024/12/13 release notes include new enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-io-2024-12-13.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.io 2024/12/13 release notes

Logik.io 2024/12/13 release notes include new enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Wednesday, Dec 11, 2024, 8 pm CT|
|Test|Thursday, Dec 19, 2024, 8 pm CT|
|Prod|Friday, Jan 10, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Jan 10, 2025.

## Release notes

This release version includes the following new enhancements and fixes.

## New enhancement: New UI Theme available in Admin

A fresh, modern UI theme is now available in the Admin interface. Users can switch to the new theme by selecting the New Admin Version setting on the Utilities &gt; Settings page. This setting is applied at the user level, so each user can choose their preference. We recommend that customers administrating Transaction Manager use the New Admin Version. Configuration-only customers are encouraged to try it out at leisure.

## New enhancement: New Admin option for exclusion action

An option has been added to exclusion rules. When a field is changed to read-only as a result of a determination action, an additional drop-down menu is displayed in the actions section of the page. An Admin now has the option to select between "leave unchanged" and "override and deselect options" from the menu.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-13341|An error in calculations for child components in a Solution meant that in some scenarios, the individual components were multiplied per solution hierarchy level. This has been corrected.|
|LGK-13526|In scenarios where a parent product in a Solution has a Parent Product ID of a product that does not exist, the orphaned child product is now treated as a root product to complete the Solution.|
|LGK-13758|When Blueprints shared components, in certain scenarios a race condition occurred where deployment for some Blueprints failed on the first attempt. This has been fixed.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

