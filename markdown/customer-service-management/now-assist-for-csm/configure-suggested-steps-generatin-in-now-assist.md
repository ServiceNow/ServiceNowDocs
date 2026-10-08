---
title: Configure Suggested Steps Generation
description: Configure suggested steps generation to analyze clusters of similar cases and suggest next steps for case resolution for accelerated and consistent agent case troubleshooting.Learn how to enable the suggested steps generation in the CRM Workspace after skill activation.Replace the default sn\_customerservice\_agent and sn\_customerservice.consumer\_agent role with a custom role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/now-assist-for-csm/configure-suggested-steps-generatin-in-now-assist.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents, generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Activate ServiceNow Otto Skills, Configure, ServiceNow Otto for CSM, Customer Service Management]
---

# Configure Suggested Steps Generation

Configure suggested steps generation to analyze clusters of similar cases and suggest next steps for case resolution for accelerated and consistent agent case troubleshooting.

## Before you begin

Role required: admin

Suggested steps are generated from the records identified based on the information that you enter in the following fields:

-   Short Description
-   Edited Conditions

Assess your case data before setup:

-   Before activating Suggested Steps Generation, verify that your case data meets quality requirements. Poor data quality is the primary cause of setup failures and inadequate suggestions.
-   Verify the following before beginning configuration:
    -   Percentage of cases with populated Short Description field \(target: 80%+\)
    -   Consistency of Edited Conditions usage across agents
    -   Minimum of 2000 similar cases for effective clustering
    -   Case data currency \(verify historical data is recent enough to be relevant\)
    -   Special characters or formatting issues that could break parsing
-   Don't proceed if:
    -   Less than 2000 cases match your use case
    -   Short descriptions are very generic. For example, "Fixed" or "Case resolved"
    -   Edited Conditions are inconsistently formatted or mostly empty
    -   Cases span many unrelated product lines

## Procedure

1.  Navigate to **AI Admin Hub** &gt; **AI Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate Skill for the **Suggested Steps Generation** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **Choose Inputs** and review the tables and fields to create prompts that determine where data is pulled from.

    **Note:** You can't modify the input data source. However, you can refine which records are used by editing the Edited Conditions filter.

    Understanding Edited Conditions: Edited Conditions are structured troubleshooting steps or resolution details that agents enter when resolving cases. The Suggested Steps system uses these to identify common resolution patterns. You can filter Edited Conditions by:

    -   Date range: "Created in last 6 months" \(avoid stale cases\)
    -   Resolution status: "State = Resolved"
    -   Assignment group: "Assignment group = Platform Support"
    -   Severity: "Priority &gt;= 2"
    Example Filter- "Created in last 6 months AND State = Resolved AND Assignment group = First Level Support AND Short\_description NOT EMPTY"

    |Input|Description|
    |-----|-----------|
    |Input table|Case \[sn\_customerservice\_case\]|
    |Input fields|Short description|
    |Filter conditions|Edited Conditions: Edit the conditions to update the filter and verify that only relevant and up-to-date records are used.|

5.  Select **Record Clustering** to group records by similarity based on the adjusted inputs in the previous step.

    **Note:** Record clustering allows you to add the job in the queue, providing you with the ability to leave the page while the task is running in the background. You will be notified when the task is complete.

    Expected Clustering Performance- Clustering times vary by case volume and instance load:

    -   Minimum 2,000 cases: ~10-20 minutes
    -   5,000+ cases: 30+ minutes \(runs as background job\)
    If Clustering Fails- Common reasons and solutions:

    -   Filter returns zero records → Broaden your Edited Conditions filter
    -   Special characters in descriptions → Clean description data
    -   Other background jobs running → Wait for completion or try again
    -   Check logs: **AI Admin Hub** &gt; **Logs** for detailed error messages
