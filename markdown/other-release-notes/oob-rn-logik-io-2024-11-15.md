---
title: Logik.io 2024/11/15 release notes
description: Logik.io 2024/11/15 release notes
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-io-2024-11-15.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.io 2024/11/15 release notes

Logik.io 2024/11/15 release notes

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Nov 14, 2024, 8 pm CT|
|Test|Thursday, Nov 21, 2024, 8 pm CT|
|Prod|Friday, Dec 06, 2024, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Dec 06, 2024.

## Release notes

This release version includes the following new enhancements and fixes.

## New enhancement: Enhanced Shopping Cart with CSV export

Logik.io now supports an easy way to export the configuration BOM before quote finalization via the exporting of the BOM to a CSV file. Additionally, the BOM UI has been enhanced to enable on-screen manipulation of fields, such as column re-sizing, pinning of fields, and hiding of fields.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-13499|When working with advanced rules scripts in the debugger, admins were getting "An unexpected error occurred" error message. This has been fixed.|
|LGK-13518|When trying to launch Logik for certain blueprints, users sometimes got an "Error executing rules" error message. This was intermittent and occurred only under certain circumstances. This has been resolved.|
|LGK-13525|Some blueprints could not be exported. The export failed with a generic error message. This has been fixed.|
|LGK-13602|The BOM API structure was inadvertently changed due to an underlying library security upgrade. A pageable section was added to the sort section. This has been corrected to match the API structure before the upgrade.|
|LGK-13611|Error where no content was getting added to manufacturing BOM on the UI has been corrected.|
|LGK-13633|Fixed 'Cannot read properties of undefined' error when launching certain blueprints.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

