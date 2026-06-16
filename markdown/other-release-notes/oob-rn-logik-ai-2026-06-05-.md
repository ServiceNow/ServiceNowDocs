---
title: Logik.ai 2026/06/05 release notes
description: Logik.ai is a high-performance Commerce Logic Engine that complements Salesforce CPQ and eCommerce applications. This document outlines everything you need to know about new features and fixes made in the upcoming Logik.ai release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2026-06-05-.html
release: other
topic_type: reference
last_updated: "2026-04-10"
reading_time_minutes: 2
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2026/06/05 release notes

Logik.ai is a high-performance Commerce Logic Engine that complements Salesforce CPQ and eCommerce applications. This document outlines everything you need to know about new features and fixes made in the upcoming Logik.ai release.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, 04 Jun 2026 8 p.m. CT|
|Test|Thursday, 04 Jun 2026 8 p.m. CT|
|Prod|Friday, 19 Jun 2026 8 p.m. CT|

Example: an environment with URL, https://\[YourLogikURL\].prod.logik.io, receives this build June 19, 2026.

## Release notes

This release version includes the following new enhancements and fixes.

## Transaction Manager: Blueprint deployment status

View the deployment status of a transaction blueprint in the admin UI.

## Transaction Manager: layout updates

-   Use new layout properties for the transaction header.
-   Add fields to the transaction header.

## Transaction Manager: update transaction

Use the new system event to update transaction header or line data through API calls.

|Fix|Short description|
|---|-----------------|
|PRB1970961|Fixed issue where full blueprint migration did not correctly override enrichments.|
|PRB1974689|Fixed issue in Smart Predict where recommended field values displayed option codes instead of user-facing labels.|
|PRB1975566|Resolved issue where the BOM export functionality was unavailable when Solution Configuration was active.|
|PRB1976709|Removed an erroneous validation warning that appeared for pick list fields configured with a dynamic option source.|
|PRB1979652|Fixed issue in Solution Configuration where the product list layout did not populate until the shopping cart was opened.|
|PRB1984887|Fixed issue in the kBridge integration where rapidly entering input into a field caused an error.|
|PRB1989375|Fixed issue where the ExtendedPicklist display type did not display extended data for table-based pick lists.|
|PRB1993566|Resolved an error that occurred when loading non-editable configurations containing listener fields in the kBridge visualizer.|
|PRB2008282|Fixed issue where searching for users in the Manage Access panel returned no results due to API failures.|
|PRB2010669|Fixed issue where deleting a library function parameter removed the last parameter in the list instead of the selected one.|
|PRB2012259|Resolved issue where stale price book entries in Logik caused incorrect pricing despite valid Salesforce data.|
|PRB2021808|Fixed issue in Transaction Manager where configured rules did not fire until a field was manually interacted with.|
|PRB2029873|Resolved issue where a custom theme turned off functionality for fields using the VerticalCheckbox display type.|
|PRB2030624|Fixed an issue where URL UI Effects could not access line-level fields during string interpolation.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

