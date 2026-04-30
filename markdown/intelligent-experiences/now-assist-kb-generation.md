---
title: KB generation
description: You can quickly write drafts of knowledge articles based on cases, incidents, or work order tasks with Now Assist. Generating article content with artificial intelligence \(AI\) enables agents to write efficiently as they address common user concerns.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-15"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, KB, Knowledge base, CSM, Service Operations, ITSM, Configurable Workspace, Workspace, FSM Configurable Workspace, Agent Workspace for HR Case Management, Now LLM, large language model, Knowledge article, Field Service Management, Customer Service Management, IT Service Management, HRSD, HR Service Delivery, Service Operations Workspace, SOW]
breadcrumb: [Content generation skills, Now Assist skills, Exploring Now Assist, Now Assist, Enable AI experiences]
---

# KB generation

You can quickly write drafts of knowledge articles based on cases, incidents, or work order tasks with Now Assist. Generating article content with artificial intelligence \(AI\) enables agents to write efficiently as they address common user concerns.

Generate a KB article from similar incidents 

## KB generation overview

Now Assist can create drafts of knowledge articles on how to resolve a case, an incident, or a work order task for agents to review and edit before publishing. Articles can be created in CSM Configurable Workspace, Service Operations Workspace for ITSM, Agent Workspace for HR Case Management, CSM/FSM Configurable Workspace, classic environment, or in the Now Assist panel. As a prerequisite to creating knowledge articles, it is recommended to activate the appropriate plugins for the respective workspaces. For example, to create a knowledge article from an incident, activate the [Activate KCS Integration for Incident Management](https://www.servicenow.com/docs/access?context=activate-kcs-integration-for-im&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) plugin \(com.snc.incident.knowledge\).

The following fields are used as inputs:

-   Short description
-   Description
-   Resolution notes
-   Close notes
-   Work notes
-   Comments

**Note:** Now LLM Service is the provider for this Now Assist skill.

Once a Now Assist application is installed, the agent will have the option to use Now Assist to generate a knowledge article on cases that are resolved and closed, incidents that are resolved, as well as work order tasks that are closed complete or closed incomplete.

In this example, an agent working in the CSM Configurable Workspace has the option to use Now Assist to draft an article.

![Dialog box in the CSM Configurable Workspace for creating a new knowledge article with a banner suggesting Now Assist help with writing for an agent to review, edit, and publish](../../../product/knowledge-management/image/Kb-gen-enable-Now-Assist-CSM.png "Generating a new knowledge article in the CSM Configurable Workspace")

In this example, an agent has used the Now Assist panel to start a draft from a resolved incident in the classic environment. After an article draft is generated, the agent clicks a link to review, edit, and publish the article.

![The Now Assist panel used to generate a knowledge article from an incident in the classic environment.](../images/KB-gen-NAP-CoreUI.png "Generating a knowledge article in the Now Assist panel")

## Generating knowledge articles

You can generate knowledge articles in the following products.

-   [Generate a knowledge article from the CSM Configurable Workspace and classic environment with Now Assist](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-csm-workspace&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)
-   [Generate a knowledge article from the Service Operations Workspace for ITSM and classic environment by using Now Assist](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)
-   [Generate a knowledge article from HR Agent Workspace with Now Assist](https://www.servicenow.com/docs/access?context=gen-kb-now-assisthr&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)
-   [Generate a knowledge article from multiple cases](https://www.servicenow.com/docs/access?context=gen-kb-now-assisthr-multi-case&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)
-   [Generate a knowledge article from the CSM/FSM Configurable Workspace and classic environment with Now Assist](https://www.servicenow.com/docs/access?context=na-fsm-generate-kb-article&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)
-   [Generate a knowledge article from the classic environment with Now Assist](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-coreui&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [Generate a knowledge article from the Now Assist panel](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-NApanel&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

## Availability

This skill is available in the workflows and products listed below.

<table id="table_r25_vxc_dbcfff"><thead><tr><th>

Workflow

</th><th>

Product

</th></tr></thead><tbody><tr><td>

Technology

</td><td>

[Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)

 [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)

</td></tr></tbody>
</table>