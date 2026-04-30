---
title: Workflow configuration
description: Define workflow, framework, regulation, and its associated versions, impacts, and view rules. CAM ships National Institute of Standards and Technology \(NIST\) workflow configuration by default, but you can create additional workflows for other frameworks such as Protective Security Policy Framework \(PSPF\) or custom internal frameworks.
locale: en-US
release: yokohama
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-12-03"
reading_time_minutes: 2
breadcrumb: [CAM workflow configuration, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Workflow configuration

Define workflow, framework, regulation, and its associated versions, impacts, and view rules. CAM ships National Institute of Standards and Technology \(NIST\) workflow configuration by default, but you can create additional workflows for other frameworks such as Protective Security Policy Framework \(PSPF\) or custom internal frameworks.

## Before you begin

-   The **Enable CAM workflow configuration** property must be turned on. For more information, see [Enable CAM workflow configuration](enable-cam-workflow-configuration.md).
-   You must run the migration scheduled jobs to associate existing authorization packages and boundaries with the workflow after enabling the CAM workflow configuration property. For more information, see [Run migration scheduled job](run-migration-scheduled-job.md).
-   With CAM advanced plugin \(app-grc-cont-auth-monitor-advanced\): You can create unlimited workflow configurations. If you don’t have CAM advanced plugin, you can create a maximum of two workflow configurations \(including the NIST workflow\).

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **Workflow Configurations**.

2.  To create a workflow configuration, select **New**.

3.  On the **Workflow Configuration New record** form, fill in the fields.

<table id="table_ofh_sqz_thc"><thead><tr><th>

Fields

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the workflow.

</td></tr><tr><td>

State Model

</td><td>

Select the state model to which you want to associate this workflow.**Note:** You must create the state model before you can map it to the workflow configuration. For more information, see [GRC state model configuration](cam-create-state-model.md).

</td></tr><tr><td>

Description

</td><td>

Enter details about the workflow and its purpose.

</td></tr></tbody>
</table>    ![Creating workflow configuration.](../image/WF-config.png)

4.  Select **Submit** to create the workflow.


## What to do next

To add versions, impact, and view rules to the workflow, see:

-   [Add version to workflow](add-version-and-impact-to-workflow.md)
-   [Add impact to version](add-impact-to-version.md)
-   [Add view rules to workflow](add-view-rules-to-workflow.md)

