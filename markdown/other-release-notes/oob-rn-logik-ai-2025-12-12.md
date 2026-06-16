---
title: Logik.ai 2025/12/12 release notes
description: Logik.ai 2025/12/12 release notes include new enhancements and bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-12-12.html
release: other
topic_type: reference
last_updated: "2026-06-02"
reading_time_minutes: 3
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/12/12 release notes

Logik.ai 2025/12/12 release notes include new enhancements and bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, December 11, 2025, 8 pm CT|
|Test|Thursday, January 08, 2026, 8 pm CT|
|Prod|Friday, February 13, 2026, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Friday, February 13, 2026.

## Release notes

This release version includes the following new enhancements and fixes.

## Admin UI navigation change

On January 9, Logik introduced updated admin navigation for all users in test and production environments. The legacy UI was discontinued at that time. The new navigation retains all functionality from the legacy UI and includes a hierarchy in the side panel for more context when editing blueprints.

## Transaction Manager: Transaction AI - bulk line update via file upload

A new Transaction AI feature allows users to complete a bulk Transaction Line update via a .csv file upload. Add non-configurable products as new lines and update existing lines via the upload. For more information, see [https://www.servicenow.com/docs/r/order-management/cpq-transaction-converse.html](https://www.servicenow.com/docs/r/order-management/cpq-transaction-converse.html).

## Transaction Manager: Export Lines UI Effect

Export Transaction Lines to a .csv file via a new UI Effect. The exported file includes all lines in the transaction that meet current line sort, filter, and column show/hide settings. For more information, see [https://www.servicenow.com/docs/r/order-management/transaction-manager-layouts-ui-effects.html](https://www.servicenow.com/docs/r/order-management/transaction-manager-layouts-ui-effects.html).

## Transaction Manager: Visual Layout Editor

Layouts can now be designed and maintained in a visual-based editor. Add and organize layout components, configure UI Effect and element properties, manage theming, and more, all in an intuitive visual interface. For more information, see [https://www.servicenow.com/docs/r/order-management/transaction-manager-layouts.html](https://www.servicenow.com/docs/r/order-management/transaction-manager-layouts.html).

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-20087|DB CPU maxed out in test DB during bulk export|
|LGK-20164|Resolved issue with Stage Progress UI Chevron highlighting incorrect state|
|LGK-20188|Resolved issue with tabs not displaying content after hiding action trigger|
|LGK-20220|Added tenant setting to manage whether interactive mode applies|
|LGK-20224|Fixed issue where tabular set rows did not render after 10 on a specific blueprint|
|LGK-20231|Improved UX for line drag-and-drop reorder when an error is present on a line|
|LGK-20232|Addressed minor UI issue with Stage Progress UI Chevron|
|LGK-20234|Fixed solution definition loading to accurately indicate when no solution definition exists|
|LGK-20239|Addressed issue with session management for custom events|
|LGK-20251|Addressed race condition with picklist option updates|
|LGK-20256|Fixed issue where Flightpath on/off state was affecting the configuration|
|LGK-20262|Added support for migration of dynamic picklists in Transaction Manager blueprint|
|LGK-20267|Fixed issue where BOM information was incorrectly saved when reconfiguring|
|LGK-20268|"Show size field" set property overrode the layout|
|LGK-20270|Fixed issue where blueprint failed to deploy when a Library Function is called|
|LGK-20272|Fixed issue where Transaction Header error state icon showed incorrectly when line errors are present|
|LGK-20296|Configuration blueprints seemingly undeployed themselves and configuration didn't load|
|LGK-20315|Fixed issue where Product Picker Bulk Action tab crashed the browser in Demo|
|LGK-20323|Fixed issue where a table was not displaying, allowing edits, or able to be deleted in certain environments|
|LGK-20340|Fixed errors occurring when filtering a table using column filters on text columns with the "=" and "≠" operators|
|LGK-20350|Fixed issue where CSV upload failed to apply changes|
|LGK-20351|Fixed Transaction selected line integration errors|
|LGK-20358|Fixed issue where reconfiguration did not retain set repeater size and product picker field values|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

