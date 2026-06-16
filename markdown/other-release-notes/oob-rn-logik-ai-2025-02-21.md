---
title: Logik.ai 2025/02/21 release notes
description: Logik.ai 2025/02/21 release notes include minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-02-21.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/02/21 release notes

Logik.ai 2025/02/21 release notes include minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Feb 20, 2025, 8 pm CT|
|Test|Thursday, Mar 06, 2025, 8 pm CT|
|Prod|Friday, Mar 21, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Mar 21, 2025.

## Release notes

This release version includes the following fixes.

|Fix|Short description|
|---|-----------------|
|LGK-13710|Sometimes customers faced a frozen UI on solution config when trying to add more than the maximum allowed number of children. This has been fixed so that the user is blocked from adding more children Blueprints than allowed, and the user is sent an explanatory error message.|
|LGK-15251|Picklists that included over 20 options were not returning all options. This has been fixed.|
|LGK-15291|Images were not displayed in a product picker when used in the last column. This has been fixed.|
|LGK-15336|When a single user made a large number of changes when using an older computer with a slower CPU, they ran into a "Maximum Call Stack Size Exceeded" error. This has been handled appropriately.|
|LGK-15423|Sometimes the select field of a product picker was not hidden via a hiding rule even when the rule conditions were met. This has been corrected.|
|LGK-15510|New Dynamic Picklists could not be created under some scenarios. This has been fixed.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