6.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_customerservice\_agent or sn\_customerservice.consumer\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they are updated automatically by a script.
    -   If custom roles are created after the upgrade, you must manually add them in both the **Define Access** and **Select Display**.

        **Note:** A role added in **Define Access** will not automatically appear in **Select Display**. You must manually select it in the next step.

        If agents can't see Suggested Steps after activation, verify:

        -   Role is present in **Define Access** step
        -   Role is toggled on in **Select Display** step
        -   Agent has sn\_gaf.data\_writer role \(required for skill access\)
        -   Recommended Actions widget is enabled in CRM Workspace
        -   Clustering job completed successfully \(check logs\)
        -   Clear browser cache and refresh case form
7.  Toggle **Display** to determine if suggested step recommendations appear in In-product desktop, displaying AI skills on forms and workspaces.

8.  After selecting **Review and Activate** to examine changes, select **Done** to close the Suggested Steps Generation settings.

9.  Select **Activate** to turn on the skill for agents and complete the configuration.


|Error or symptom|Cause|Solution|
|----------------|-----|--------|
|No clusters generated|Edited Conditions filter is too restrictive|Broaden filter to capture at least 2000+ cases|
|Skill appears inactive in AI Admin Hub|Skill configuration not saved after setup|Complete all guided setup steps.|
|Agents see "No suggestions available"|Insufficient similar cases or insufficient data|Re-cluster with broader filter|
|Suggested steps are outdated or irrelevant|Cluster includes very old cases|Add date filter: "Created &gt;= 90 days ago"|
|Role added in Define Access but not visible in Select Display|Select Display must be configured separately|Add role in Select Display and toggle ON|
|Recommended Actions widget not visible|ACL permissions or form configuration issue|Verify sn\_gaf.data\_writer role + check widget enabled|
|Custom table suggestions not appearing|Widget data source not set to custom table|Verify table extends case table; check widget binding|
|GAF access denied error|sn\_gaf.data\_writer role not in role hierarchy|Add sn\_gaf.data\_writer to custom role Contains Roles list|

## Make suggested steps available on CRM Workspace

Learn how to enable the suggested steps generation in the CRM Workspace after skill activation.

### Before you begin

Role required: admin

After activating the Suggested steps generation feature in the AI Admin Hub, follow the steps outlined to make the skill available in CRM Workspace.

### Procedure

1.  Navigate to **All** &gt; **UI Builder**.

2.  Go to **Experiences** &gt; **CSM/FSM Configurable Workspace** &gt; **Record** &gt; **Front-line Case Page**.

3.  In the left content navigation pane, scroll down and select **Recommended Action 1**.

4.  In the right pane, clear the checkbox **Hide recommended actions**.

5.  Select **Save** to apply the changes.


### Result

Recommended Actions will be displayed in the CRM Workspace and you can see the Suggested steps generation skill under it.

## Customize access control for suggested steps

Replace the default sn\_customerservice\_agent and sn\_customerservice.consumer\_agent role with a custom role.

### Before you begin

Role required: admin

### Procedure

1.  Update role permissions

    In the sys\_user\_role table, open your custom role and add sn\_gaf.data\_writer to the Contains Role related list.

2.  Update ACLs

    In the sys\_security\_acl table, filter for ACL names starting with gaf\_suggested\_steps\_csm. Add your custom role to each of the four matching records.

3.  Configure skill access

    In AI Admin Hub, complete the setup for the CSM Suggested Steps Generation skill:

    -   Add your custom role in the **Define Access** step.
    -   Add the same role in the **Select Display** step.
    **Note:** The `sn_gaf.data_writer` role includes `platform_ml_read` by default. Since `sn_gaf.data_writer` is assigned to agent roles like `sn_esm_agent`, those agents inherit `platform_ml_read` as well, which gives them broader access than intended. To avoid unintended access, never assign `platform_ml_read` directly to a user- it should always be inherited through their agent role.


### Result

By default, the sn\_customerservice\_agent and sn\_customerservice.consumer\_agent  role is used. These steps allow you to configure a custom role if needed.

