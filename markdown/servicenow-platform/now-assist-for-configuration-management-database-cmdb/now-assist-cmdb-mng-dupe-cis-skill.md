---
title: Let Now Assist help you to manage duplicate CIs
description: Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Let Now Assist help you to manage duplicate CIs

Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.

## Before you begin

Role required: cmdb\_dedup\_admin and now\_assist\_panel\_user

## About this task

This procedure describes how you can manually access the skill. In addition, any agentic workflow can use the skill.

When a Now Assist skill is enabled, the Now Assist icon ![](../../../administer/virtual-agent/images/icon-now-assist-sparkle.png) appears in the toolbar of the workspace.

## Procedure

1.  On the Service Graph Workspace orCMDB Workspace or in any form or list view, select the Now Assist icon ![](../../../administer/virtual-agent/images/icon-now-assist-sparkle.png) and then select **Manage duplicate CIs** in the Now Assist panel \(or enter similar text\).

2.  Follow the guidance on the Now Assist panel to remediate duplication.

    As you select options to remediate duplication, the skill adjusts the options and guides you through the process.

<table id="table_kkv_vvm_yhc"><thead><tr><th>

Interactions with the skill

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Start the manage duplicate CIs skill.](../../now-assist-cmdb/image/na-cmdb-select-mng-dupe-cis.png)

</td><td>

Review root causes for duplication: The analysis surveys IRE identification rules \(including criterion attributes\) and discovery sources and responds by grouping causes to suggest related groups of tasks.

 **Tip:** Use this information to help avoid further creation of duplicate CIs.

</td></tr><tr><td>

![Start the preview template process.](../../now-assist-cmdb/image/na-cmdb-start-prevw-tmplt-results.png)

</td><td>

Decide which de-duplication template to apply: Select **Review existing templates** and then follow the suggestions to preview the results of applying the template.

</td></tr><tr><td>

![Now Assist generates a preview of the results of applying a template.](../../now-assist-cmdb/image/na-cmdb-prevw-tmplt-results.png)

</td><td>

Without actually running the remediation process, Now Assist generates a preview of the results of applying a template. You can preview the results for any existing template. When you see the desired result in a preview, you can specify that template and proceed with the de-duplication process.

</td></tr></tbody>
</table>3.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d494892e234">

Option

</th><th align="left" id="d494892e237">

Procedure

</th></tr></thead><tbody><tr><td id="d494892e243">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up ![](../image/icon-thumbs-up.png). If you think that it wasn’t helpful, select thumbs-down ![](../image/icon-thumbs-down.png).This feedback improves the Agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the Agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d494892e258">

**Copy the summary**

</td><td>

Select the copy to clipboard icon ![](../image/icon-clipboard.png) to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d494892e269">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon ![](../image/icon-redo.png) to refresh the response information.

</td></tr></tbody>
</table>
## What to do next

-   For more information, see [Working in the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

-   To start over, select **Reset conversation** in the More menu \(![More menu icon](../../../administer/dynamic-translation/image/Ellipses.png)\).

    **Warning:** If you reset the conversation, all existing messages are deleted and an entirely new conversation starts. To learn more about using the Now Assist panel, see [Working in the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

-   [See how IRE detects duplicate CIs and generates de-duplication tasks](../concept/id-detect-dup-ci.md).
-   [See how to manage and remediate the de-duplication tasks by using de-duplication templates](../concept/de-duplication-tasks.md).

**Related topics**  


[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[Duplicate CIs remediation](../concept/de-duplication-tasks.md)

[Detecting duplicate CIs](../concept/id-detect-dup-ci.md)

[View CMDB Health Dashboard](../concept/c_MonitorCMDBHealth.md)

