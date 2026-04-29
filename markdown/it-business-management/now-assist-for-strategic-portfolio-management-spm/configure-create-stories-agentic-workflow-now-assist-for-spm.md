---
title: Configure Create stories agentic workflow with Now Assist for SPM
description: Using the AI Agent Studio, you can review and edit the configuration of the Create stories agentic workflow to modify the workflow description, steps, and agents included.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Configure Create stories agentic workflow with Now Assist for SPM

Using the AI Agent Studio, you can review and edit the configuration of the Create stories agentic workflow to modify the workflow description, steps, and agents included.

## Before you begin

Ensure that the Application scope of your ServiceNow instance is set to Now Assist for Strategic Portfolio Management \(SPM\).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  From the list of Agentic workflows, select **Create stories**.

    Each AI agent included in this workflow is active by default.

    **Note:** Only users with the Now Assist panel \(NAP\) role can access agents, even if the current agentic workflow doesn’t require that role.

3.  Review and modify the Create stories AI workflow using the following sections:

    1.  From the Define key requirements section, review the workflow description, steps involved, and AI agents added.
    2.  From the Define user access section, select which user roles can access this agentic workflow
    3.  From the Define data access section, select the type of user who can access this agentic workflow.
    4.  From the Add triggers section, add triggers if you like this agentic workflow to be launched according to predefined triggers.
    5.  From the Select channels and status section, choose the ways in which your users can access this agentic workflow. The default selection for Create stories workflow is the Now Assist panel.
4.  Select **Save and test**.

    The Create stories agentic workflow can only be tested in the Enterprise Agile Planning \(EAP\) workspace, from an epic or a feature record. To access EAP, navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**. For more information on how to use this agentic workflow in EAP, see [Generate multiple stories at once in EAP using Now Assist for SPM](generate-stories-from-epics-now-assist-eap.md).

    After testing the workflow, you can come back to AI Agent Studio to make any further changes.


**Related topics**  


[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[Using AI agent or agentic workflows in Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-na-spm-ai-agents.md)

[Strategic Portfolio Management AI agents for the monitor project tasks agentic workflow](../concept/na-spm-task-monitoring-usecase.md)

