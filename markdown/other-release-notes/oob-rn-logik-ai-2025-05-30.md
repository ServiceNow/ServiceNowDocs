---
title: Logik.ai 2025/05/30 release notes
description: Logik.ai 2025/05/30 release notes include new enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-05-30.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/05/30 release notes

Logik.ai 2025/05/30 release notes include new enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, May 29, 2025, 8 pm CT|
|Test|Thursday, Jun 05, 2025, 8 pm CT|
|Prod|Friday, Jun 20, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Jun 20, 2025.

## Release notes

This release version includes the following new enhancements and fixes.

## New Transaction Manager enhancement: layout editor - YAML format

In addition to viewing and editing the TM Layout in JSON, there is a new option to view and edit in YAML. This is a step in our progression towards a visual-based layout editor, as the YAML data format will serve as the underlying data for the visual editor. YAML provides several benefits, including:

-   Better readability: fewer wrappers such as quotes and brackets
-   Schemas ease of use
    -   Enhanced validation
    -   Property help on hover
    -   Autocomplete with acceptable values
-   Support for comments

## New enhancement: Library functions

You can now import and export library functions.

## New enhancement: Use CSV files to add user permissions to tables

Enabled utilization of CSV uploads in adding user permissions to tables. Also fixed various bugs related to access control.

## New enhancement: Last modified time in configurable products table

Added last modified time.

## New enhancement: HTTP methods

The PUT and DELETE HTTP methods are now available in Configuration External Connections and Transaction Manager integrations.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-15428|Fixed bug where product pickers were not displaying properly on Shopify platform|
|LGK-17249|Resolved issue sometimes causing solution configuration ID to be missing from transaction lines|
|LGK-17306, LGK-17312|Resolved issue that caused library functions to depend on Transaction Manager being enabled|
|LGK-17308|Resolved issue where users would see excessive warnings when access control was enabled and the user lacked admin permissions|
|LGK-17344|Resolved issue with delete transaction lines event|
|LGK-17385|Resolved issue in smart predict where users were not given indication of status after starting model training|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

