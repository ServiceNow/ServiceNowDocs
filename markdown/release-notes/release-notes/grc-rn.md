---
title: Common Core release notes
description: The ServiceNow Integrated Risk Management \(IRM\) application enables your organization to continue to provide its business services during adverse operational events, such as a pandemic, extreme weather, or hacking. Integrated Risk Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [Common Core, GRC Common Core, GRC Common]
---

# Common Core release notes

The ServiceNow® Integrated Risk Management \(IRM\) application enables your organization to continue to provide its business services during adverse operational events, such as a pandemic, extreme weather, or hacking. Integrated Risk Management was enhanced and updated in the Zurich release.

## IRM highlights for the Zurich release

-   Use the report a GRC issue AI agent in the Employee Center to report issues through a guided conversational experience.
-   Ensure seamless access for users and groups referenced in user fields on records by leveraging entity-based access restrictions through record attribute user access configuration. Minimize manual effort, reduce administrative overhead, and enable entity-based access with minimal disruption.
-   Configure which task and tab settings appear in My Tasks by marking them Active or Inactive in the applicable table for easier management. Use the Active/Inactive flag in the GRC choice table to control visibility.
-   Automatically sync and maintain entity names in GRC with associated CI names to improve data consistency and reduce manual effort.
-   Authenticate users with the MCP Server to add a Model Context Protocol tool to AI agents using the Model Context Protocol Client.
-   Create ACLs for AI agents and agentic workflows to customize who can discover and trigger AI agents and agentic workflows.
-   Generate control recommendations for each regulatory alert to address compliance requirements. Use these suggestions to save time, minimize manual effort, and ensure a consistent response to regulatory changes.
-   Apply access restrictions at the record level by using the record access update utility in guided assistance. You can also preview the impacted record counts before updating and review the results and execution logs after the update.
-   Apply access restrictions automatically to newly created or modified records using entity-based record access rules.
-   Deactivate the entity-based access configurations.
-   Enable entity-based access on custom GRC tables.

For detailed documentation, see [Common Governance, Risk, and Compliance features](https://www.servicenow.com/docs/access?context=common-grc-features&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US).

**Important:** IRM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Entity based record access update utility guided experience](https://www.servicenow.com/docs/access?context=entity-based-access-playbook&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Apply entity-based access \(EBA\) restrictions at the record level by using guided assistance in the entity based record access update utility. Guided assistance consists of a four-step process:

    1.  Define the scope for the relevant entities
    2.  Scope the record types
    3.  Apply the conditions to each record type to refine the scope
    4.  Review the selected records before you execute and initiate the update
    See the execution logs for a status after each update. You can get the details about the impacted records, applied scopes, and outcomes.

-   ****

    The report a GRC issue AI agent is now available in the Employee Center, enabling employee users to report issues through a guided conversational experience. As users respond to prompts, the agent structures the issue and recommends relevant controls, entities, and policies based on the input provided. The AI agent helps ensure that the issue is well-defined and enriched with contextual information before it's submitted.

-   **[Entity based record access rules to secure new records](https://www.servicenow.com/docs/access?context=continuous-monitoring-of-entity-based-access&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Configure entity-based record access rules on record types to ensure that access restrictions are applied automatically to secure new records or modified records related to entities with active EBA configurations.

-   ****

    Maintain seamless access for users and groups referenced in record fields when entity-based access restrictions are applied. This feature enables users and groups referenced in a record’s user or group fields to access the records they are associated with. By configuring record-level user access at the table or record type level, it reduces administrative overhead and streamlines EBA adoption with minimal disruption.

-   **[Deactivation of entity-based access configuration](https://www.servicenow.com/docs/access?context=deactivating-entity-based-access&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Deactivate the entity-based access configuration, enabling the system to automatically assess the records that it impacts. If entity-based access configuration is restricting a record, the access restrictions are removed. If other configurations also apply to the record, the restrictions remain in place and only the selected configuration is deactivated.

-   ****

    Apply or remove domain-specific tags across multiple records at once. This streamlines workspace management by letting you quickly filter and organize records, for example, you can exclude non-privacy-tagged items in the Privacy Workspace for a more focused, efficient view.

-   **[Entity record page enhancements](https://www.servicenow.com/docs/access?context=entities-in-risk-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Entity type and Downstream Risks \(now renamed as Risks\) related lists on the Entity record page have been converted to UIB pages, providing a more intuitive and modern interface. The Downstream Risks related list has been moved to the dedicated Risks page, featuring organized tabs for Directly related risks, Suggested risks, and All risks.

    **Note:** You may experience issues with custom actions that emit events on the Risks or Entity type related lists on the Entity record page. To ensure a smooth transition and adopt these changes, refer to [KB2593527](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2593527) for detailed guidance.

-   **[Model Text Protocol \(MCP\) Client](https://www.servicenow.com/docs/access?context=mcp-client&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enable users of the ServiceNow® AI Agent Studio to access tools that are hosted externally and published using an MCP Server via the Model Context Protocol Client application.

    Authenticate users with the MCP Server to add the MCP tool to an AI agent.

-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The **Add** button on the **AI agents** tab is added as a drop-down providing different agent types for AI agent creation:

    -   Chat
    -   External
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Configure the Access Control Lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   ****

    Easily manage which configurations appear on the My Tasks page by marking them Active or Inactive. This gives you flexibility to enable or disable configurations without manual intervention, simplifying administration and improving control. An Active/Inactive flag has also been introduced in the My Choice table for enhanced configuration management.


-   ****

    Entity names in GRC now automatically update when the associated CI name changes. This enhancement improves data consistency, reduces manual effort, and ensures alignment between CI and Entity records without requiring custom automation.


## UI changes

-   **[Downstream risks related list](https://www.servicenow.com/docs/access?context=entities-in-risk-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Downstream risks related list on the entity record page has been renamed Risks.

-   **Coral theme**

    Coral is now the default theme for Vendor Management Workspace, portal, and mobile experiences. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[States in the entity based record access update utility](https://www.servicenow.com/docs/access?context=eba-configuration-states&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    A new Preview state has been added to the record access update utility life cycle. You can now review the estimated number of impacted records before you apply the restrictions. This step helps you to validate the selected scope, assess potential impacts, and make adjustments, if needed. It also adds an extra layer of control and reduces the risk of unintended access changes.


## Activation information

Install Integrated Risk Management and Now Assist for IRM by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

