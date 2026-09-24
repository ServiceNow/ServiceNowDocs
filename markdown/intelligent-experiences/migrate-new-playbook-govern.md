---
title: Migrate to updated AI asset onboarding playbook
description: Configure the new AI asset onboarding playbook to simplify AI asset management through structured lifecycle workflows. The migration also includes an opt-in to decide between moving to the new playbook or continuing in the existing playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/migrate-new-playbook-govern.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [playbook]
breadcrumb: [AI Control Tower playbooks, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Migrate to updated AI asset onboarding playbook

Configure the new AI asset onboarding playbook to simplify AI asset management through structured lifecycle workflows. The migration also includes an opt-in to decide between moving to the new playbook or continuing in the existing playbook.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Settings** &gt; **Playbooks**.

    The **Playbooks** settings page shows all published playbooks and their current status.

2.  Locate the **Switch to AI Asset Onboarding playbook V2** option.

    This card displays the scope of the migration. It includes a description of what will change and a **Review and switch** button.

    **Note:** Switching to the new playbook will not migrate customization that has been implemented in the existing playbook and flows. However, it will flag the customized playbooks and flows. This enables you to make fixes to prevent disruptions.

3.  Select **Review and switch**.

4.  On the **What’s changing** tab, review the three sections: **What's changing**, **What it affects**, and **Confirm**.

    The dialog lists artifacts that will be deactivated, remain active without changes, and activate as part of the migration.

    | | |
    |---|---|
    |What's changing|Review details of the new playbook structure that is being introduced. The system retires artifacts specific to the old playbook during migration. After the switch, the new AI Asset Onboarding playbook introduces updates six areas: playbook structure, task assignment per asset, task rule configuration, lifecycle progression triggers, stage-specific user views, and new task type addition. The new approach replaces fixed paths with flexible, configurable options.|
    |What it affects|Existing playbooks and flows remain active without changes. Review these items to verify they do not create duplicate approval tasks. The system activates one new customized AI asset onboarding playbook with all required components|
    |Confirm|The system deactivates the old playbook automatically. Your customized flows and playbooks remain active and require your review. The new playbook activates with all required components. Confirm that you understand the old setup deactivates while your customizations remain active.|

    **Note:**

    Switching to the new playbook impacts only new AI Assets. Existing AI Assets which are already part of a playbook will not be impacted.

5.  Expand each section to confirm the specific playbooks, flows, and configurations affected by the switch.

    Based on your app version, complete the appropriate steps:

<table id="table_mth_jt1_nkc"><thead><tr><th>

Scenario and impact

</th><th>

Steps

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

App versions from `AICT UI Application v7.1.1`

</td></tr><tr><td>

There are no impacts. AI Asset Onboarding V2 is enabled by default and requires no migration.

</td><td>

Not applicable.

</td></tr><tr><td class="sub-head" colspan="2">

App versions before `AICT UI Application v7.1.1`.

</td></tr><tr><td>

If no customizations were made to the default playbook, the switch to the new playbook is executed with no impacts.

 Impact: No impact

 Remedial measures: No remedial measures are required.

</td><td>

1.  In **Settings** &gt; **Playbooks**, select **Review impacts** on the **Switch to AI Asset Onboarding V2** banner.
2.  Select **Review and switch** to complete the migration.


</td></tr><tr><td>

-   If the default playbook has been customized
-   If a custom playbook has been created to replace the default playbook and the default playbook has been deactivated.
 Impact: No impact

 Remedial measures: The existing playbook needs to be deactivated.

</td><td>

1.  Deactivate the customized playbook.
2.  In **Settings** &gt; **Playbooks**, select **Review and switch** to switch to AI Asset Onboarding V2.


</td></tr><tr><td>

If the default flows are customized.

 Impact: Customized flows associated with the old playbook may create duplicate tasks when they continue to run alongside the new playbook.

 Remedial measures: Configure flow to check if AI Asset Governance Details record is linked to the old playbook and end the flow to prevent the flow from executing further. Add this check to all customized flows that generate tasks.

</td><td>

Modify the flow to introduce a check. For more information, see [Edit a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/flow-edit.md)1.  Add an action **Check if AI Asset Governance Details record is linked to the old playbook** to the customized flow.
2.  Add an **If** condition immediately after the check.
3.  Configure the condition: if the AI Asset Governance Details record is not linked to the old playbook, add an **End Flow** step.

This configuration allows the flow to exit early for new assets tied to the V2 playbook and continue running only for existing assets on the old playbook.

**Note:** The action **Check if AI Asset Governance Details record is linked to the old playbook** is available only after upgrading to version `6.1.2`

</td></tr><tr><td>

If the V2 playbook is to be cloned and customized.

</td><td>

1.  Create a copy of the V2 playbook and modify it as needed.
2.  Set the **sn\_ai\_asset\_mgmt.new\_playbook\_opt\_in** system property to `true`.
3.  Deactivate the old playbook.
4.  Activate the newly cloned playbook.
5.  In the Playbook Configuration record, set the **Playbook record** field to `AI Asset Onboarding V2`.
6.  In the `AIAssetLifecycleAPI` script include, update the *NEW\_PLAYBOOK\_SYS\_ID* variable to reference the copied playbook's sys\_id.


</td></tr></tbody>
</table>6.  Select **Continue**.

7.  Review any additional confirmation prompts and select **Confirm** to complete the switch.


**Parent Topic:**[AI Control Tower playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-playbooks-reference.md)

