---
title: Create a CI using Now Assist
description: The Create configuration item agentic workflow accepts your natural language request to manually generate a valid CI in the class that you specify.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use agentic workflows, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CI using Now Assist

The Create configuration item agentic workflow accepts your natural language request to manually generate a valid CI in the class that you specify.

## Before you begin

Role required:

-   Now Assist for CMDB v2.4 and earlier: sn\_cmdb\_editor and now\_assist\_panel\_user
-   Starting with Now Assist for CMDB v2.5: sn\_cmdb\_admin and now\_assist\_panel\_user
-   Starting with Now Assist for CMDB v3.0: sn\_cmdb\_editor and now\_assist\_panel\_user

## About this task

Occasionally, you might create a CI manually. To help you, the Create configuration item agentic workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks Identification and Reconciliation engine \(IRE\) rules to determine the required attributes for the CI and requests that information. After you provide sufficient data, the workflow ensures that the proposed CI includes the attributes that you requested, complies with IRE rules, and is not a duplicate. The workflow then creates the CI.

The Create configuration item agentic workflow is particularly useful for adding CIs to tables accessed by Operational Technology because users might add physical CIs while unaware of the importance of managing CI data in the CMDB.

**Note:** The workflow helps avoid creation of a CI whose class does not have an identification rule. For more information, see [Identification rules](../../configuration-management/concept/c_IdentificationRules.md).

To learn more about using the Now Assist panel, see Working in the Now Assist panel.

## Procedure

1.  Use either of the following methods to start the process.

    -   While working in the Service Graph Workspace orCMDB Workspace, select **Create CI** in the Quick Links section.
    -   While working in the Service Graph Workspace orCMDB Workspace, select the Now Assist icon ![](../../../administer/virtual-agent/images/icon-now-assist-sparkle.png) and then enter `create a ci`.
2.  Enter the class of CI to create and then continue by answering the Now Assist questions.

3.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d511938e202">

Option

</th><th align="left" id="d511938e205">

Procedure

</th></tr></thead><tbody><tr><td id="d511938e211">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up ![](../../configuration-management/image/icon-thumbs-up.png). If you think that it wasn’t helpful, select thumbs-down ![](../../configuration-management/image/icon-thumbs-down.png).This feedback improves the Agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the Agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d511938e226">

**Copy the summary**

</td><td>

Select the copy to clipboard icon ![](../../configuration-management/image/icon-clipboard.png) to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d511938e237">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon ![](../../configuration-management/image/icon-redo.png) to refresh the response information.

</td></tr></tbody>
</table>
**Parent Topic:**[Using agentic workflows in Now Assist for CMDB](../../configuration-management/concept/now-assist-cmdb-using.md)

