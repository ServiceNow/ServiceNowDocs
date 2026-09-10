---
title: Create on-call schedules for multiple groups
description: Use the on-call onboarding utility to create schedules for many groups at once instead of configuring each group individually. The On-Call Onboarding wizard helps you create on-call schedules for multiple teams by mapping shift templates, uploading a roster spreadsheet, and optionally configuring escalation policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/oc-create-bulk-schedule-onboarding.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-08-21"
reading_time_minutes: 4
keywords: [on-call onboarding wizard, bulk create schedules, rota\_admin, on-call roster upload]
breadcrumb: [Configuring On-Call Scheduling in Service Operations Workspace, On-Call Scheduling in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Create on-call schedules for multiple groups

Use the on-call onboarding utility to create schedules for many groups at once instead of configuring each group individually. The On-Call Onboarding wizard helps you create on-call schedules for multiple teams by mapping shift templates, uploading a roster spreadsheet, and optionally configuring escalation policies.

## Before you begin

Confirm that the following plugins are installed:

-   On-Call Scheduling \(com.snc.on\_call\_rotation\)
-   On-Call Onboarding \(com.snc.on\_call\_onboard\)

Create the on-call templates that you plan to map to teams, using standard on-call scheduling configuration. If you plan to use the optional escalation policy step, create the escalation policy templates that you want to apply.

Role required: rota\_admin

## About this task

The On-Call Onboarding wizard streamlines the creation of on-call schedules for multiple teams simultaneously.

For more information about the on-call scheduling setup activities the wizard streamlines, see [Configuring On-call Scheduling in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configuring-oncall-scheduling-sow.md). For more information about the Teams page, see [On-Call Scheduling in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/on-call-scheduling-in-sow.md).

**Note:**

Your progress is saved as you move between steps. However, selecting **Back** discards any unsaved changes on the current step.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    Alternatively, you can navigate to **On-Call Scheduling** &gt; **Bulk onboarding setup** &gt; **Excel Upload**.

2.  Select the teams icon \(\[Omitted image "icon-sow-teams.png"\]\).

3.  On the Teams page, select **On-Call Bulk Onboarding**

    The **On-Call Bulk Onboarding** button appears only when you have the required plugins are installed and you have the rota\_admin role.

    The Bulk schedule setup wizard page opens.

4.  Review the prerequisites and configure wizard options.

    1.  Review the prerequisites for shift and escalation policy templates and groups.

        1.  Verify that shift templates exist. If no templates exist, select **Create shift template**.
        2.  Verify that escalation policy templates exist. If no templates exist, select **Create escalation policy template**.
        The number of detected groups and existing shift templates displays.

    2.  Select how incidents escalate.

        -   **Escalate through a policy**: Notifies the on-call person, then escalates to others when the on-call person does not respond.

            Configure the escalation policy step later in the wizard.

        -   **Skip escalation policy**: Enables you to manually select on-call people to notify.
    3.  Select **Let's set it up**.

5.  Map teams to a shift templates.

    1.  Select one or more teams or groups from the teams list.

    2.  Select a shift template from the templates list.

    3.  Select **Connect teams**.

        A summary card appears showing the template name, configured shifts, and mapped teams.

    4.  To map additional teams, repeat these steps.

    5.  Select **Next - Roster upload**.

6.  Prepare and upload the roster spreadsheet.

    For more information about the workbook structure and the upload validation, see [On-call bulk roster template Excel file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/oc-bulk-schedule-roster-template.md).

    1.  Select **Download template**.

        The Excel file template contains prefilled shift information for each mapped team and includes placeholders that indicate where to add members and modify on-call configurations.

    2.  Update roster details as needed.

    3.  Add shift members on the corresponding team sheet in the workbook.

    4.  Upload the completed file.

        A preview of the uploaded data appears if no errors are found.

        Errors or warnings appear if issues are detected:

        -   Blocking errors prevent upload. Correct the file and select **Replace file**.
        -   Warnings indicate non-blocking issues and don't prevent continuing.
7.  Configure escalation policies for teams.

    This step appears only if you chose the **Escalate through a policy** option on the instructions screen.

    1.  Select a team from the list.

        Only mapped teams appear in the list.

    2.  Select a system default policy or an existing escalation policy template.

    3.  Define trigger conditions for the policy.

    4.  Select **Save**.

        A summary card appears showing the escalation policy name, configured trigger, and mapped teams.

    5.  Repeat these steps to configure policies for other teams.

8.  Review the configuration summary.

    The review screen displays counts for configured groups, shift templates, rosters, and escalation policies. Details appear in the following section showing each shift template with its mapped groups and each escalation policy with its associated groups. To make changes, return to an earlier step before submitting.

9.  Select **Create schedule**.

    -   The wizard creates new schedules without modifying existing ones.
    -   Escalation policies activate when the schedule is created.
    Schedule creation runs asynchronously, with each team or group processed as a separate unit. If creation fails for one or more groups, only those groups are rolled back without affecting others. To retry creation for failed groups through a new request, select **Redo**.

    An email notification with a link to the wizard is sent when the job completes.


## What to do next

To verify new schedules for the selected teams, select **View in Calendar** in the completion email or wizard.

-   **[On-call bulk roster template Excel file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/oc-bulk-schedule-roster-template.md)**  
The roster template workbook contains one sheet per mapped group, prefilled with shift template details.

**Parent Topic:**[Configuring On-Call Scheduling in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configuring-oncall-scheduling-sow.md)

