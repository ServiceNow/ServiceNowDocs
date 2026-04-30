---
title: Default skipped rules
description: Reduce considerable processing time with the default skipped rules to auto-retain high friction causing configuration metadata types.
locale: en-US
release: xanadu
product: Upgrade Center
classification: upgrade-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administration, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Default skipped rules

Reduce considerable processing time with the default skipped rules to auto-retain high friction causing configuration metadata types.

Starting with Xanadu, new skipped rules have been introduced by default to help you auto-retain certain customizations during the upgrade process. This eliminates the need for manual review of the skipped records generated during the upgrade process.

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

![Image showing retained skipped rules in the Skipped Changes Reviewed related list](../image/uc-default-skipped-rules.png)

**Note:** You can also find a comment for each retained skipped records to show the related table it was generated from during the upgrade process.

