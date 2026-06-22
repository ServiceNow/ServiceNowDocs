---
title: Logik.ai 2026/06/19 release notes
description: Logik.ai is a high-performance Commerce Logic Engine that complements Salesforce CPQ and eCommerce applications. This document outlines everything you need to know about new features and fixes made in the upcoming Logik.ai release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2026-06-19-.html
release: other
topic_type: reference
last_updated: "2026-04-10"
reading_time_minutes: 2
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2026/06/19 release notes

Logik.ai is a high-performance Commerce Logic Engine that complements Salesforce CPQ and eCommerce applications. This document outlines everything you need to know about new features and fixes made in the upcoming Logik.ai release.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, 18 Jun 2026 8 p.m. CT|
|Test|Thursday, 18 Jun 2026 8 p.m. CT|
|Prod|Friday, 10 July 2026 8 p.m. CT|

Example: an environment with URL, https://\[YourLogikURL\].prod.logik.io, receives this build July 10, 2026.

## Release notes

This release version includes the following fixes.

|Fix|Short description|
|---|-----------------|
|PRB1975635|Fixed issue where table-based pick list conditions appeared blank after refreshing the UI.|
|PRB2005752|Resolved issue where solution child configurations were missing from or removed from the side pane without showing an error.|
|PRB2009029|Fixed issue that prevented On Configure/Reconfigure scripts from running in certain configurations.|
|PRB2009524|Fixed issue where SVG images rendered at zero size in the Visual Picker.|
|PRB2015322|Fixed issue where the radio display type did not appear when viewing a configuration.|
|PRB2018156|Resolved an issue that occurred when configuring a new product.|
|PRB2018657|Fixed issue where Quote Line info and error icons did not render correctly after a stage transition.|
|PRB2020690|Fixed issue in where a hidden column reappeared when the Show Hidden toggle was unchecked.|
|PRB2021978|Fixed issue where successive Line Item Grid updates could be dropped before they were applied.|
|PRB2022990|Fixed issue where the Line Item Grid detail drawer flickered when a scroll bar appeared and the layout resized.|
|PRB2027111|Fixed issue where the Transaction Line Items Grid became out of order when a layout class was applied to a Transaction Header field.|
|PRB2029816|Fixed issue where the extended list price was not set correctly for new lines added during reconfiguration.|
|PRB2029825|Fixed issue where CBOM feature was enabled automatically without notice, disrupting layouts and Quote Line Item editing.|
|PRB2030494|Improved an error message shown when a Logik blueprint fails to import.|
|PRB2030592|Improved performance of the version event when Dynamic Picklists are enabled.|
|PRB2033279|Fixed issue where Config Sync switched to the Bulk API based on the combined BOM and configuration data count.|
|PRB2034725|Fixed issue where System Events lost their rule groupings and integrations during deploy and export.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

