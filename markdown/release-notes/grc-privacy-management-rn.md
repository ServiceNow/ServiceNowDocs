---
title: Privacy Management release notes
description: The ServiceNow Privacy Management application enables you to manage your organization's privacy risks and compliance to protect your customers, employees, and suppliers. See the following sections for release notes by version.Privacy Management, version 23.0.1, introduces data transfers to record the movement of personal data, transfer mechanisms to associate legal safeguards with those movements, AI-recommended control objectives and risk statements during privacy assessment reviews, and multi-language support for the Personal Data Rights \(PDR\) external-facing form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/grc-privacy-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [privacy management, data transfer, personal data rights, reviewer assist]
breadcrumb: [Governance, Risk, and Compliance release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Privacy Management release notes

The ServiceNow® Privacy Management application enables you to manage your organization's privacy risks and compliance to protect your customers, employees, and suppliers. See the following sections for release notes by version.

## About Privacy Management

-   Identify, assess, and mitigate privacy risk across your organization's processing activities.
-   Maintain a central record of processing activities, entities, and privacy elements such as information objects and data subjects.
-   Maintain a library of authority documents, citations, control objectives, and risk statements with [Privacy content accelerator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/privacy-content-accelerator.md).
-   Manage data subject rights requests from intake through fulfillment with Personal Data Rights.
-   Track and resolve privacy issues from assessments, processing activities, and incidents with Privacy Case Management.

See [Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/privacy-management.md) for more information.

## Activation and other requirements

**Note:** Privacy Management is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Install Privacy Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-rn-landing.md)

## Version 23.0.1

Privacy Management, version 23.0.1, introduces data transfers to record the movement of personal data, transfer mechanisms to associate legal safeguards with those movements, AI-recommended control objectives and risk statements during privacy assessment reviews, and multi-language support for the Personal Data Rights \(PDR\) external-facing form.

### What's new

-   **[AI-reviewer assist for control objective and risk statement recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-reccos-for-pia.md)**

    When a privacy assessment task moves to the Review state, the assigned reviewer can generate AI-recommended control objectives and risk statements for the associated processing activity.

    The Control Objective Recommender and Risk Statement Recommender skills analyze completed assessment responses and surface relevant records from the privacy library. Each recommendation includes an AI suggestion guide that explains why the record was suggested, citing the specific response or record detail that triggered it.

    Each risk statement recommendation also surfaces related control objectives that serve as mitigating controls for the identified risks. When you accept a risk statement, this control-to-risk mapping is carried over to the processing activity.

    Accepted records are automatically added to the Applicable scope tab on the assessment task. After you close the task, the corresponding controls and risks are automatically scoped to the processing activity.

-   **[Record data transfers in processing activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/data-transfers.md)**

    Data transfer records capture the movement of personal data between hierarchy nodes in a processing activity. These records are generated automatically from a privacy assessment when a business user defines relationships that send or receive personal data. Adding data subject types and their locations to these relationships generates additional transfer records, which capture each distinct movement between nodes and data subject locations.

    You can review the records in the Data transfers tab of the privacy assessment task and remove those that don't apply. After you close the assessment task, the remaining transfer records appear in the **Regulatory details** &gt; **Data transfers** tab of a processing activity. You can also manually add or remove data transfers from this tab.

-   **[Transfer mechanisms for data transfers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/transfer-mechanisms.md)**
    -   Privacy analysts can add a transfer mechanism to a data transfer record to associate the legal safeguard that regulate the movement of personal data.
    -   Privacy managers can add new transfer mechanisms in the Privacy Workspace or update existing ones.
-   **[Multi-language support in the Personal Data Rights \(PDR\) external-facing form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/translate-pdr-form-text.md)**

    The external-facing PDR form now supports translations in multiple languages. The selected language drives the form text, including labels, instructions, options, and error messages.

-   **[Mandatory fields in the Personal Data Rights \(PDR\) external-facing form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/map-request-type-to-ds.md)**

    Configure mandatory and optional fields for each request type. Requesters must complete all mandatory fields on the external-facing PDR form to submit their request.


### What's changed

-   **[Data lineage map UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/editing-data-lineage.md)**

    When you select the relationship line between two nodes in the data lineage map, a side pane opens with the relationship details, where you can edit or remove a relationship.

-   **[Node location fields in the hierarchy modal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/new-relationship-forms.md)**

    The hierarchy modal now includes node location fields. The Define relationship step includes a **Primary node location** field, and the Relationship details step includes a **Related node location** field.

-   **[Data subject selection in hierarchy relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/config-ds-sys-property-hierarchy.md)**

    Privacy admins can enable data subject selection for custom relationship types in a hierarchy by modifying the sn\_privacy.relationship\_involving\_data\_subjects system property.

-   **[Applicable scope tab in a privacy assessment task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-reccos-for-pia.md#applicable-scope-tab-pia)**

    The Applicable scope tab on the assessment task record replaces the former Outcomes tab. It lists the control objectives and risk statements that have been scoped to the processing activity through manual addition, automation rules, or AI-assisted recommendations.

-   **[External-facing Personal Data Rights \(PDR\) form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/submit-privacy-request-external-pdr.md)**

    The external-facing PDR form layout is updated to support mobile screens.


### What's deprecated or removed

-   **Now LLM service deprecation**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


### Plugin information

-   **New plugins**

    AI Data Explorer \(sn\_pa\_ai\_canvas\): Install the plugin to enable privacy managers and analysts to analyze privacy data, explore trends across sources, and surface actionable recommendations using natural language queries. Use the **Explore** button on the home pages of the Privacy Workspace and Personal Data Rights Workspace to open AI Data Explorer. For information on installing, configuring and using it, see [Use AI to explore data with AI Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/ai-data-explorer.md).

    GRC Issue Management \(sn\_grc\_issue\_mgmt\): Install the plugin to enable a redesigned issue management experience with configurable workflows, custom state models, issue approvals, and centralized administration. For more information, see [Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/issue-workflows.md).


