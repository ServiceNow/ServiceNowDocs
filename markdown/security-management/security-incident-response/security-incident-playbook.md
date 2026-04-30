---
title: Security Incident Playbook
description: Invoke the security incident playbook flow automatically or manually.Use this section to add playbook manually.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Playbook

Invoke the security incident playbook flow automatically or manually.

A Playbook is visible only if at least one playbook is associated with a security incident. The playbook component works only for the Process Automation Designer \(PAD\) built processes and not for the flow designer-built flows. For the existing flow designer enabled flows, it will continue to work, and the activities will be continuing to be rendered as response tasks.

There are two ways of associating playbook with the security incident:

-   Automatically invoke playbook
-   Manually add playbook

## Invoke playbook automatically

For a Playbook to be invoked automatically, a process needs to be defined using **Process Automation Designer \(PAD\)**, and when the trigger condition is met then automatically the playbook tab is rendered with the playbook activities being displayed.

## Add playbook manually

For a Playbook to be invoked manually, navigate to the Form UI action drop down and select **Add Playbook**. For more information see, [Add Playbook](security-incident-playbook.md#)

**Note:** If there is already a playbook available then the new playbooks added will run in parallel to the existing playbooks.

-   Within the playbook, the analyst can filter the playbook cards by status.
-   The analyst can cancel a playbook by selecting it from the ellipse icon.
-   Within each activity, the analyst will be able to perform the actions defined within the activity cards such as Skip, Mark as complete, Cancel, or Orchestration actions such as Submit to sandbox, Search Emails and so on.
-   Each of these actions are defined within the activity definition, and the complete card visible is customizable at the time of building the activity definition itself.

**Note:** All the future activity definitions and the next steps to be performed are displayed with a lock icon and are in read-only mode to the user. The playbook display mode is controlled by a configuration as explained below.

1.  Navigate to **All** &gt; **Playbook Experiences**.
2.  In the Playbook Experiences page, select an **SIR Playbook Experience**.

    ![The Security Incident Playbook experience](../image/playbook-experience.png "Playbook Experience")

    The **Playbook Experience SIR Playbook Experience** page is displayed.

    ![Editing the SIR Playbook Experience record](../image/playbook-expereince-record.png "Playbook Experience Record")

3.  Click on the **Configuration** record.

    ![Playbook configuration record](../image/playbook-expereince-config-record.png)

4.  In the Configuration tab, click the SIR Playbook Experience Configuration.

    ![Edit the Playbook Configuration](../image/playbook-config-record.png "Playbook Configuration")

5.  Navigate to the **Pending Item Visibility** field's drop down list, select the desired option and save the record. Choose from the following options:
    -   **Hide pending activities**: Select this option to hide the pending activities that you would like to see on the playbook section of the workspace.

        ![Hide pending activities in Phishing Manual playbook.](../image/playbook-hide-pending-activities.png "User Reported Phishing Example")

    -   **Show pending stages and activities**: Select this option to show pending stages and activities that you would to like to see on the playbook section of the workspace.

        ![Show pending stages and activities in Phishing Manual playbook](../image/playbook-show-pending-stages.png "Show pending stages and activities")

    -   **Hide pending activities and stages**: Select this option to hide pending activities and stages,that you would like to see on the playbook section of the workspace.

        ![Hide pending activities and stages in Phishing Manual playbook](../image/playbook-hide-pending-activities-stages.png "Hide pending activities and stages")

6.  On the Playbook section, use the filter option to filter the activities by Playbook card status \(activity definition\).

    ![Playbook card status](../image/playbook-card-status-filters.png "Playbook card status")


**Parent Topic:**[Using SIR Workspace](../reference/using-sir-workspace.md)

**Related topics**  


[Working with Security Incident Records](using-analyst-workspace.md)

[Prerequisites for the Playbooks](../../playbook-migration-guide/concept/getting-started-with-processes.md)

[Rebuilding existing playbooks in Workflow Studio](../../playbook-migration-guide/concept/rebuilding-existing-playbooks-on-pad.md)

[Activity Definitions](../../playbook-migration-guide/concept/build-activities.md)

[Sample Playbooks for SIR Workspace](../../playbook-migration-guide/concept/sir-workspace-playbooks.md)

[Working with MSI Records](working-with-msi-records.md)

[Working with Form UI actions](enable_workspace_form_ui_actions.md)

[Security Incident Closure workflow](security-incident-closure-workflow_0.md)

[Handle security incidents using Advanced Work Assignment](../task/handle-incidents-using-awa.md)

## Add Playbook

Use this section to add playbook manually.

### Before you begin

Role required: sn\_si.analyst

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Analyst Workspace**.

2.  Open an incident record.

3.  Click **Add Playbook**.

    ![Add a playbook manually](../image/manually-invoke-playbook.png)

    The **Add Playbook** dialogue box is displayed.

    ![Add playbook](../image/manually-invoke-playbook1.png)

4.  Select the playbook template.

5.  Click **Add Playbook**.

    A confirmation message dialogue box is displayed for you to confirm.

6.  Click **Add Anyway**.

    ![Confirmation message](../image/addanyway-button.png)

7.  The **Playbook** gets added next to the **Details** tab.

    ![Playbook confirmation message](../image/playbook-attached.png)

8.  Click the **Playbook** tab.

    ![Playbook activities](../image/playbook-tasks.png)

9.  Perform the series of activities as listed to move to the next level.

    **Note:** If a Security incident is associated with a playbook, until the associated playbook gets closed or cancelled the user cannot again associate the same playbook to the same security incident.


