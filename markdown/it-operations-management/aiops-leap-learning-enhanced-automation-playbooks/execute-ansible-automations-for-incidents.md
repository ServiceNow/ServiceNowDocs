---
title: Execute Ansible automations for incidents
description: Use the Ansible Execution Agent to automatically launch mapped Ansible job templates during incident remediation in the Service Operations Workspace, reducing manual effort and accelerating mean time to resolution..
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/execute-ansible-automations-for-incidents.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2025-01-07"
reading_time_minutes: 2
keywords: [Ansible execution, incident remediation, automation, Service Operations Workspace]
breadcrumb: [Using LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Execute Ansible automations for incidents

Use the Ansible Execution Agent to automatically launch mapped Ansible job templates during incident remediation in the Service Operations Workspace, reducing manual effort and accelerating mean time to resolution..

## Before you begin

Before executing Ansible automations:

-   Step-to-job mappings must exist for the predicted automation opportunity group

    For more information, refer to [Map Ansible jobs to resolution steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/map-ansible-jobs-to-resolution-steps.md).

-   The mappings must be in **active** state
-   The Ansible Execution Agent must be configured and enabled

Role required: LEAP agent

## About this task

When an incident arrives in the SOW, LEAP predicts the automation opportunity group using existing clustering. If step-to-job mappings exist for that group, automation options are presented to incident responders for execution.

## Procedure

1.  In SOW, select the incident.

2.  In the **Ansible Automations** section, review the available automation options.

    This section appears only if LEAP has predicted an automation opportunity group with active step-to-job mappings.

3.  Select **Execute Ansible Playbook**.

    Complete the workflow by appropriately providing approvals to the tasks,

4.  For each automated step, provide the required inputs when prompted:

    1.  Review the job template details presented by the agent.

        The agent displays the template name, description, playbook, and current status.

    2.  Complete the input form with required survey questions and launch parameters.

        The agent consolidates all required inputs into a single form, including survey questions and any ask\_on\_launch parameters.

    3.  Approve the launch job to execute the automation.

5.  For manual steps, complete the required actions and confirm completion:

    1.  Review the manual step description provided by the agent.

    2.  Perform the required manual actions outside of ServiceNow.

    3.  Select **Step Completed** to confirm that the manual step is finished.

6.  Monitor job execution status and respond to agent prompts:

    -   The agent provides real-time status updates while a job is running.
    -   You can request job status at any time.
    -   After completing a step, the agent waits for your confirmation before proceeding to the next step.
7.  Review the execution summary when all steps are completed.

    The agent provides a summary including total steps processed, jobs launched with their Ansible Job IDs, manual steps completed, and any failures or errors.

8.  Update the incident record with the remediation results and close the incident if resolution is successful.


## Result

The mapped Ansible automations are executed in sequence, with manual steps completed as needed. The incident is remediated using the automated workflow defined in the step-to-job mapping.

## Example execution flow

For a database connectivity incident, the execution might proceed as follows:

1.  Agent: "Step 1: 'Restart the nginx service' — launching nginx-restart-playbook"
2.  Agent: "Launched successfully. Ansible Job ID: 12345. Status: Running"
3.  Agent: "Job completed successfully. Proceeding to next step."
4.  Agent: "Step 2: 'Flush DNS cache' — this step has no playbook mapped. Please complete this step manually."
5.  User: "Step completed" \(after manually flushing DNS cache\)
6.  Agent: "Step 3: 'Verify service health' — launching health-check-playbook"
7.  Agent: "All steps completed. Summary: 2 jobs launched, 1 manual step completed."

## What to do next

After execution:

-   Review the Ansible job logs in Ansible Automation Platform for detailed execution information.
-   Document any issues or improvements for future automation opportunity mappings.
-   Consider updating step-to-job mappings based on execution results and feedback.

