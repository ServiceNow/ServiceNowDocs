---
title: Enterprise Architecture AI agent generate enterprise architecture diagram agentic workflow
description: Use the Enterprise architecture diagrams AI agent to generate Enterprise Modeling and Visualization diagrams for business applications hierarchy and summarize them.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-03-07"
reading_time_minutes: 3
breadcrumb: [Use AI agent agentic workflow, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Enterprise Architecture AI agent generate enterprise architecture diagram agentic workflow

Use the Enterprise architecture diagrams AI agent to generate Enterprise Modeling and Visualization diagrams for business applications hierarchy and summarize them.

## Generate enterprise architecture diagram overview

Use the Generate enterprise architecture diagram agentic workflow to create enterprise architecture diagrams for business applications hierarchy, through a conversation with an AI agent in the Now Assist panel. This agentic workflow accelerates the time to value for enterprise architects while building business hierarchy diagrams. It also enables non-enterprise architects to understand the context of an architectural diagram.

After generating the diagram, the AI agent suggests summarizing the created business application hierarchy diagram, listing all entities in the diagram and describing the relationship between them.

You can activate the agentic workflow template by setting the display settings to include the Now Assist panel. If you want to change instructions for this agentic workflow, you must duplicate the agentic workflow, adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead. For information on how to duplicate a agentic workflow, see [duplicate the agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

**Important:**

-   The Now Assist Panel user role \(now\_assist\_panel\_user\) is required to view the Now Assist panel on your instance.
-   The Enterprise Architecture user role \(sn\_apm.apm\_user\) is required to use the Generate enterprise architecture diagram agentic workflow.

## Generate enterprise architecture diagram agentic workflow

Generate Enterprise Architecture diagrams for business applications hierarchy and summarize them.

For Admins to access or enable the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Generate enterprise architecture diagram**.

For users to invoke the agentic workflow:

1.  Select the Now Assist icon \(![Now Assist icon.](../image/now-assist-panel-icon.png)\) anywhere in your instance.
2.  Enter a prompt to create a diagram for a particular business application.

    It’s essential that your prompt contains the word **diagram** in some form. An example prompt is **Create a diagram for XYZ business application**.


## AI Agents used in the Generate enterprise architecture diagram agentic workflow

The Enterprise architecture diagrams AI agent is used in the Generate enterprise architecture diagram agentic workflow.

## Activate the Generate enterprise architecture diagram agentic workflow

To activate the Generate enterprise architecture diagram agentic workflow, follow the steps mentioned in [Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

**Note:** No triggers are required for the Generate enterprise architecture diagram agentic workflow.

However, in the Define key requirements page, in the **Define who can access this agentic workflow** section, you can review the roles that can access the agentic workflow. For **Generate enterprise architecture diagram** agentic workflow, sn\_apm.apm\_user role is applied by default.

To add access to more roles, perform the following:

1.  Set your application scope to Now Assist for Enterprise Architecture \(EA\). For information on how to change the application scope, see [Select an application from the application picker](https://www.servicenow.com/docs/access?context=t_SelectAnAppFromTheAppPicker&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
2.  Select the edit icon \(![Edit icon.](../image/edit-icon.png)\).
3.  On the Access Control page, in the **Requires role** section, select **Insert new row**.

    ![Access Control page for Generate Enterprise Architecture Diagram agentic workflow with a row to add new roles highlighted.](../image/acl-add-new-user.png)

4.  On the pop-up window, enter the new role and select the save icon \(![Save icon.](../image/save-icon.png)\).

    ![Save icon highlighted in the Requires role section.](../image/save-icon-highlighted.png)

5.  Select the header of the access control record and select **Save**.

    The new role is added to the **Define who can access this agentic workflow** section of the Define key requirements page.

    **Note:** To know more about security in Now Assist AI agents with Access Control Lists \(ACLs\), see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).


Also, on the Select a UI display page, do the following:

1.  Enable the **Display** toggle.
2.  Select **Save and test**.
3.  On the Choose and AI agent or agentic workflow page, in the **Task** box, enter an instruction to test the Generate enterprise architecture diagram agentic workflow.

    An example instruction: **Create a business hierarchy map for XYZ business application**.

4.  Select **Start Test**.

    The agent executes the request for the agentic workflow.


![Generate enterprise architecture diagram agentic workflow output in the ServiceNow AI Agent Studio.](../image/ai-agent-diagrammer-test.png)

To view information on how to create AI agents and agentic workflows and how to use the AI Agent Studio, see the following:

-   [AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
-   [Install the AI Agent Studio](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
-   [Install Now Assist AI Agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
-   [Configuring Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
-   [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
-   [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
-   [Test an AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
-   [Test an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

**Parent Topic:**[Using AI agent agentic workflow in Now Assist for Enterprise Architecture \(EA\)](using-na-ea-ai-agents.md)

