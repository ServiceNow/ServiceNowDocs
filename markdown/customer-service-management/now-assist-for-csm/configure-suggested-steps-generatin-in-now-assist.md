---
title: Configure Suggested Steps Generation
description: Configure suggested steps generation to analyze clusters of similar cases and suggest next steps for case resolution for accelerated and consistent agent case troubleshooting.Learn how to enable the suggested steps generation in the CRM Workspace after skill activation.Replace the default sn\_customerservice\_agent and sn\_customerservice.consumer\_agent role with a custom role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/configure-suggested-steps-generatin-in-now-assist.html
release: brazil
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 10
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
    -   Less than 50 cases match your use case
    -   Short descriptions are very generic. For example, "Fixed" or "Case resolved"
    -   Edited Conditions are inconsistently formatted or mostly empty
    -   Cases span many unrelated product lines

## Procedure

1.  Navigate to **AI Admin Center** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate Skill for the **Suggested Steps Generation** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **Choose Inputs** and review the tables and fields to create prompts that determines where data is pulled from.

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
    -   Special characters in descriptions → Clean data or adjust NLP settings
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
    -   For customizing access control, see [Customize access control for suggested steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/now-assist-for-csm/configure-suggested-steps-generatin-in-now-assist.md)
7.  Toggle **Display** to determine if suggested step recommendations appear in In-product desktop, displaying AI skills on forms and workspaces.

8.  After selecting **Review and Activate** to examine changes, select **Done** to close the Suggested Steps Generation settings.

9.  Select **Activate** to turn on the skill for agents and complete the configuration.


|Error or symptom|Cause|Solution|
|----------------|-----|--------|
|No clusters generated|Edited Conditions filter is too restrictive|Broaden filter to capture at least 200+ cases|
|Skill appears inactive in AI Admin Hub|Skill configuration not saved after setup|Complete all 9 steps and select **Done**|
|Agents see "No suggestions available"|Insufficient similar cases or insufficient data|Re-cluster with broader filter|
|Suggested steps are outdated or irrelevant|Cluster includes very old cases|Add date filter: "Created &gt;= 90 days ago"|
|Role added in Define Access but not visible in Select Display|Select Display must be configured separately|Add role in Select Display and toggle ON|
|Recommended Actions widget not visible|ACL permissions or form configuration issue|Verify sn\_gaf.data\_writer role + check widget enabled|
|Custom table suggestions not appearing|Widget data source not set to custom table|Verify table extends case table; check widget binding|
|GAF access denied error|sn\_gaf.data\_writer role not in role hierarchy|Add sn\_gaf.data\_writer to custom role Contains Roles list|

## Make suggested steps available on CRM Workspace

Learn how to enable the suggested steps generation in the CRM Workspace after skill activation.

### Before you begin

After activating the Suggested steps generation feature in the AI Admin Hub, follow these steps to make the skill visible in CRM Workspace.

Verify these before proceeding:

-   Recommended Action 1 widget exists on your instance
-   UI Builder is accessible to administrators
-   CRM Workspace has been provisioned

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **UI Builder**.

2.  Go to **Experiences** &gt; **CRM Workspace** &gt; **Record** &gt; **Front-line Case Page**.

3.  In the left content navigation pane, scroll down and select **Recommended Action 1**.

4.  In the right pane, clear the **Hide recommended actions** check box.

5.  Select **Save** to apply the changes.


### Result

After saving configuration, open a case record in CRM Workspace. Suggested Steps generation skill appears below the case form in the Recommended Actions section.

**Configure Recommended Actions for custom tables**

To enable Suggested Steps on custom case tables or extensions, configure the Recommended Actions widget in UI Builder.

Prerequisites for custom tables:

-   Custom table must extend sn\_customerservice\_case
-   Table must have Short Description and Edited Conditions fields or custom equivalents
-   UI Builder experience must exist for the custom form

Configuration steps:

1.  Navigate to **All** &gt; **UI Builder**.
2.  Go to **Experiences** &gt; **\[Your Custom Workspace\]** &gt; **Record** &gt; **\[Your Custom Form Page\]**.
3.  In the left pane, scroll to find Recommended Action widgets or add if missing.
4.  In the right pane, clear the **Hide recommended actions** check box.
5.  Under Widget Settings, verify:
    -   Recommended Actions data source points to your custom table
    -   Binding context includes Short Description field
6.  Select **Save**.

If Recommended Actions Widget is missing:

1.  Navigate to **All** &gt; **UI Builder** &gt; **Experiences** &gt; **\[Your Workspace\]** &gt; **Record** &gt; **\[Your Form\]**.
2.  In the left pane, select **Add** &gt; **Widgets** &gt; **Recommended Actions** or **Recommended Action 1**.
3.  Configure the widget data source to point to your custom table.
4.  Test on the custom form to verify suggestions appear.

**Troubleshooting**

If suggestions aren't visible:

