---
title: Logik.io 2024/12/27 release notes
description: Logik.io 2024/12/27 release notes include minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-io-2024-12-27.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.io 2024/12/27 release notes

Logik.io 2024/12/27 release notes include minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Dec 26, 2024, 8 pm CT|
|Test|Thursday, Jan 09, 2025, 8 pm CT|
|Prod|Friday, Jan 24, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Jan 24, 2025.

## Release notes

This release version includes the following fixes.

|Fix|Short description|
|---|-----------------|
|LGK-13126|If a user entered non-numerical values in a number field in Logik \(such as % or \*\), the invalid value persisted in the UI in some scenarios and was reset to 0 in other scenarios. \(The invalid value was never saved, but because it sometimes persisted in the UI, it gave the user the impression that it was saved.\) This has been fixed so that in all scenarios, entering non-numerical values in number fields results in the number field being reset to a 0 value as soon as the user clicks out of the field.|
|LGK-13721|BOM API responses were being sent out incorrectly in certain scenarios when multiple BOM items were being enriched simultaneously. This has been fixed.|
|LGK-13819|If Logik is open on multiple tabs \(Admin or user side sessions\) the heartbeat for session timeout was being calculated incorrectly. This has been fixed.|
|LGK-13844|Order fields were not working correctly for table-based picklists. This is fixed.|
|LGK-14169|In solution config, when an item is added to a child blueprint that has a grandchild blueprint, the newly added item was incorrectly assigned to the grandchild blueprint instead of the child blueprint in some scenarios. This has been fixed.|
|LGK-14234|When using contains operator with Table based Picklists, users were getting a generic error. This has been resolved.|
|LGK-14444|Side bar in solution config changed as a result of an enhancement such that the View Quote Details button was misplaced in some scenarios. This has been corrected.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

