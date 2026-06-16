---
title: Logik.ai 2025/06/13 release notes
description: Logik.ai 2025/06/13 release notes include new enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-06-13.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/06/13 release notes

Logik.ai 2025/06/13 release notes include new enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Jun 12, 2025, 8 pm CT|
|Test|Thursday, June 19, 2025, 8 pm CT|
|Prod|Friday, Jul 11, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Jul 11, 2025.

## Release notes

This release version includes the following new enhancements and fixes.

## New Transaction Manager enhancement: aggregate behavior update

Aggregate elements with no children or defaults will now always run, ensuring that rules containing aggregates execute as expected. If no default is defined, aggregates will return null, and lookups will return an empty array. Update your aggregates to include a default or handle the null/empty array to avoid errors.

|Fix|Short description|
|---|-----------------|
|LGK-17687|Fixed issue where set repeater data was not properly loading|
|LGK-17813|Fixed issue where multi-billion dollar orders could cause an exception|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

