---
title: Let Now Assist help you to manage duplicate CIs
description: Resolve deduplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-mng-dupe-cis-skill.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-02-06"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Let Now Assist help you to manage duplicate CIs

Resolve deduplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.

## Before you begin

Role required: cmdb\_dedup\_admin and now\_assist\_panel\_user

## About this task

When a Now Assist for SGC skill is enabled, the Now Assist icon \[Omitted image "now-assist-sgc-ai.png"\] appears in the SGC Central view of the CMDB Workspace. For more information, see [Working in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  On the CMDB Workspace or in any form or list view, select the Now Assist icon \[Omitted image "ai-sparkle-cmdb.png"\] and then select **Manage duplicate CIs** in the Now Assist panel \(or enter similar text\).

2.  Follow the guidance on the Now Assist panel to remediate duplication.

    As you select options to remediate duplication, the skill adjusts the options and guides you through the process.

<table id="table_kkv_vvm_yhc"><thead><tr><th>

Interactions with the skill

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Omitted image "na-cmdb-select-mng-dupe-cis.png"\] Alt text: Start the manage duplicate CIs skill.

</td><td>

Review root causes for duplication: The analysis surveys IRE identification rules \(including criterion attributes\) and discovery sources and responds by grouping causes to suggest related groups of tasks.

 **Tip:** Use this information to help prevent further creation of duplicate CIs.

</td></tr><tr><td>

\[Omitted image "na-cmdb-start-prevw-tmplt-results.png"\] Alt text: Start the preview template process.

</td><td>

Decide which deduplication template to apply: Select **Review existing templates** and then follow the suggestions to preview the results of applying the template.

</td></tr><tr><td>

\[Omitted image "na-cmdb-prevw-tmplt-results.png"\] Alt text: Now Assist generates a preview of the results of applying a template.

</td><td>

Without actually running the remediation process, Now Assist generates a preview of the results of applying a template. You can preview the results for any existing template. When you see the desired result in a preview, you can specify that template and proceed with the deduplication process.

</td></tr></tbody>
</table>
## What to do next

-   To learn more about using the Now Assist panel, see [Working in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).

-   To start over, select **Reset conversation** in the More menu \(\[Omitted image "Ellipses.png"\] Alt text: More menu icon\).

    **Warning:** If you reset the conversation, all existing messages are deleted and an entirely new conversation starts. To learn more about using the Now Assist panel, see [Working in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).

-   [See how IRE detects duplicate CIs and generates deduplication tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/id-detect-dup-ci.md).
-   [See how to manage and remediate the deduplication tasks by using deduplication templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/de-duplication-tasks.md).

**Related topics**  


[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)

[Duplicate CIs remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/de-duplication-tasks.md)

[Detecting duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/id-detect-dup-ci.md)

[View CMDB Health Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_MonitorCMDBHealth.md)

