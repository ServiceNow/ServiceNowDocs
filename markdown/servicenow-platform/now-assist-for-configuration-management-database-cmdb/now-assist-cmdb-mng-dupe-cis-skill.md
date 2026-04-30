---
title: Use the Now Assist manage duplicate CIs skill
description: Resolve deduplication tasks with support from Now Assist. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.
locale: en-US
release: xanadu
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2025-02-01"
reading_time_minutes: 3
breadcrumb: [Using Now Assist for CMDB, Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Use the Now Assist manage duplicate CIs skill

Resolve deduplication tasks with support from Now Assist. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.

## Before you begin

Role required: cmdb\_dedup\_admin

## About this task

The following scheduled jobs support the manage duplicate CIs skill:

-   The Populate Duplicate Task Data scheduled job must be enabled. For more information, see [Components installed for duplicate CI remediation](../reference/components-installed-with-dup-ci.md).
-   The Populate Duplicate Task Group Daily scheduled job must be enabled to provide analysis of the root cause of remediation tasks. For more information, see [Components installed with CMDB Workspace](../reference/installed-with-cmdb-workspace.md).
-   The Correctness Score Calculation scheduled job improves the accuracy of summary details on the CMDB Health Dashboard. For more information, see [Enable and configure a CMDB Health Dashboard job](t_EnableCMDBHealthDashboardJob.md).

When a Now Assist for SGC skill is enabled on an instance, the Now Assist icon ![](../image/now-assist-sgc-ai.png) appears in the CMDB Workspace. For more information, see [Working in the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  On the CMDB workspace or in any form or list view, select the Now Assist icon \(![Now Assist icon.](../image/ai-sparkle-cmdb.png)\) and then select **Manage duplicate CIs** in the Now Assist panel.

    ![Start the manage duplicate CIs skill.](../image/na-cmdb-select-mng-dupe-cis.png)

2.  Follow the guidance on the Now Assist panel to remediate duplication.

    -   Select an option in the Now Assist panel or enter text that resembles one of the options. As you select options to remediate duplication, the skill adjusts the options and guides you through the process.
    -   Review root causes for duplication: The analysis surveys IRE identification rules \(including criterion attributes\) and discovery sources and responds by grouping causes to suggest related groups of tasks.

        **Tip:** Use this information to help prevent further creation of duplicate CIs.

    -   Decide which deduplication template to apply: Select **Review existing templates** and then follow the suggestions to preview the results of applying the template. Now Assist generates a preview of the results of applying a template without actually running the remediation process. You can preview the results for any existing template. When you see the desired result in a preview, you can specify that template and proceed with the deduplication process.

        ![Start the preview template process.](../image/na-cmdb-start-prevw-tmplt-results.png)

        ![Now Assist generates a preview of the results of applying a template.](../image/na-cmdb-prevw-tmplt-results.png)


## What to do next

-   In the More menu \(![More menu icon](../../../administer/dynamic-translation/image/Ellipses.png)\), select **Reset conversation** to start over.

    **Warning:** If you reset the conversation, all existing messages are deleted and an entirely new conversation starts. To learn more about using the Now Assist panel, see [Working in the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

-   See how IRE detects duplicate CIs and generates deduplication tasks. For more information, see [See how IRE detects duplicate CIs and generates deduplication tasks](../concept/id-detect-dup-ci.md).
-   See how to manage and remediate the deduplication tasks by using the deduplication templates. For more information, see [See how to manage and remediate the deduplication tasks by using deduplication templates](../concept/de-duplication-tasks.md).

**Related topics**  


[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Duplicate CIs remediation](../concept/de-duplication-tasks.md)

[Detecting duplicate CIs](../concept/id-detect-dup-ci.md)

[View CMDB Health Dashboard](../concept/c_MonitorCMDBHealth.md)

