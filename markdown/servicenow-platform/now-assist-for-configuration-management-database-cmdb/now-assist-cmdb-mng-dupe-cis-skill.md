---
title: Let Now Assist help you to manage duplicate CIs
description: Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-mng-dupe-cis-skill.html
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

When a Now Assist for SGC skill is enabled, the Now Assist icon \[Omitted image "now-assist-sgc-ai.png"\] appears in the SGC Central view of the CMDB Workspace. For more information, see [Working in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-panel-overview.md).

## Procedure

1.  On the CMDB Workspace or in any form or list view, select the Now Assist icon \[Omitted image "ai-sparkle-cmdb.png"\] and then select **Manage duplicate CIs** in the Now Assist panel.

2.  Follow the guidance on the Now Assist panel to remediate duplication.

    \[Omitted image "na-cmdb-select-mng-dupe-cis.png"\] Alt text: Start the manage duplicate CIs skill.

    -   Select an option in the Now Assist panel or enter text that resembles one of the options. As you select options to remediate duplication, the skill adjusts the options and guides you through the process.
    -   Review root causes for duplication: The analysis surveys IRE identification rules \(including criterion attributes\) and discovery sources and responds by grouping causes to suggest related groups of tasks.

        **Tip:** Use this information to help prevent further creation of duplicate CIs.

    -   Decide which de-duplication template to apply: Select **Review existing templates** and then follow the suggestions to preview the results of applying the template. Now Assist generates a preview of the results of applying a template without actually running the remediation process. You can preview the results for any existing template. When you see the desired result in a preview, you can specify that template and proceed with the de-duplication process.

        \[Omitted image "na-cmdb-start-prevw-tmplt-results.png"\] Alt text: Start the preview template process.

        \[Omitted image "na-cmdb-prevw-tmplt-results.png"\] Alt text: Now Assist generates a preview of the results of applying a template.


## What to do next

-   To learn more about using the Now Assist panel, see [Working in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-panel-overview.md).

-   To start over, select **Reset conversation** in the More menu \(\[Omitted image "Ellipses.png"\] Alt text: More menu icon\).

    **Warning:** If you reset the conversation, all existing messages are deleted and an entirely new conversation starts. To learn more about using the Now Assist panel, see [Working in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-panel-overview.md).

-   [See how IRE detects duplicate CIs and generates de-duplication tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/id-detect-dup-ci.md).
-   [See how to manage and remediate the de-duplication tasks by using de-duplication templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/de-duplication-tasks.md).

**Related topics**  


[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-panel-overview.md)

[Duplicate CIs remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/de-duplication-tasks.md)

[Detecting duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/id-detect-dup-ci.md)

[View CMDB Health dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/c_MonitorCMDBHealth.md)

