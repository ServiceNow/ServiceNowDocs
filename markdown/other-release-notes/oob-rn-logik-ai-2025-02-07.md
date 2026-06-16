---
title: Logik.ai 2025/02/07 release notes
description: Logik.ai 2025/02/07 release notes include new enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-02-07.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/02/07 release notes

Logik.ai 2025/02/07 release notes include new enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Feb 06, 2025, 8 pm CT|
|Test|Thursday, Feb 20, 2025, 8 pm CT|
|Prod|Friday, Mar 07, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Mar 07, 2025.

## Release notes

This release version includes the following new enhancements and fixes.

## New enhancement: Error logging improvements

Several improvements have been made to Admin Error logs as outlined in [Admin Logs](https://www.servicenow.com/docs/bundle/zurich-order-management/page/product/servicenow-cpq/concept/admin-logs.html).

## New enhancement: Hide option for pin icon

Logik layouts now support new variables to control the display and behavior of the sidebar pin.

-   `"pinned": "PINNED"` value hides pin button and renders sidebar as pinned
-   `"pinned": "UNPINNED"` value hides pin button and renders sidebar as unpinned
-   `"pinned": "DEFAULT"` value \(or omitted\) shows pin button and defaults sidebar as pinned

## New enhancement: Width option for sidebar component

The sidebar component width can now be defined in the layout. An admin may now provide a width value in either px or vw.

-   `"width": " px"` sets the default width of the sidebar component
-   `"minWidth": " px"` sets the minimum width of the sidebar component
-   `"maxWidth": " px"` sets the maximum width of the sidebar component

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-13987|Added the ability to define max Height using CSS Classes for a Product Picker Grid Inside a Set Repeater.|
|LGK-15056|Added optimization for Managed Table upload scenarios to account for frequent upload of very large tables.|
|LGK-15202|Calendar object was running into an issue where pagination was not working as expected. This has been fixed.|
|LGK-15225|In some scenarios, Column sets and Set Grids were not hidden when all the fields in the Set were hidden. This has been corrected.|
|LGK-15233|Some Set fields were rendering on the UI in a constant loop, causing repeated API calls. This has been fixed.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

