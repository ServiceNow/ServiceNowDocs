---
title: Logik.ai 2026/01/16 release notes
description: Logik.ai 2026/01/16 release notes include new enhancements and bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2026-01-16.html
release: other
topic_type: reference
last_updated: "2026-06-02"
reading_time_minutes: 2
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2026/01/16 release notes

Logik.ai 2026/01/16 release notes include new enhancements and bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, January 15, 2026, 8 pm CT|
|Test|Thursday, February 12, 2026, 8 pm CT|
|Prod|Friday, March 20, 2026, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Friday, March 20, 2026.

## Release notes

This release version includes the following new enhancements and fixes.

## AI capabilities

The following AI features are now available. Contact your Customer Experience Representative to enable AI features.

-   Smart Predict: Get real-time, in-flow recommendations for configuration values based on configuration history.
-   AI Rules Search: Improve rules discovery using semantic search across conditions, actions, and more.

## Transaction Manager: Share Product Favorites

Users can now share their saved favorite products and configurations with other users, improving collaboration and efficiency by enabling easy sharing and reuse of product configurations. Contact Support to enable this feature on your instance.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-19766|Resolved issue with dynamic picklist query when running rules on dynamic picklists|
|LGK-20196|Resolved issue that allowed creation of overlapping variable names on sets and product pickers|
|LGK-20237|Added pagination support for picker rule rows|
|LGK-20270|Improved error handling in Library Function compilation to prevent errors during blueprint deployment|
|LGK-20363|Addressed issue in Transaction Manager with delay in a favorite clearing from the UI after removal|
|LGK-20378|Added support for all product ID types in the Bulk Upload Transaction AI feature|
|LGK-20379|Addressed data type inconsistency issue in Transaction Manager Get Lines API response|
|DEF0785994|Resolved issue where a parent blueprint configures a Solution with mapping on a field within a set and set index updates|
|DEF0788634|Fixed issue where Price Sync fails in Salesforce when the tenant setting namespace is changed in the Config Sync Service|
|DEF0788682|Fixed issue with updating existing lines using the Bulk Update feature in Transaction AI|
|DEF0789455|Fixed issue where context variables in ServiceNow Advanced Product Configurator were not updating during reconfiguration despite correct new values in the sourceInstance payload|
|DEF0789618|Fixed issue where LibraryFunction related objects API ignored page and size URL parameters|
|DEF0790164|Fixed issue where on reconfiguration, new fields added to a set had no corresponding data|
|DEF0790470|Fixed issue in Transaction Manager where rules incorrectly ran on open of transaction|
|DEF0799038|Fixed issue in Shopify app where a quantity greater than one was not added to the cart|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

