---
title: Logik.ai 2025/03/21 release notes
description: Logik.ai 2025/23/21 release notes include new enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-03-21.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/03/21 release notes

Logik.ai 2025/23/21 release notes include new enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Mar 20, 2025, 8 pm CT|
|Test|Thursday, Apr 03, 2025, 8 pm CT|
|Prod|Friday, Apr 18, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Apr 18, 2025.

## Release notes

This release version includes the following new enhancements and fixes.

## New function: Date.toLocaleString

For use in Advanced Functions and Enrichment Scripts, the Date.toLocaleString returns a string with a language and location-specific representation of a Date object.

The function can be found in the Help function library in the Script Editor.

## New Transaction Manager enhancement: isReorderable system line field

New line-level system field that indicates whether a line can be reordered.

## New Transaction Manager enhancement: refreshSession UI effect

New UI effect that checks if the session has been modified, and if so, will refresh the sessionId and merge in changes.

## New Transaction Manager enhancement: stages progress chevron layout component

The stages progress chevron represents a transaction’s stage progression as a horizontal chevron bar. It can be defined statically or dynamically, and is configurable through layout JSON.

## New Transaction Manager enhancement: Admin UI-related entities

The Admin UI now displays information on entities related to the current entity being viewed. For example, for a rule, you can quickly see how many fields and rule grouping are associated with it and click the tiles to see more relationship information.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-15747|Field labels on subfields within set grids and field grids were visible when they shouldn't be in fields with Advanced Rules. This was fixed.|
|LGK-15757|When Table based picklist filters rely on other fields to evaluate their condition, the order in which the field values are set needs to be consistent. Table based picklist are loaded last on reconfiguration to support this scenario.|
|LGK-15786|Data type mismatch occurred for Table Based picklists when using number type picklists. This has been fixed.|
|LGK-15812|Managed Table upload generated errors around index creation/deletion/renaming of natural keys. This has been corrected.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

