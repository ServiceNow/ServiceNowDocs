---
title: Map Ansible jobs to resolution steps
description: Create mappings between automation opportunity resolution steps and Ansible job templates to enable automated incident remediation.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/map-ansible-jobs-to-resolution-steps.html
release: brazil
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2025-01-07"
reading_time_minutes: 2
keywords: [step-to-job mapping, Ansible jobs, resolution steps, automation mapping]
breadcrumb: [Use, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Map Ansible jobs to resolution steps

Create mappings between automation opportunity resolution steps and Ansible job templates to enable automated incident remediation.

## Before you begin

Before mapping Ansible jobs to resolution steps:

-   The [automation opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/automation-opportunities.md) must have generated resolution steps
-   The Ansible discovery agent must have analyzed the automation opportunity
-   Job templates related to the resolution steps must exist and be available in your connected Ansible Automation Platform instance.
-   
Role required: LEAP admin

## About this task

Step-to-job mapping creates the relationship between specific resolution steps and Ansible job templates. This mapping enables the Ansible execution agent to automatically launch the appropriate automation during incident remediation. At remediation time, the Ansible execution agent reads this mapping to determine which job template to launch for each step, in sequence.

## Procedure

1.  Navigate to **Learning-Enhanced Automation Platform\(LEAP\)**.

2.  Locate the automation opportunity that you want to configure for Ansible integration.

3.  In the automation opportunity details page, the Ready for review section displays whether there are Ansible playbooks detected.

4.  Select **Review details** to open the mapping modal.

    \[Omitted image "map\_ansible\_playbooks.png"\] Alt text: Map resolution steps to Ansible pllaybooks

    This button appears only after the Ansible discovery agent has analyzed the automation opportunity and identified candidate job templates. If the button does not appear, confirm that the Ansible discovery agent has completed analysis.

5.  Review the resolution steps displayed in the mapping modal.

    The modal parses the resolution steps and displays each step with a numbered index.

6.  For each resolution step, select the appropriate Ansible job templates from the drop-down list:

    -   Select a job template for the step to be automated.

        A step can be automated if a matching job template exists.

    -   Leave the drop-down empty if the step requires manual intervention.
    The drop-down is populated with job templates discovered by the Ansible discovery agent. Each job template shows:

    -   Job template name
    -   Description
7.  Review your mappings to verify that:

    -   Automated steps have appropriate job template selected.
    -   Manual steps are left unmapped \(empty drop-down\).
    -   The sequence of steps makes logical sense for incident remediation.
8.  Select **Save** to create the mapping.

    The mapping is saved to the `sn_itom_leap_ansible_mapping` table.


## Result

The step-to-job mapping is created. The automation opportunity detail page now displays each resolution step with its mapped job template. Manual steps are indicated with **\(manual\)**. The mapping is available for incident remediation in Service Operations Workspace.

## Step-to-job mapping

After saving a mapping, the automation opportunity displays resolution steps like this:

```
Step 1: Restart the nginx service
  ▶ nginx-restart-playbook

Step 2: Flush DNS cache
  (manual)

Step 3: Verify service health
  ▶ health-check-playbook
```

## What to do next

After creating the mapping:

**Note:** If resolution steps are regenerated after saving, this mapping is deleted and must be recreated.

Editing replaces the existing mapping. Don't edit a mapping while it is in use during an active incident remediation.

