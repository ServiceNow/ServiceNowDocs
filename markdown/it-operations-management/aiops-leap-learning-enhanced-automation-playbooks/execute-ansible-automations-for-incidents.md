---
title: Execute Ansible playbooks for incidents
description: The Ansible Execution Agent launches Ansible playbooks mapped to LEAP resolution steps in Service Operations Workspace that can reduce manual effort and time to resolve incidents.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/execute-ansible-automations-for-incidents.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2025-01-07"
reading_time_minutes: 2
keywords: [Ansible execution, incident remediation, automation, Service Operations Workspace]
breadcrumb: [Use, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Execute Ansible playbooks for incidents

The Ansible Execution Agent launches Ansible playbooks mapped to LEAP resolution steps in Service Operations Workspace that can reduce manual effort and time to resolve incidents.

## Before you begin

-   The Ansible Execution Agent must be configured and enabled
-   Ansible jobs must be mapped to resolution steps for the predicted automation opportunity group

    For more information, see [Map Ansible jobs to resolution steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/map-ansible-jobs-to-resolution-steps.md).


Role required: sn\_itom\_leap.leap\_ansible\_agent\_worker

## About this task

When an incident arrives in SOW, LEAP predicts the automation opportunity group. If any matching automation opportunities are found with resolution steps, they are used in the prediction. If the predicted automation opportunities are mapped to Ansible jobs, they are presented to incident responders for execution. When execution starts, the agent logs a journal entry on the incident record.

## Procedure

1.  In SOW, select and open the required incident.

2.  In the **Recommendations** section, review any available Ansible playbooks.

    This section appears only if LEAP has predicted an automation opportunity group with step-to-job mappings. If the Recommendations section doesn't appear, the incident might not be matched to an automation opportunity group.

3.  Complete the resolution step.

<table id="choicetable_xyd_2f4_skc"><thead><tr><th align="left" id="d238571e133">

If the step has.

</th><th align="left" id="d238571e136">

Steps

</th></tr></thead><tbody><tr><td id="d238571e142">

**Manual \(no mapped Ansible jobs\)**

</td><td>

1.  Complete the manual step description provided by the Ansible Execution Agent.
2.  Select **Step Completed** after you finish it.


</td></tr><tr><td id="d238571e166">

**Automated \(mapped Ansible jobs\)**

</td><td>

1.  Select **Execute Ansible Playbook**.
2.  Review the job template details and complete all required launch inputs in the form presented, then proceed.
3.  After the job launches, the agent reports the Ansible job ID and status. Confirm when you're ready to move to the next step.


</td></tr></tbody>
</table>4.  Review the execution summary when all steps are completed.

    The agent provides a summary including total steps processed, jobs launched with their Ansible job IDs, manual steps completed, and any failures or errors. The agent also records the overall success or failure status on the incident record.

    Ask the agent directly in the ServiceNow Otto panel at any point during execution. You can check job status, view job output, cancel a running job, or relaunch a failed job.

5.  Close the incident if resolution is successful.


## Result

The Ansible Execution Agent runs the mapped Ansible jobs in sequence. It prompts you to complete any manual steps, and records the overall success or failure status on the incident record.

## What to do next

-   Review the Ansible job logs in Ansible Automation Platform for detailed execution information.
-   Document any issues or improvements for future automation opportunity mappings.
-   Update step-to-job mappings based on execution results and feedback.

