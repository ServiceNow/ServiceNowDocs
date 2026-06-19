---
title: Map Ansible jobs to resolution steps
description: Create mappings between automation opportunity resolution steps and Ansible job templates to enable automated incident remediation.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/map-ansible-jobs-to-resolution-steps.html
release: zurich
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2025-01-07"
reading_time_minutes: 2
keywords: [step-to-job mapping, Ansible jobs, resolution steps, automation mapping]
breadcrumb: [Using LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Map Ansible jobs to resolution steps

Create mappings between automation opportunity resolution steps and Ansible job templates to enable automated incident remediation.

## Before you begin

Before mapping Ansible jobs to resolution steps:

-   The Ansible discovery agent must have analyzed the automation opportunity
-   Job templates related to the resolution steps must exist and be available in your connected Ansible Automation Platform instance.
-   The [automation opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/automation-opportunities.md) must have generated resolution steps

Role required: **sn\_itom\_leap.leap\_admin**

## About this task

Step-to-job mapping creates the relationship between specific resolution steps and Ansible job templates. This mapping enables the Ansible execution agent to automatically launch the appropriate automations during incident remediation. At remediation time, the Ansible execution agent reads this mapping to determine which job template to launch for each step, in sequence.

## Procedure

1.  Navigate to **LEAP** &gt; **AI Teammate Dashboard**.

2.  Locate the automation opportunity that you want to configure for Ansible integration.

3.  Select **Map Ansible Jobs** to open the mapping modal.

    This button appears only after the Ansible discovery agent has analyzed the automation opportunity and identified candidate job templates.

    If the button does not appear, confirm that the Ansible discovery agent has completed analysis.

4.  Review the resolution steps displayed in the mapping modal.

    The modal parses the resolution steps and displays each step with a numbered index.

5.  For each resolution step, select the appropriate Ansible job templates from the drop-down list:

    -   Select one or more job templates if the step can be automated.

        A step can be automated if a matching job template exists.

    -   Leave the drop-down empty if the step requires manual intervention.
    The drop-down is populated with job templates discovered by the Ansible discovery agent. Each job template shows:

    -   Job template name
    -   Description
    -   Confidence score from the discovery analysis
6.  Review your mappings to verify that:

    -   Automated steps have appropriate job templates selected.
    -   Manual steps are left unmapped \(empty drop-down\).
    -   The sequence of steps makes logical sense for incident remediation.
7.  Select **Save** to create the step-to-job mapping.

    The mapping is saved to the `sn_itom_leap_ansible_mapping` table in an active state.


## Result

The step-to-job mapping is created and activated. The automation opportunity detail page now displays each resolution step with its mapped job templates. Manual steps are indicated with **\(manual\)**. The mapping is available for incident remediation in the Service Operations Workspace.

## Step-to-job mapping

After saving a mapping, the automation opportunity displays resolution steps like this:

```
Step 1: Restart the nginx service
  ▶ nginx-restart-playbook
  ▶ service-restart-generic

Step 2: Flush DNS cache
  (manual)

Step 3: Verify service health
  ▶ health-check-playbook
```

## What to do next

After creating the mapping:

**Note:** If resolution steps are regenerated after saving, this mapping is deleted and must be recreated.

Editing replaces the existing mapping. Don't edit a mapping while it is in use during an active incident remediation.

