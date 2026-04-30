---
title: Let Now Assist help you to manage duplicate CIs
description: Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.
locale: en-US
release: yokohama
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-02-05"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Let Now Assist help you to manage duplicate CIs

Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.

## Before you begin

Role required: cmdb\_dedup\_admin and now\_assist\_panel\_user

## About this task

When a Now Assist for SGC skill is enabled, the Now Assist icon ![](../image/now-assist-sgc-ai.png) appears in the SGC Central view of the CMDB Workspace. For more information, see [Working in the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  On the CMDB Workspace or in any form or list view, select the Now Assist icon ![](../image/ai-sparkle-cmdb.png) and then select **Manage duplicate CIs** in the Now Assist panel.

2.  Follow the guidance on the Now Assist panel to remediate duplication.

    ![Start the manage duplicate CIs skill.](../../now-assist-cmdb/image/na-cmdb-select-mng-dupe-cis.png)

    -   Select an option in the Now Assist panel or enter text that resembles one of the options. As you select options to remediate duplication, the skill adjusts the options and guides you through the process.
    -   Review root causes for duplication: The analysis surveys IRE identification rules \(including criterion attributes\) and discovery sources and responds by grouping causes to suggest related groups of tasks.

        **Tip:** Use this information to help prevent further creation of duplicate CIs.

    -   Decide which de-duplication template to apply: Select **Review existing templates** and then follow the suggestions to preview the results of applying the template. Now Assist generates a preview of the results of applying a template without actually running the remediation process. You can preview the results for any existing template. When you see the desired result in a preview, you can specify that template and proceed with the de-duplication process.

        ![Start the preview template process.](../../now-assist-cmdb/image/na-cmdb-start-prevw-tmplt-results.png)

        ![Now Assist generates a preview of the results of applying a template.](../../now-assist-cmdb/image/na-cmdb-prevw-tmplt-results.png)


## What to do next

-   To learn more about using the Now Assist panel, see [Working in the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   To start over, select **Reset conversation** in the More menu \(![More menu icon](../../../administer/dynamic-translation/image/Ellipses.png)\).

    **Warning:** If you reset the conversation, all existing messages are deleted and an entirely new conversation starts. To learn more about using the Now Assist panel, see [Working in the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   [See how IRE detects duplicate CIs and generates de-duplication tasks](../concept/id-detect-dup-ci.md).
-   [See how to manage and remediate the de-duplication tasks by using de-duplication templates](../concept/de-duplication-tasks.md).

**Related topics**  


[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

[Duplicate CIs remediation](../concept/de-duplication-tasks.md)

[Detecting duplicate CIs](../concept/id-detect-dup-ci.md)

[View CMDB Health dashboard](../concept/c_MonitorCMDBHealth.md)

