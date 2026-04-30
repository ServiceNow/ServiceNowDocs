---
title: Review a utility customization for Agile Development 2.0
description: Use the Agile\_2.0\_Upgrade\_Diagnostics update set to analyze your customizations on the platform artifacts \(such as form layout, list layout, business rules, and client scripts\) that are modified as part of the Agile Development 2.0 enhancements. Delete the customizations prior to upgrade.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 1
breadcrumb: [Agile Development 2.0 enhancements over Agile Development 1.0, Migration from Agile Development 1.0 to Agile Development 2.0, Configure, Agile Development 2.0, Strategic Portfolio Management]
---

# Review a utility customization for Agile Development 2.0

Use the Agile\_2.0\_Upgrade\_Diagnostics update set to analyze your customizations on the platform artifacts \(such as form layout, list layout, business rules, and client scripts\) that are modified as part of the Agile Development 2.0 enhancements. Delete the customizations prior to upgrade.

## Before you begin

-   Role required: admin
-   Download the [Agile\_2.0\_Upgrade\_Diagnostics update set](https://community.servicenow.com/community?id=community_article&sys_id=dc9d24f9dbe1af0011762183ca9619fe).

## About this task

**Important:** Agile Development 1.0 and its features such as Sprint burndown chart and release burndown chart are deprecated and no longer available. [Agile Development 2.0](../reference/agile-landing-page.md) provides the latest experience for supporting your Agile work methodology.

## Procedure

1.  Click the **Retrieved Update Sets** module.

2.  Click **Import Update Set from XML**.

3.  Select and upload the update set.

4.  Preview and commit the update set.

5.  Navigate to **Agile Development 2.0** &gt; **Upgrade Diagnostics** &gt; **View Diagnostics**.

    Displays all the artifacts from Agile Development 1.0 that have been modified on the instance and on Agile Development 2.0.

6.  Click the file name of the artifact, or click the **View Update** link to review the latest update on the file.

    For example, in the following screenshot, a system script has been customized. Hence, further analysis is required to delete the customization, restore, or reapply the customization after an upgrade.

    ![Customized system script](../image/agile2-upgrade-diagnostics.png "Example of a customized system script")


**Parent Topic:**[Agile Development 2.0 enhancements over Agile Development 1.0](../concept/appendix.md)

