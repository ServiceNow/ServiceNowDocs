---
title: Security Incident Closure workflow
description: Close the security incident by updating the incident state.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Closure workflow

Close the security incident by updating the incident state.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  For example, go to **Lists** &gt; **Security Incidents** &gt; **Open incidents**.

3.  Open an incident that you want to close.

4.  Go to the **Details** tab.

5.  Drill down to the incident state and select **Close**.

6.  Perform the closing activities.

    -   This is a mandatory step to review any task before closing a security incident. Any response tasks must be reviewed by the analyst and closed or canceled before closing as security incident. When the Analyst clicks on **Review active tasks**, it takes the user to the **Response Tasks** tab. A session message is displayed prompting that you are in the process of closing a security incident. Click **continue**.

    -   Click **Continue**. The first step – review active tasks in closing the security incident is complete.

        ![Close the security incident pop-up window: Reviewing active tasks.](../image/close-incident.png "Reviewing closure tasks")

    -   Move to the next step to review the active playbooks for the analyst to review, which is an optional step. You can click the link to review the active playbook task and close them as required.

        **Note:** Any active workflow\(s\), playbook activities, and flows will be automatically cancelled on closure of the security incident.

        ![Close the security incident pop-up window: Reviewing active playbooks.](../image/review-playbook-close.png "Review playbook tasks")

        ![Using the Phishing Manual Playbook to analyse a user reported phishing incident.](../image/review-playbook-to-close.png)

    -   Post-incident review report: You will now be moved to review the post-incident activities to proceed further with the closure. If the assessment is optional then skip the step or if the assessment is mandatory then take the assessment and complete it.

        ![Close the security incident pop-up window: Take assessment.](../image/review-assessment-close-incident.png "Review/Take assessment")

        ![Post Incident Review: Assessment of the incident.](../image/assessment-closure.png)

    -   Configure/preview report: This is again an optional step, click the link to review report and proceed to **Next** step.

        ![Post Incident Review: Reports of the incident.](../image/reports-closure.png)

    -   Provide Resolution details: The analyst can select the check box to create knowledge articles automatically.
    -   Provide the Closure code, Closure notes and click **Close incident**.

        ![Close the security incident pop-up window: Providing closing code and closing notes.](../image/resolution-code-closure.png)

    **Note:** By any chance if the analyst cancels the **Close the security incident** dialogue box, then the analyst can navigate to the **Details** tab and change the incident state to **close** to continue with the closure.


**Parent Topic:**[Using SIR Workspace](../reference/using-sir-workspace.md)

**Related topics**  


[Working with Security Incident Records](using-analyst-workspace.md)

[Security Incident Playbook](security-incident-playbook.md#)

[Prerequisites for the Playbooks](../../playbook-migration-guide/concept/getting-started-with-processes.md)

[Rebuilding existing playbooks in Workflow Studio](../../playbook-migration-guide/concept/rebuilding-existing-playbooks-on-pad.md)

[Activity Definitions](../../playbook-migration-guide/concept/build-activities.md)

[Sample Playbooks for SIR Workspace](../../playbook-migration-guide/concept/sir-workspace-playbooks.md)

[Working with MSI Records](working-with-msi-records.md)

[Working with Form UI actions](enable_workspace_form_ui_actions.md)

[Handle security incidents using Advanced Work Assignment](../task/handle-incidents-using-awa.md)

