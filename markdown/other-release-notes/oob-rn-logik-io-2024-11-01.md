---
title: Logik.io 2024/11/01 release notes
description: Logik.io 2024/11/01 release notes include new enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-io-2024-11-01.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 2
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.io 2024/11/01 release notes

Logik.io 2024/11/01 release notes include new enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Oct 31, 2024, 8 pm CT|
|Test|Thursday, Nov 7, 2024, 8 pm CT|
|Prod|Friday, Nov 22, 2024, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Nov 22, 2024.

## Release notes

This release version includes the following new enhancements and fixes.

## New Enhancement: Table-based picklist

When setting up picklist field definitions in a configuration, administrators can now source picklist options from a Managed Table. This simplifies the management of options data and facilitates data re-use.

## New Enhancement: Rule loop detection

This feature helps the administrator proactively identify circular references in the fields and rules of a configuration Blueprint, so that they can be corrected before they result in buyside errors at runtime.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-10047|The Blueprint upload process has been optimized to take significantly less time than it used to. We have made changes in Logik so that parsing, validating, and uploading fields, field options, and rules runs faster. The gains will be more evident with larger blueprints.|
|LGK-10701|The “Select All”/ “Deselect All” buttons in product pickers allowed users to remove options that were set via a rule that also had the "Prevent from further editing" flag set to true. This has been corrected.|
|LGK-12900|External connection endpoints for the On Request/ On Reconfigure enrichment script was being constructed incorrectly in some scenarios. This has been fixed.|
|LGK-12942|A “Method Not Allowed” error was thrown when trying to configure products in Logik.io under certain conditions. This has been corrected.|
|LGK-12958|We have optimized the Delete API `POST /api/admin/v1/bulk/fields/delete` to execute bulk field deletions significantly faster.|
|LGK-12998|When a hiding rule is written to hide all set subfields, the set should be hidden. Instead, an empty table was being shown with only the header values. This been corrected.|
|LGK-13188|When the rule execution limit was reached, in some scenarios Logik did not show the error message in the UI even though the logs reported the correct error. This was an error with how rule executions were being calculated and has been fixed.|
|LGK-13279|When a rule with a Determination action and a Hiding action on a Product Picker is executed, an unhandled system validation error was thrown in some situations. This has been fixed.|
|LGK-13310|In some circumstances, rules were shown as being associated with a Blueprint even though none of the fields referenced in the rule were associated with the blueprint. This caused deployment errors for the Blueprint. This issue has been fixed.|
|LGK-13361|User-editable formatted number type fields were showing dual info messages in some situations. This has been corrected.|
|LGK-13366|Sum aggregate calculations for product pickers were incorrect when going through an Amend flow. This has been fixed.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

