---
title: Logik.ai 2025/11/21 release notes
description: Logik.ai 2025/11/21 release notes include new enhancements and bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-11-21.html
release: other
topic_type: reference
last_updated: "2026-06-02"
reading_time_minutes: 2
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/11/21 release notes

Logik.ai 2025/11/21 release notes include new enhancements and bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, November 20, 2025, 8 pm CT|
|Test|Thursday, December 04, 2025, 8 pm CT|
|Prod|Friday, January 09, 2026, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Friday, January 09, 2026.

## Release notes

This release version includes the following new enhancements and fixes.

## ServiceNow integration

The current integration with ServiceNow now enables the following capabilities:

-   Automatic field, rule, and layout generation from catalog structures
-   Attribute-based and catalog-based configuration
-   Pricing from the ServiceNow Pricing Engine
-   Configuration launch from Opportunity, Quote, Order, Portal, Sold Product, and more
-   Seamless SSO with ServiceNow Platform

## Tag filtering

Tag filtering has been improved. You can now apply tag filters by searching for a tag in the entity's search bar.

## Transaction Manager: Transaction Access Control

Transaction Access Control enables granular control over who can view and edit each transaction, improving security and compliance. Admins and creators automatically receive full access and can grant access to others. Any user with access can also grant or remove access for others. This feature is enabled via tenant setting.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-19675|Added line counts for success, error, warning, and total when replacing a managed table via API|
|LGK-20037|Addressed issue with values clearing on Line Item Grid after refresh|
|LGK-20044|Fixed issue where saving the layout only worked in certain click paths despite the YAML file validating before saving|
|LGK-20084|Added 1-minute cache of dynamic picklist values|
|LGK-20088|Addressed issue with duplicate item keys during reconfiguration|
|LGK-20105|For Clone Line event, new lines are now considered in rule groupings associated to the event; previously only the original selected lines were considered|
|LGK-20108|Addressed a set of issues related to editing layouts|
|LGK-20136|Fixed issue that allowed the same tag to appear in different conditions when filtering tags in a column|
|LGK-20137|Fixed issue that prevented filtering of tags on subfields in set and product picker|
|LGK-20147|Fixed issue blocking admin from adding fields to columns in a field grid|
|LGK-20150|Fixed issue that removed fields upon save when those fields were included in the layout fields array but not referenced in the layout|
|LGK-20165|Fixed error in product search flow caused by product filter rules|
|LGK-20196|Fixed issue with Delivery Product Picker bulk inclusion action|
|LGK-20203|Fixed error executing rules on reconfigure|
|LGK-20211|Fixed issue with cached callback field with stale session ID|
|LGK-20260|Fixed error executing rules on all blueprints when adjusting set size field|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

