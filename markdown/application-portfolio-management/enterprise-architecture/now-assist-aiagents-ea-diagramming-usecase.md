---
title: Enterprise Architecture AI agent generate enterprise architecture diagram agentic workflow
description: Use the Enterprise architecture diagrams AI agent to generate Enterprise Modeling and Visualization diagrams for business applications hierarchy and summarize them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/enterprise-architecture/now-assist-aiagents-ea-diagramming-usecase.html
release: zurich
product: Enterprise Architecture
classification: enterprise-architecture
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use AI agent agentic workflow, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Enterprise Architecture AI agent generate enterprise architecture diagram agentic workflow

Use the Enterprise architecture diagrams AI agent to generate Enterprise Modeling and Visualization diagrams for business applications hierarchy and summarize them.

## Generate enterprise architecture diagram overview

Use the Generate enterprise architecture diagram agentic workflow to create enterprise architecture diagrams for business applications hierarchy, through a conversation with an AI agent in the Now Assist panel. This agentic workflow accelerates the time to value for enterprise architects while building business hierarchy diagrams. It also enables non-enterprise architects to understand the context of an architectural diagram.

After generating the diagram, the AI agent suggests summarizing the created business application hierarchy diagram, listing all entities in the diagram and describing the relationship between them.

You can activate the agentic workflow template by setting the display settings to include the Now Assist panel. If you want to change instructions for this agentic workflow, you must duplicate the agentic workflow, adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead. For information on how to duplicate a agentic workflow, see duplicate the agentic workflow.

**Important:**

-   The Now Assist Panel user role \(now\_assist\_panel\_user\) is required to view the Now Assist panel on your instance.
-   The Enterprise Architecture user role \(sn\_apm.apm\_user\) is required to use the Generate enterprise architecture diagram agentic workflow.

## Role masking

Required role: sn\_apm.apm\_user.

Role masking enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

## Generate enterprise architecture diagram agentic workflow

Generate Enterprise Architecture diagrams for business applications hierarchy and summarize them.

For Admins to access or enable the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Generate enterprise architecture diagram**.

For users to invoke the agentic workflow:

1.  Select the Now Assist icon \(\[Omitted image "now-assist-panel-icon.png"\] Alt text: Now Assist icon.\) anywhere in your instance.
2.  Enter a prompt to create a diagram for a particular business application.

    It’s essential that your prompt contains the word **diagram** in some form. An example prompt is **Create a diagram for XYZ business application**.


## AI Agents used in the Generate enterprise architecture diagram agentic workflow

The Enterprise architecture diagrams AI agent is used in the Generate enterprise architecture diagram agentic workflow.

## Activate the Generate enterprise architecture diagram agentic workflow

To activate the Generate enterprise architecture diagram agentic workflow, follow the steps mentioned in .

**Note:** No triggers are required for the Generate enterprise architecture diagram agentic workflow.

However, in the Define key requirements page, in the **Define who can access this agentic workflow** section, you can review the roles that can access the agentic workflow. For **Generate enterprise architecture diagram** agentic workflow, sn\_apm.apm\_user role is applied by default.

To add access to more roles, perform the following:

1.  Set your application scope to Now Assist for Enterprise Architecture \(EA\). For information on how to change the application scope, see .
2.  Select the edit icon \(\[Omitted image "edit-icon.png"\] Alt text: Edit icon.\).
3.  On the Access Control page, in the **Requires role** section, select **Insert new row**.

    \[Omitted image "acl-add-new-user.png"\] Alt text: Access Control page for Generate Enterprise Architecture Diagram agentic workflow with a row to add new roles highlighted.

4.  On the pop-up window, enter the new role and select the save icon \(\[Omitted image "save-icon.png"\] Alt text: Save icon.\).

    \[Omitted image "save-icon-highlighted.png"\] Alt text: Save icon highlighted in the Requires role section.

5.  Select the header of the access control record and select **Save**.

    The new role is added to the **Define who can access this agentic workflow** section of the Define key requirements page.

    **Note:** To know more about security in Now Assist AI agents with Access Control Lists \(ACLs\), see .


Also, on the Select a UI display page, do the following:

1.  Enable the **Display** toggle.
2.  Select **Save and test**.
3.  On the Choose and AI agent or agentic workflow page, in the **Task** box, enter an instruction to test the Generate enterprise architecture diagram agentic workflow.

    An example instruction: **Create a business hierarchy map for XYZ business application**.

4.  Select **Start Test**.

    The agent executes the request for the agentic workflow.


\[Omitted image "ai-agent-diagrammer-test.png"\] Alt text: Generate enterprise architecture diagram agentic workflow output in the ServiceNow AI Agent Studio.

To view information on how to create AI agents and agentic workflows and how to use the AI Agent Studio, see the following:

-   AI Agent Studio
-   Install the AI Agent Studio
-   Install Now Assist AI Agents
-   
-   
-   
-   
-   

**Parent Topic:**[Using AI agent agentic workflow in Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/enterprise-architecture/using-na-ea-ai-agents.md)

