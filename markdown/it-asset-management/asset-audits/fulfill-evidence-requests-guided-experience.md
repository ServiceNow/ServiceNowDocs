---
title: Fulfill evidence requests through the Asset Response Guided Experience
description: Use the Asset Response Guided Experience to fulfill and respond to evidence requests for financial regulatory audit engagements.
locale: en-US
release: australia
product: Asset Audits
classification: asset-audits
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Fulfilling evidence requests, Asset Audit Response, IT Asset Management]
---

# Fulfill evidence requests through the Asset Response Guided Experience

Use the Asset Response Guided Experience to fulfill and respond to evidence requests for financial regulatory audit engagements.

## Before you begin

Role required: sn\_audit\_response.asset\_governance

## About this task

The Asset Response Guided Experience takes you through the entire process of fulfilling an evidence request, from accepting the request to submitting a final response to the request. Each set of tasks in this process is represented by a step in the guided experience. You must complete all tasks within a step before you can move on to the next step. You can also save your progress at any point in the process and return to the guided experience at a later time.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **Asset Governance Workspace**.

2.  From the Asset evidence tasks related list in the Asset governance overview, select the task that is associated with the evidence request that you want to fulfill.

    The Asset Response Guided Experience opens.

3.  In the Audit scope step of the guided experience, verify the details of the evidence request and then select **Accept**.

    **Note:** At any point in the Audit scope step, you can post comments and view your activity stream in the contextual side panel.

    **Note:**

    At any point after you select **Accept**, you can automatically generate a comprehensive summary of the evidence request by selecting **Summarize evidence**. This summarization skill uses generative AI to provide the following information about the request:

    -   Evidence Request Overview: General information about the request, including the purpose of the request, the date and time at which the request was created, the user who the request is assigned to, and details about the corresponding audit engagement.
    -   Evidence Records: Information about the evidence records that were created for the request, including the total number of records, the type of supporting information that is included in each record, and the state of each record.
    -   Remediation Rules: Information about the remediation rules that were created for the request, including the total number of rules and the focus of each rule.
    -   Remediation Tasks: Information about the remediation tasks that were automatically generated based on the remediation rules, including the total number of tasks and the status of each task.
    -   Activity &amp; Audit Notes: Additional notes and activity logs for the request.
    This skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). If you choose to deactivate the skill, you must reactivate it manually. For detailed instructions, see [Activate a Now Assist skill](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

4.  Create evidence records for the supporting information or data that you want to collect and submit for the evidence request.

    1.  In the side panel of the guided experience, select **Asset Evidence**.

    2.  From the Asset Evidence related list, select **New**.

    3.  On the form, fill in the fields.

<table id="table_p54_hfj_qfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

Status of the evidence collection.

</td></tr><tr><td>

Evidence type

</td><td>

Type of evidence that you want to collect and submit. Select one of the following options:-   **Attachment**: Document that contains supporting information or data.

**Important:** If you select this option, you must use the **Attachment** option in the contextual side panel of the Create New Asset Evidence form to attach the document.

-   **Data Visualization**: Internal report that contains supporting information or data.
-   **Report**: Internal report that contains supporting information or data.
-   **URL**: URL for the website or shared online folder that contains supporting information or data.


</td></tr><tr><td>

Assignment group

</td><td>

User group that is assigned to collect the evidence.

</td></tr><tr><td>

Assigned to

</td><td>

User who is assigned to collect the evidence.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the evidence that you want to collect and submit.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the evidence that you want to collect and submit.

</td></tr><tr><td>

Report

</td><td>

Report that contains the supporting information or data that you want to collect and submit. If you use this option, the user who is assigned to this evidence record must run the selected report to collect this information or data.**Note:** This field appears only if you set the **Evidence type** field to **Report**.

</td></tr><tr><td>

Data Visualization

</td><td>

Report that contains the supporting information or data that you want to collect and submit. If you use this option, the user who is assigned to this evidence record must run the selected report to collect this information or data.**Note:** This field appears only if you set the **Evidence type** field to **Data Visualization**.

</td></tr><tr><td>

URL

</td><td>

URL of the website or shared online folder that contains the supporting information or data that you want to collect and submit. The assigned user must collect this information or data from the website or shared online folder that you specify.**Note:** This field appears only if you set the **Evidence type** field to **URL**.

</td></tr></tbody>
</table>    4.  Select **Save**.

        The evidence record is added to the Asset Evidence related list.

    5.  Repeat steps b to d for each evidence record that you want to create.

    The assigned user can begin collecting the required evidence. After the evidence is collected, the user can upload it by using the **Attachment** option in the contextual side panel of the evidence record. After the evidence is successfully uploaded, the user can update the **Status** field to **Complete**.

5.  Create remediation rules to identify any data gaps that are discovered during the evidence collection process.

    1.  In the side panel of the guided experience, select **Evidence Remediation Rules**.

    2.  From the Evidence Remediation Rules related list, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Asset evidence|Evidence record that the remediation rule applies to.|
        |Resolution|Action that must be taken to resolve and close any remediation tasks that are automatically generated from the remediation rule.|
        |Assignment group|User group that is assigned to manage the remediation tasks that are automatically generated from the remediation rule.|
        |Assigned to|User who is assigned to manage the remediation tasks that are automatically generated from the remediation rule.|
        |Short description|Brief description of the remediation rule.|
        |Description|Detailed description of the remediation rule.|
        |Evidence scope|Table that the remediation rule applies to. For example, if you set this field to **Computer**, the remediation rule applies only to the computer records that are defined in the **Scope filter** field.|
        |Scope filter|Conditions that enable you to filter the evidence scope that the remediation rule applies to. Select **Set conditions** to specify the field, operator, and value of each condition that you want to set.|
        |Scope condition|Conditions for creating remediation tasks based on the evidence scope and scope filter of the remediation rule. Select **Set conditions** to specify the field, operator, and value of each condition that you want to set.|

6.  On the header of the Asset Response Guided Experience, select **Next**.

7.  In the Readiness step of the guided experience, monitor the status of your evidence collection by using the following widgets and related lists:

    |Widget or related list|Description|
    |----------------------|-----------|
    |Task analytics by priority|Total number of remediation tasks that were automatically generated from your remediation rules, grouped by the task priority.|
    |Total assets evaluated|Total amount of evidence that has been evaluated through your remediation rules, grouped by the compliance status.|
    |Evidences|List of evidence records that you have created for the evidence request. Select a record to view additional details.|
    |Remediation tasks|List of remediation tasks that were automatically generated from your remediation rules. Select a task to view additional details, including the list of impacted records that are associated with that task. Use this information to determine if you want to defer or take action on that task.|

8.  On the header of the Asset Response Guided Experience, select **Next**.

9.  In the Remediation step of the guided experience, review your remediation tasks by using the following widgets and related lists:

    |Widget or related list|Description|
    |----------------------|-----------|
    |Task analytics by priority|Total number of remediation tasks that were automatically generated from your remediation rules, grouped by the task priority.|
    |Task burndown|Burndown chart that enables you track the progress of your outstanding remediation tasks against the estimated timeline of completion.|
    |Remediation tasks|List of remediation tasks that were automatically generated from your remediation rules. Select a task to view additional details, including the list of impacted records that are associated with that task. Use this information to determine if you want to defer or take action on that task.|

10. On the header of the Asset Response Guided Experience, select **Next**.

11. In the Review step of the guided experience, review and approve all evidence that has been collected for the evidence request.

    Select each record in the Evidence related list to review the evidence that has been collected and uploaded by the assigned user. You can also verify other important details, such as the status of the evidence collection.

    **Important:** All evidence collection must be completed before you approve the evidence.

    You can also review your remediation tasks by using the Task analytics by priority and Remediation task by status widgets.

12. After all evidence is successfully collected and approved, select **Submit for review**.

    The collected evidence is submitted to the audit manager for final review. Based on the results of the review, the audit manager can choose to accept, cancel, request a revision, or request additional information for the associated evidence request.


