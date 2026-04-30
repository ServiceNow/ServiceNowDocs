---
title: Migration to ITSM Mobile Agent 5.0.3
description: Migration to ITSM Mobile Agent 5.0.3 enables the Next Experience theme and accessibility compliance in ITSM Mobile Agent.
locale: en-US
release: xanadu
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure, ITSM Mobile Agent, IT Service Management]
---

# Migration to ITSM Mobile Agent 5.0.3

Migration to ITSM Mobile Agent 5.0.3 enables the Next Experience theme and accessibility compliance in ITSM Mobile Agent.

This migration includes the following component changes:

-   Migration of legacy icon sections to new icon sections. It includes better grouping of icon sections for on-call scheduling and incidents along with color variables for icons.
-   Migration of legacy UI parameters to new input form screens. It simplifies the way parameters are defined, enables theming on the input form screen, and supports accessibility enhancements by Mobile Platform.
-   Migration of legacy card views to mobile views. It allows using color variables as per theme.
-   All styling changes can be done through UI rules instead of UI styles.
-   For buttons that perform a positive action, button emphasis has changed from primary to positive.

When customers migrate from any older version to ITSM Mobile Agent 5.0.3, the following steps are automatically performed:

-   When the **plugin.upgraded** event is triggered for the ITSM Mobile Agent \(sn\_itsm\_mobile\_agt\) application, the **Run clean upgrade for ITSM Mobile Agent** script action is run.
-   This script action invokes the following upgrade APIs:
    -   For legacy icon sections to new navigation sections, the cleanUpgradeIconSections\(\) method from the `sn_itsm_mobile_agt.MobileUtahUpgradeEngine` script include.
    -   For old ui parameters to new input form screen,cleanUpgradeButtonInstance\(\) method from the `sn_itsm_mobile_agt.MobileUtahUpgradeEngine` script include.
    -   For legacy cards to new mobile views, cleanUpgradeLegacyCards\(\) method from the `sn_itsm_mobile_agt.MobileUtahUpgradeEngine` script include.
    -   A map with key value pairs, **sn\_itsm\_mobile\_agt.MobileIconSectionMigrationConstant**, is introduced where the key is the sys\_id of the legacy default configuration and the value is an object with a comma-separated list of metadata for the corresponding new default configuration that is introduced in the upgrade process.
-   After the script action is run and performs all the required actions, it is deactivated so that it isn’t run again on future upgrades.

## Migration of legacy icon sections to navigation sections

In this case, the `sn_itsm_mobile_agt.MobileIconSectionMigrationConstants` script include contains the following key value pairs:

-   Key: sys\_id of the legacy default **sys\_sg\_icon\_section** record.
-   Value: Object with a comma-separated list of sys\_ids of **sys\_sg\_navigation\_section** and **sys\_sg\_applet\_launcher\_m2m\_section** records.

The `Run clean upgrade for ITSM Mobile Agent` script action upgrade script runs to perform the following steps for each key in the map:

1.  Check the following records for customizations.
    -   Legacy default **sys\_sg\_icon\_section** record.
    -   Compare if the legacy default icon section has at least one new or one less **sys\_sg\_applet\_launcher\_m2m\_section** record when compared to the new default icon section.
2.  Based on customizations, one of the following steps is performed.
    -   If any of the above records are customized, the script deactivates the new default **sys\_sg\_navigation\_section** record.
    -   If none of the above records are customized, the script deactivates the legacy default **sys\_sg\_icon\_section** record.

**Note:**

-   Custom icon sections that are not available by default continues to function but may not support Next Experience theme and accessibility compliance. Customers must migrate them to navigation sections for better experience.
-   For customized icon sections that are available by default, customers must manually review the legacy default icon sections that are still active and move their customizations to the new default navigation sections.
-   If customized icon sections are not migrated to the new navigation sections, then users will have a mixed experience that may not be fully compatible with the new Next Experience theme and can lead to accessibility issues.

## Migration of UI parameters to input form screen

In this case, the `sn_itsm_mobile_agt.MobileInputFormScreenMigrationConstants` script include contains the following key value pairs:

-   Key: sys\_id of the legacy default **sys\_sg\_button\_instance** record.
-   Value: Object with comma-separated list of sys\_ids of the new default **sys\_sg\_button\_instance** record and other meta data.

The `Run clean upgrade for ITSM Mobile Agent` script action upgrade script then runs to perform the following steps for each key in the map:

1.  Check the following records for customizations.
    -   Legacy default **sys\_sg\_button\_instance** record.
    -   **sys\_sg\_button** record associated with the **sys\_sg\_button\_instance** record.
    -   **sys\_sg\_ui\_parameter** and **sys\_sg\_action\_param\_map** records associated with the **sys\_sg\_button** record.
    -   **sys\_sg\_write\_back\_action\_item** record associated with the **sys\_sg\_button** record.
2.  Based on customizations, one of the following steps is performed.
    -   If any of the above records are customized, the script deactivates the new default **sys\_sg\_button\_instance** record.
    -   If none of the above records are customized, the script deactivates the legacy default **sys\_sg\_button\_instance** record.

**Note:**

-   Custom button instance flows \(UI Params\) that are not available by default continues to function but may not support Next Experience theme and accessibility compliance. Customers must migrate them to input form screens for better experience.
-   For custom button instance flows \(UI Params\) that are available by default, customers must manually review the legacy default **sys\_sg\_button\_instance** records that are still active and move their customizations to the new **sys\_sg\_button\_instance** flow \(refer to the map sn\_itsm\_mobile\_agt.MobileInputFormScreenMigrationConstants\). For configuring Input form screens on mobile, see [Input form screen](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).
-   If customized UI parameters are not migrated to the new input form screens, then users will have a mixed experience that may not be fully compatible with the new Next Experience theme and can lead to accessibility issues.

## Migration of item views to new mobile cards

In this case, the `sn_itsm_mobile_agt.MobileIconSectionMigrationConstants` script include contains the following key value pairs:

-   Key: sys\_id of the legacy default **sys\_sg\_item\_view** record.
-   Value: Object with a comma-separated list of sys\_ids of **sys\_sg\_form\_screen** and **sys\_sg\_master\_item** records where legacy card \(that is, item view\) is referenced.

The `Run clean upgrade for ITSM Mobile Agent` script action upgrade script then runs to perform the following steps for each key in the map:

1.  Check the following records for customizations.
    -   Legacy default **sys\_sg\_item\_view** record.
    -   All **sys\_sg\_ui\_style** records associated with the **sys\_sg\_item\_view** record.
2.  If any of the mentioned records are customized, the script reverts the **sys\_sg\_form\_screen** and **sys\_sg\_master\_item** records to previous state only if these records are not customized.

**Note:**

-   Custom item views that are not available by default will continue to function but may not support Next Experience theme and accessibility compliance. Customers must migrate them to input form screens for better experience.
-   For custom icon sections that are available by default, customers must manually review the old default flows which are still active and move their customizations to the new flow. For information about configuring cards on mobile, see [Customize a screen using Mobile Card Builder](https://www.servicenow.com/docs/access?context=mcb-customize-item-view&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).
-   If customized item views are not migrated to new mobile cards, then users will have a mixed experience that may not be fully compatible with the new Next Experience theme and can lead to accessibility issues.

