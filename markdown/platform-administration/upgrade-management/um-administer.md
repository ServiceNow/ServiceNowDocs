---
title: Administering Upgrade Console
description: The Administration module contains information about managing upgrade risks.You will be notified of the possible conflicts that might result due to several customizations in a skipped metadata file, with a new UI message on the form pages of the metadata files.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Administering Upgrade Console

The Administration module contains information about managing upgrade risks.

## Managing upgrade risk

You will be notified of the possible conflicts that might result due to several customizations in a skipped metadata file, with a new UI message on the form pages of the metadata files.

One of the major conflict areas during an upgrade is resolving conflicts for skipped metadata files that are released by ServiceNow® but have been customized. These conflicts result from multiple users updating the same files. ServiceNow might update the code in the files which you have customized over time. Whenever you install an application or a plugin, you often customize them as per your requirements. During the next upgrade, you might have several skipped records depending on the previous customizations.

**Important:** Avoid modifying the high risk and medium risk \(if possible\) skipped metadata files that can potentially cause conflicted skipped metadata files in your next upgrade. You can edit the files if the modifications are absolutely required.

The purpose of the UI message is to inform you about potential complications that might arise during the upgrade process, especially if any high-priority files have been modified. The notification is of the form of UI messages on the form pages of the metadata files.

The UI message varies based on the severity of the files.

-   Medium risk and non-customized: The medium risk files that are not customized might be updated in future releases. It is recommended not to modify these files unless necessary.

    ![Image showing medium risk warning](../../upgrade-center/image/uc-risky-non-customized-medium.png)

-   High risk and non-customized: The high risk files that are non-customized might be updated in future releases. It is recommended not to modify these files unless necessary.

    ![Image showing high risk warning](../../upgrade-center/image/uc-risky-non-customized-high.png)

    **Note:** You can proceed to modify these files if the changes are absolutely required. The following modal shows up.

    ![Image showing File Customizations modal](../../upgrade-center/image/uc-risk-modal.png)

-   High risk and customized: The high risk files that are customized might be updated in future releases. It is recommended to revert them to the Base System to avoid conflicts.

    ![Image showing high risk warning](../../upgrade-center/image/uc-risky-customized-high.png)

-   Medium risk and customized: The medium risk files that are customized might be updated in future releases. It is recommended to revert it to the Base System to avoid conflicts.

    ![Image showing medium risk warning](../../upgrade-center/image/uc-risky-customized-medium.png)

-   Non-risky and non-customized: You don’t see any warning for this condition.
-   Non-risky and customized: You don’t see any warning for this condition.

### High Risk Customizations menu

The **High Risk Customizations** menu item presents the overlap between ServiceNow's high and medium risk files and your customizations.

![Image showing High Risk Customizations menu item](../../upgrade-center/image/uc-menu-item.png)

They are stored in a virtual table called v\_metadata\_customization\_risk, and is refreshed after a set period of time or when you select the **Refresh** on the list view.

![Image showing the list of risk files](../../upgrade-center/image/uc-metadata-risk.png)

### Risk files storage

The high risk and medium risk files are stored in the new sys\_metadata\_volatility table.

**Note:** It is recommended not to modify the sys\_metadata\_volatility table and is automatically updated for every family upgrade. The sys\_metadata\_volatility table is not a part of the menu item in the navbar.

![Image showing the volatility level](../../upgrade-center/image/uc-metadata-volatility.png)

**Note:** Risk is determined by the likelihood of a given metadata file being modified, which is predicted based on trends in updates from recent releases. Some files that may not currently exist in the system will be present in the table to account for future installation of apps/plugins.

