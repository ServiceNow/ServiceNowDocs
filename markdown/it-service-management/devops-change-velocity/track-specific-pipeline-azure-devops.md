---
title: Track specific pipelines in Azure DevOps
description: Enable and configure specific pipelines in Azure DevOps that you want to track. Select the pipelines you want to monitor and receive job notifications from Azure DevOps.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Track specific pipelines in Azure DevOps

Enable and configure specific pipelines in Azure DevOps that you want to track. Select the pipelines you want to monitor and receive job notifications from Azure DevOps.

## Before you begin

-   Connect DevOps to Azure DevOps tools.
-   Ensure that you have modeled, configured, and associated Azure pipelines to DevOps.
-   Review how to configure form layouts. For more information, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

Role required: admin, personalize\_form

## About this task

By default, the **Track Specific Pipeline** field is set to **False** when you discover Azure DevOps orchestration tasks and pipelines. The **Track** flag for all Azure DevOps pipelines is also disabled. So, by default, this leads to all pipelines sending job notifications to DevOps and increased processing times, which could cause the pipeline you really want to track to be delayed. So, enable the **Track Specific Pipeline** check box to process only notifications for the pipeline events that you specify to track, and ignore all other pipeline notifications.

## Procedure

1.  Navigate to **All** &gt; **DevOps** &gt; **Tools** &gt; **Orchestration Tools**, and open the Azure DevOps tool record.

2.  Click the **Additional Actions** icon \(![additional actions icon](../image/additional-actions-icon.png)\), and select **Configure** &gt; **Form Layout**.

3.  Move the **Track Specific Pipeline** field to the selected list.

4.  Click **Save**.

    You are redirected back to the Azure DevOps form in the DevOps tool, and the **Track Specific Pipeline** check box appears.

5.  Select the **Track Specific Pipeline** check box.

6.  Navigate to the Pipelines related list.

7.  Click the **Update Personalized List** icon \(![Update personalized list](../image/personalize-list.png)\).

8.  In the Personalize List Columns form, move the **Track** field to the Selected list.

    Track Specific pipeline ![Track Specific pipelines](../image/track-specific-pipeline.png)

9.  Click **OK**.

    You are redirected back to the Pipelines related list, where the **Track** field now appears.

10. Navigate to the pipeline step which you want to track, double-click the **Track** field.

11. Change the **Track** field's value to **true**, and click **Save**.


## Result

Only the pipelines that have **Track** field set to **true** in the Pipelines related list are now being tracked and sent to the Inbound Events table \[sn\_devops\_inbound\_event\_list.do\]. All pipelines that have the **Track** field set to **false** are ignored.

**Note:**

-   If the **Track Specific Pipeline** check box is selected only those pipelines that have the **Track** field value set to **true** are tracked and sent to the Inbound Events table. If **Track** field is set to **false** for all pipelines none of the pipelines are tracked.
-   If the **Track Specific Pipeline** check box is unselected, all events of the pipeline are tracked and sent to the Inbound Events table.

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)

