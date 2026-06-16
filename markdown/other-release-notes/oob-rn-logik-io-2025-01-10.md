---
title: Logik.io 2025/01/10 release notes
description: Logik.io 2025/01/10 release notes include minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-io-2025-01-10.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.io 2025/01/10 release notes

Logik.io 2025/01/10 release notes include minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Jan 09, 2025, 8 pm CT|
|Test|Thursday, Jan 23, 2025, 8 pm CT|
|Prod|Friday, Feb 07, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Feb 07, 2025.

## Release notes

This release version includes the following fixes.

|Fix|Short description|
|---|-----------------|
|LGK-13930|In Solution Config when fields being used for Solution Config Mappings were also referenced in enrichment scripts, it caused the BOM to be built incorrectly. This has been fixed.|
|LGK-14587|In some scenarios, products removed from the BOM on reconfiguration do not cause the corresponding Quote Lines to be removed in Salesforce when the reconfiguration is saved. This has been corrected.|
|LGK-14626|Solution Config child blueprints were causing a Minified React Error on runtime in certain scenarios. This has been fixed.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

