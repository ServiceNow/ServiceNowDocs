---
title: Explore Upgrade Skipped Record Rules Editor in Upgrade Console
description: Configure skipped record rules with the use of Upgrade Skipped Record Rules Editor to automate or facilitate the resolution of data inconsistencies arising from the upgrade process.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Upgrade Console summary, Exploring Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Explore Upgrade Skipped Record Rules Editor in Upgrade Console

Configure skipped record rules with the use of Upgrade Skipped Record Rules Editor to automate or facilitate the resolution of data inconsistencies arising from the upgrade process.

Formulate automated resolution rules to mitigate potential customization conflicts following an upgrade. These rules can be configured to execute autonomously during the upgrade process or manually initiated post-upgrade.

Starting Xanadu release, new skipped rules have been introduced by default to help you auto-retain certain customizations during the upgrade process. This eliminates the need for manual review of the skipped records generated during the upgrade process.

The following is the list of tables from which if any skipped record is being generated as a metadata file, the customizations are retained by default with the new skipped rules:

-   sys\_ui\_section
-   sys\_ui\_form
-   sys\_ui\_form\_section
-   sysevent\_email\_action
-   sys\_ui\_related\_list
-   sys\_ui\_list
-   sys\_choice
-   sys\_choice\_set
-   sys\_report
-   pa\_dashboards
-   wf\_workflow

**Note:** For wf\_workflow\_version table, the new skipped rules automatically sets the generated skipped records to **Keep My Modifications \(Always Retain\)**. This table is generally used for configuration changes and doesn’t need to be reviewed.

The skipped records that are retained automatically by the default skipped rules are found in the Skipped Changes Reviewed related list.

![Image showing retained skipped rules in the Skipped Changes Reviewed related list](../../upgrade-center/image/uc-default-skipped-rules.png)

**Note:** You can also find a comment for each retained skipped record to show the related table it was generated from during the upgrade process.

See [Upgrade Skipped Record Rules Editor tool in Upgrade Console](um-skipped-rules-tool.md) for more information.

