---
title: Associate orchestration tool from Veracode tool record and vice-versa
description: You can associate orchestration tool from the Veracode tool record and associate the Veracode tool record from the orchestration or pipeline record.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Veracode, Integrate, DevOps Change Velocity, IT Service Management]
---

# Associate orchestration tool from Veracode tool record and vice-versa

You can associate orchestration tool from the Veracode tool record and associate the Veracode tool record from the orchestration or pipeline record.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces &gt;DevOps Change Workspace &gt; Tools &gt; Security tools**.

2.  From the Security tools list, select the tool with which you want to associate an orchestration tool.

3.  In the Security tool record, navigate to the Orchestration tools tab.

4.  Select **Associate orchestration tools**.

5.  In the Select tool dialog box, select the orchestration tools you want to associate with your security tool, and select **Associate orchestration tools**. ![Associate orchestration tool for a security tool](../image/asso-orch-tool-sec-01.png)

6.  In the Add custom action dialog box, copy the required custom action code for your orchestration tool, and add it as a step in your pipelines. ![Add custom action to your pipeline](../image/asso-orch-tool-sec-02.png)

7.  Select **Done**.

    **Note:** In a similar way, you can associate a security tool instance with an orchestration tool or pipeline record. You can navigate to the orchestration tool or pipeline record, and from the Security tools tab, you can select **Associate security tool**. In the dialog boxes that are displayed, you can select the security tool instances to associate and then copy the custom action to add it in the corresponding pipeline step.


**Parent Topic:**[Veracode integration with DevOps Change Velocity](../concept/veracode-integration-with-devops-change-velocity.md)

