---
title: Security Incident Closure workflow
description: Close the security incident by updating the incident state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/security-incident-closure-workflow\_0.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
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

    -   This is a mandatory step to review any task before closing a security incident. Any response tasks must be reviewed by the analyst and closed or canceled before closing as security incident. When the Analyst selects on **Review active tasks**, it takes the user to the **Response Tasks** tab. A session message is displayed prompting that you're in the process of closing a security incident. Select **continue**.

    -   Select **Continue**. The first step – review active tasks in closing the security incident is complete.

        \[Omitted image "close-incident.png"\] Alt text: Close the security incident pop-up window: Reviewing active tasks.

    -   Move to the next step to review the active playbooks for the analyst to review, which is an optional step. You can select the link to review the active playbook task and close them as required.

        **Note:** Any active workflow\(s\), playbook activities, and flows will be automatically cancelled on closure of the security incident.

        \[Omitted image "review-playbook-close.png"\] Alt text: Close the security incident pop-up window: Reviewing active playbooks.

        \[Omitted image "review-playbook-to-close.png"\] Alt text: Using the Phishing Manual Playbook to analyse a user reported phishing incident.

    -   Post-incident review report: You will now be moved to review the post-incident activities to proceed further with the closure. If the assessment is optional then skip the step or if the assessment is mandatory then take the assessment and complete it.

        \[Omitted image "review-assessment-close-incident.png"\] Alt text: Close the security incident pop-up window: Take assessment.

        \[Omitted image "assessment-closure.png"\] Alt text: Post Incident Review: Assessment of the incident.

    -   Configure/preview report: This is again an optional step, select the link to review report and proceed to **Next** step.

        \[Omitted image "reports-closure.png"\] Alt text: Post Incident Review: Reports of the incident.

    -   Provide Resolution details: The analyst can select the check box to create knowledge articles automatically.
    -   Provide the Closure code, Closure notes and select **Close incident**.

        \[Omitted image "resolution-code-closure.png"\] Alt text: Close the security incident pop-up window: Providing closing code and closing notes.

    **Note:** By any chance if the analyst cancels the **Close the security incident** dialogue box, then the analyst can navigate to the **Details** tab and change the incident state to **close** to continue with the closure.


**Parent Topic:**[Using SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/using-sir-workspace.md)

**Related topics**  


[Working with Security Incident Records]()

[Security Incident Playbook]()

[Prerequisites for the Playbooks]()

[Rebuilding existing playbooks in Workflow Studio]()

[Activity Definitions]()

[Sample Playbooks for SIR Workspace]()

[Working with MSI Records]()

[Working with Form UI actions]()

[Handle security incidents using Advanced Work Assignment]()

