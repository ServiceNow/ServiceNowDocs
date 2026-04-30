---
title: Manage customizations before upgrading to Agile Development 2.0
description: You can take complete advantage of enhanced agile functionality by managing your customizations before upgrading to Agile Development 2.0.
locale: en-US
release: zurich
product: Agile Development
classification: agile-development
topic_type: reference
last_updated: "2025-10-23"
reading_time_minutes: 2
breadcrumb: [Migration from Agile Development 1.0 to Agile Development 2.0, Configure, Agile Development 2.0, Strategic Portfolio Management]
---

# Manage customizations before upgrading to Agile Development 2.0

You can take complete advantage of enhanced agile functionality by managing your customizations before upgrading to Agile Development 2.0.

**Important:** Agile Development 1.0 and its features such as Sprint burndown chart and release burndown chart are deprecated and no longer available. [Agile Development 2.0](agile-landing-page.md) provides the latest experience for supporting your Agile work methodology.

As of any regular upgrade, if core platform artifacts such as form layout, adding of fields, removal of preconfigured fields, list layout, business rules, or client scripts, are customized in your environment, then changes made to any of these artifacts as part of the Agile Development 2.0 enhancements are not applied in your environment. You should delete all your customizations before upgrading to Agile Development 2.0, and selectively reapply customizations as needed after upgrade.

Following are the three possible scenarios:

-   **No customizations**

    You do not have any customizations in your Agile Development implementation and want to use the Agile Development 2.0 functionality. In such a case, install the Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\).

-   **Minor customizations**

    There are few minor customizations, but you want to use the Agile Development 2.0 functionality. In such a case, [delete all customizations](../task/delete-customizations.md).

-   **Customizations require review**

    There are a few customizations in your Agile Development implementation that are mapped to your business process. Though you want to use the Agile Development 2.0 functionality, you may want to review your customizations and decide whether to delete all the customizations or retain a few customizations. For such a case:

    -   A utility is provided which automatically detects the customized platform artifacts, such as list layout, form layout, business rules, that were enhanced as part of the Agile Development 2.0 enhancements. For details of this utility and list of all platform artifacts enhanced in Agile Development 2.0, see [Review a utility customization for Agile Development 2.0](../task/utility-review-customizations.md#).
    -   After analyzing, if you do not want to retain any of the customizations, then [delete the customizations](../task/delete-customizations.md). If you want to retain a few, delete the customizations and reapply them after the upgrade.
    -   If you have created your own artifacts, such as business rules and UI policies, verify whether the artifacts work as intended after the upgrade.

**Parent Topic:**[Migration from Agile Development 1.0 to Agile Development 2.0](../concept/migrate-agile.md)

