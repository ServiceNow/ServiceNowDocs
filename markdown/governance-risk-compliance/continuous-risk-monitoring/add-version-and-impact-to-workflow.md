---
title: Add version to workflow
description: Add workflow versions to a workflow configuration to support different revisions or iterations of your workflow. Workflow versions filter control objectives based on the version requirements.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Workflow configuration, CAM workflow configuration, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Add version to workflow

Add workflow versions to a workflow configuration to support different revisions or iterations of your workflow. Workflow versions filter control objectives based on the version requirements.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## About this task

Workflow versions and impacts work together to filter control objectives:

-   Version: Filters by workflow revision \(for example, National Institute of Standards and Technology \(NIST\) 800-53 Revision 4, Revision 5\).
-   Impact: Filters by risk level \(for example, Low, Moderate, High\).
-   Combined filter: Version and Impact conditions are applied together to generate baseline controls.

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **Workflow Configurations**.

2.  Select a Workflow Configuration from the list to add the version.

    ![Selecting workflow.](../image/WF-version-and-impact1.png)

3.  On the **Versions** tab, select **New** to add a version.

    ![Selecting new version.](../image/WF-version-and-impact2.png)

    A new version record page displays to add the version details to the selected workflow configuration.

4.  On the form, fill the fields.

<table id="table_g5w_4rz_thc"><thead><tr><th>

Fields

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the version name \(For example, Revision 4, Revision 5, Version 2.0, or 2025 Edition\).

</td></tr><tr><td>

Workflow configuration

</td><td>

The workflow configuration is automatically populated based on the workflow that you have selected.

</td></tr><tr><td>

Active

</td><td>

Select the **Active** option to activate the version.

</td></tr><tr><td>

Order

</td><td>

The order in which you want to list the versions in the authorization package.

</td></tr><tr><td>

Filter condition

</td><td>

Enter the condition to filter control objectives for this version.**Note:** When configuring filter conditions for impact, the version filter conditions now appear on the same screen for reference.

</td></tr></tbody>
</table>    ![New version fields.](../image/WF-version-and-impact3.png)

5.  Select **Submit** to add the new version to the selected workflow configuration.

    You can view the new version listed in the **Versions** tab.


## Result

The workflow version is available for selection in authorization packages based on the workflow configuration selected in the associated authorization boundary. Based on the defined condition, CAM filters control objectives and creates appropriate baseline controls.

## What to do next

[Add impact to version](add-impact-to-version.md)

