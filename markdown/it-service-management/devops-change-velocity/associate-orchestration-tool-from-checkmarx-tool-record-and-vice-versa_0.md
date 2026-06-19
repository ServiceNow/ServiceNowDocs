---
title: Associate orchestration tool from Checkmarx tool record and vice-versa
description: You can associate orchestration tool from the Checkmarx tool record and associate the Checkmarx tool record from the orchestration or pipeline record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-change-velocity/associate-orchestration-tool-from-checkmarx-tool-record-and-vice-versa\_0.html
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Checkmarx, Integrate, DevOps Change Velocity, IT Service Management]
---

# Associate orchestration tool from Checkmarx tool record and vice-versa

You can associate orchestration tool from the Checkmarx tool record and associate the Checkmarx tool record from the orchestration or pipeline record.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces &gt;DevOps Change Workspace &gt; Tools &gt; Security tools**.

2.  From the Security tools list, select the tool with which you want to associate an orchestration tool.

3.  In the Security tool record, navigate to the Orchestration tools tab.

4.  Select **Associate**.

5.  In the Select tool dialog box, select the orchestration tools you want to associate with your security tool, and select **Associate**. \[Omitted image "checkmarx-09.png"\] Alt text: Select tools dialog box to associate orchestration tool from Checkmarx tool record

6.  In the Add custom action dialog box, copy the required custom action code for your orchestration tool, and add it as a step in your pipelines. \[Omitted image "checkmarx-08.png"\] Alt text: Add custom action dialog box

7.  Select **Done**.

    **Note:** In a similar way, you can associate a security tool instance with an orchestration tool or pipeline record. You can navigate to the orchestration tool or pipeline record, and from the Security tools tab, you can select **Associate**. In the dialog boxes that are displayed, you can select the security tool instances to associate and then copy the custom action to add it in the corresponding pipeline step.


**Parent Topic:**[Checkmarx integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/checkmarx-integration-with-devops-change-velocity.md)

