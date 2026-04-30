---
title: Now Assist for Enterprise Architecture \(EA\) release notes
description: The ServiceNow Now Assist for Enterprise Architecture \(EA\) application introduces generative AI skills into the Enterprise Architecture Workspace. Now Assist for Enterprise Architecture \(EA\) was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
---

# Now Assist for Enterprise Architecture \(EA\) release notes

The ServiceNow® Now Assist for Enterprise Architecture \(EA\) application introduces generative AI skills into the Enterprise Architecture Workspace. Now Assist for Enterprise Architecture \(EA\) was enhanced and updated in the Zurich release.

## Now Assist for Enterprise Architecture \(EA\) highlights for the Zurich release

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   All Now Assist for EA skills are activated by default.
-   Use the Diagram change analysis Now Assist skill to compare an Enterprise Modeling and Visualization diagram with its previous version and generate a summary of the differences.

-   Use the Refine text Now Assist skill to elaborate or shorten text in the **Description** field of the business application, business capability, business process, and information object records. Also, use this skill to generate, elaborate, or shorten text in the **Reasoning** field under the **Planned Disposition** section of the business application record.

-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Use the Business Application Insights Now Assist skill to generate insights into your business applications.
-   Implement security in Now Assist AI agents with access control lists \(ACLs\).
-   On the Architectural Decision Records page, use the field in the Architectural Decision Records menu to enter queries and derive the required information from the Architectural Decision Records \(ADR\) artifact content.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use the Business Application Insights Now Assist skill to generate insights into your business applications.
-   Implement security in Now Assist AI agents with access control lists \(ACLs\).
-   On the Architectural Decision Records page, use the field in the Architectural Decision Records menu to enter queries and derive the required information from the Architectural Decision Records \(ADR\) artifact content.

Zurich Early Availability

-   Enhance your productivity by using the Now LLM Service or a supported third-party LLM with any Now Assist for Enterprise Architecture \(EA\) skill or AI agent.
-   Enhance your user experience with Coral that is used as the default theme for new portal, web, and mobile experiences.

See [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US) for more information.

**Important:** Now Assist for Enterprise Architecture \(EA\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Now Assist for Enterprise Architecture \(EA\) features

-   **[Compare Enterprise Modeling and Visualization diagrams](https://www.servicenow.com/docs/access?context=compare-modeling-diagrams&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Learn the details of the changes in the Enterprise Modeling and Visualization diagrams by comparing a diagram with its previous version. You can compare business application hierarchy, business capability map, and business process map diagrams.

-   **[Elaborate or shorten content in form fields](https://www.servicenow.com/docs/access?context=elaborate-or-shorten-content-form-fields&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Elaborate or shorten text in the **Description** field of the following records using the Refine text Now Assist skill:

    -   Business application
    -   Business capability
    -   Business process
    -   Value stream stages
    -   Information object
    Also, generate, elaborate, or shorten text in the **Reasoning** field in the **Planned Disposition** section of the business application record.

-   **[Business Application Insights skill configuration changes](https://www.servicenow.com/docs/access?context=configure-now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    For the Business application insights Now Assist skill, you can view the business application source fields based on which the business application insights are generated. Also, you can determine the availability of the skill by defining a specific criteria in the **Define access** tab of the Business application insights skill.

-   **[Role restrictions for Now Assist for EA skills](https://www.servicenow.com/docs/access?context=configure-now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Role restriction is added to the default roles associated with the following skills:

    -   Diagram change analysis
    -   ADR Doc Summarization and Actions
    -   Business application insights
    -   Refine text
-   **[Business Application Insights skill](https://www.servicenow.com/docs/access?context=generate-insights-into-ba&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Learn the details of business applications and gather concise and actionable insights on business applications from the summary that is generated by Now Assist for Enterprise Architecture \(EA\). The business application insights help you to make informed decisions without manually reviewing large volumes of data.

-   **[Implement access control lists for security in AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enable security implementation to execute AI agents and agentic workflows through access control lists \(ACLs\) and user identities.

    ACLs provide you with the capability to run AI agents and agentic workflow executions either as a dynamic user or an AI user.

    To learn about ACLs for Now Assist for Enterprise Architecture \(EA\) agents and skills, see [Configure Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=configure-now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US) and [Enterprise Architecture AI agent generate enterprise architecture diagram agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-aiagents-ea-diagramming-usecase&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).

-   **[Generate a summary of the Architectural Decision Records \(ADR\) document or get a particular information from the document](https://www.servicenow.com/docs/access?context=summarize-docs-genai-skill-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    On the Architectural Decision Records page, use the field option in the Now Assist menu to derive a particular information about the ADR content.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


## UI changes

-   The **Compare versions** button is added to the diagram page in the Enterprise Modeling and Visualization.
-   The Now Assist icon is added to the diagram page in the Enterprise Modeling and Visualization. You can use this icon to show or hide the Now Assist panel.
-   The Now Assist icon ![](../../product/now-assist-ea/image/now-assist-side-pane-icon.png) is displayed on selecting the description field of the business application, business capability, business process, value stream stages, and information objects.

    Also, the icon is displayed on selecting the **Reasoning** field in the **Planned Disposition** section of the business application record.

-   Added **Define availability** and **Define access** tabs in the Business application insights Now Assist skill configuration page in the Now Assist Admin console.

-   Added **Role restrictions to skill** section in the **Define access** tab of Now Assist skills in the Now Assist Admin console.

-   The **Generate insights** button is added to the business application page in the Enterprise Architecture Workspace.
-   Changes to the Architectural Decision Records page:
    -   The Now Assist drop-down menu is added.
    -   A field is added to the Now Assist drop-down menu to enter queries and get answers for Architectural Decision Records \(ADR\) artifact content.
    -   The **Summarize** button is moved to the Now Assist drop-down menu.
    -   In the context menu, the **Now Assist** button is changed to the Now Assist icon and placed as the first option of the context menu.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    [Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

## Activation information

Now Assist features are available with activation of the Now Assist for Enterprise Architecture \(EA\) plugin. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The Now Assist Admin console provides you with quick and effortless access to the important information that you must set up, configure, and monitor in Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist panel to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including content summarization in docs.


**Parent Topic:**[Enterprise Architecture release notes](enterprise-architecture-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

