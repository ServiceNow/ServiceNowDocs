---
title: Configure extended tables
description: Create a child skill variant of the resolution notes generation skill to create concise summaries of case resolutions, helping agents to quickly understand resolution details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/configure-extended-table-support-for-the-resolution-notes-skill.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 2
breadcrumb: [Resolution notes generation, Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Configure extended tables

Create a child skill variant of the resolution notes generation skill to create concise summaries of case resolutions, helping agents to quickly understand resolution details.

## Before you begin

Role required: Admin to copy and configure the skill in Now Assist Admin \(NAA\). sn\_skill\_builder.admin to edit input configurations in Now Assist Skill Kit \(NASK\).

Confirm the following prerequisites are met before you begin:

-   Your instance must be running **uxc-generative-ai** version 12.2.2 or later.
-   The base resolution notes generation skill must already be activated.

## About this task

When you copy the resolution notes generation skill in Now Assist Admin, a child skill is created that inherits the parent skill's configuration. You then open the copied skill in Now Assist Skill Kit to select the target child table and configure the additional input fields that are injected into the AI prompt for that table. Once the skill is configured and published in NASK, and activated in NAA, the platform automatically uses the child skill when an agent triggers Resolution Notes generation on a case record that belongs to the extended table.

## Procedure

1.  Navigate to &gt; &gt; **Admin** &gt; **Now Assist admin** &gt; **Skills**.

2.  Select the **Customer** workflow and **CSM** as the product.

3.  Locate the **Resolution notes generation** skill and select **Make a copy**.

4.  In **General Details**, enter a name for the child skill that reflects the target case subtype.

5.  Enter a short description specific to this child skill.

6.  Select **Save and continue**.

    The child skill is created and inherits the parent skill's configuration. You cannot change the table name of the copied skill in Now Assist Admin. Table selection is performed in Now Assist Skill Kit as the next step.

7.  Navigate to **Now Assist Skill Kit** &gt; **ServiceNow skills**.

8.  Locate the copied skill you created earlier and open it.

9.  Select **Choose Input** by clicking Edit Skill Input pencil icon \[Omitted image "edit-new.png"\] Alt text: available under Skill contents.

10. Select the child or extended table that this skill variant should apply to.

    For example, select **Complaint \[sn\_customerservice\_complaint\]** from input table drop-down.

11. Add one or more additional input fields from the selected table to include in the AI prompt.

    For example, add **Account**, **Additional comments**, or **Address**. These fields are appended to the base prompt inputs inherited from the parent skill.

12. Select **Save and continue**.

13. Select **Clone prompt** to edit the prompt.

14. Complete skill configuration in Now Assist Admin, by selecting **Define Availability** to set conditions for when this child skill is active.

    -   Select **Skill is always available** to apply no restrictions.
    -   Select **Customize skill availability** to define conditions using the condition builder.
15. Select **Define Access** to control which roles can use this child skill.

16. Toggle **Display** to make the skill visible in the in-product desktop for agents.

17. Select **Review and Activate** to review your configuration, then select **Done**.

18. Select **Activate** to turn on the child skill for agents.

    The resolution notes generation child skill is active for the selected extended table. When an agent triggers **Resolution Notes Generation** on a case record that belongs to the configured child table, the platform automatically uses the child skill and its custom input fields to generate concise summaries of the case.