-   Clear browser cache \(Ctrl+Shift+Delete\)
-   Hard refresh the case page \(Ctrl+F5\)
-   Verify your role is in the **Select Display** step
-   Confirm the case is not excluded by Edited Conditions filter
-   Check that Suggested Steps skill clustering completed under **AI Admin Hub** &gt; **Logs**
-   For custom tables: Verify table extends sn\_customerservice\_case
-   For custom tables: Confirm widget data source is set to correct table

## Customize access control for suggested steps

Replace the default sn\_customerservice\_agent and sn\_customerservice.consumer\_agent role with a custom role.

### Before you begin

Role required: admin

### About this task

For custom roles to access Suggested Steps and other AI-powered skills, proper Generative AI Framework \(GAF\) configuration is required. The `sn_gaf.data_writer` role is the base permission for all AI skill access and should be added to the Contains Role list for custom agent roles. don't assign this role directly to users.

### Procedure

1.  Add the GAF data writer role to your custom role

    In the sys\_user\_role table, open your custom role and add `sn_gaf.data_writer` to the Contains Role related list.

    **Tip:** The `sn_gaf.data_writer` role should always be inherited through an agent role such as `sn_customerservice_agent`, never assigned directly to users.

2.  Identify GAF-related ACLs

    Navigate to the sys\_security\_acl table and filter where Name starts with `gaf_suggested_steps_csm`.

    Four matching ACL records appear.

3.  Add your custom role to each GAF ACL

    For each of the four matching ACL records:

    1.  Open the ACL record.
    2.  In the Roles related list, add your custom role.
    3.  Save the record.
4.  Configure skill access in AI Admin Hub

    Complete the setup for the CSM Suggested Steps Generation skill:

    -   In the **Define Access** step, add your custom role.
    -   In the **Select Display** step, add the same custom role.
    **Warning:** The `sn_gaf.data_writer` role includes `platform_ml_read` by default. Since `sn_gaf.data_writer` is assigned to agent roles like `sn_esm_agent`, those agents inherit `platform_ml_read` as well, which gives them broader access than intended. To avoid unintended access, never assign `platform_ml_read` directly to users.

5.  Verify GAF access

    Test that your custom role has proper access:

    1.  Assign the custom role to a test user.
    2.  Log in as the test user and navigate to a case.
    3.  Verify that Suggested Steps appear in Recommended Actions.

### Result

Your custom role now has the same access to Suggested Steps as the default `sn_customerservice_agent` and `sn_customerservice.consumer_agent` roles.

### What to do next

Before marking the Suggested Steps skill as complete and activating it for all agents, validate all aspects of the configuration.

|Validation item|Expected result|Status|
|---------------|---------------|------|
|Case volume|200+ similar cases identified for clustering|☐ Pass ☐ Fail|
|Short Description coverage|80%+ of cases have populated Short Description|☐ Pass ☐ Fail|
|Edited Conditions consistency|Conditions are formatted consistently across cases|☐ Pass ☐ Fail|
|Data freshness|Most cases created in last 6-12 months|☐ Pass ☐ Fail|
|Special characters|No parsing-breaking characters in descriptions|☐ Pass ☐ Fail|

|Configuration item|Verification step|Status|
|------------------|-----------------|------|
|Choose Inputs|Verify Short Description and Edited Conditions selected|☐ Pass ☐ Fail|
|Record Clustering|Clustering job completed successfully; check logs for errors|☐ Pass ☐ Fail|
|Define Access|Custom role added to Define Access \(or default role confirmed\)|☐ Pass ☐ Fail|
|Select Display|Same role toggled ON in Select Display \(not just present\)|☐ Pass ☐ Fail|
|Role Permissions|Role includes sn\_gaf.data\_writer permission|☐ Pass ☐ Fail|
|ACL Configuration|Role added to all 4 gaf\_suggested\_steps\_csm ACL records|☐ Pass ☐ Fail|

|Workspace item|Verification step|Status|
|--------------|-----------------|------|
|Recommended Action widget|Widget exists in form; "Hide recommended actions" is unchecked|☐ Pass ☐ Fail|
|Custom tables|If used: Widget data source set to custom table; extends case table|☐ Pass ☐ Fail|
|Widget visibility|Test user sees Recommended Actions section on case form|☐ Pass ☐ Fail|

|Access check|How to verify|Status|
|------------|-------------|------|
|Test user role|Confirm test user has assigned role|☐ Pass ☐ Fail|
|Role inheritance|Verify role includes sn\_gaf.data\_writer via Contains Roles|☐ Pass ☐ Fail|
|Skill activation|Confirm Suggested Steps skill shows "Activated" status|☐ Pass ☐ Fail|
|Browser cache|Clear cache and hard refresh; suggestions still visible|☐ Pass ☐ Fail|

|Quality check|Expected result|Status|
|-------------|---------------|------|
|Suggestions appear|Suggested Steps visible for test cases|☐ Pass ☐ Fail|
|Suggestion relevance|Suggestions are relevant to the case context|☐ Pass ☐ Fail|
|Suggestion consistency|Similar cases receive similar suggestions|☐ Pass ☐ Fail|
|Suggestion freshness|Suggestions reference recent resolution patterns|☐ Pass ☐ Fail|

