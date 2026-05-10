---
title: Enterprise Architecture release notes
description: The ServiceNow Enterprise Architecture application unites strategic and operational teams, enabling organizations to achieve their business objectives. Enterprise Architecture was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 13
---

# Enterprise Architecture release notes

The ServiceNow® Enterprise Architecture application unites strategic and operational teams, enabling organizations to achieve their business objectives. Enterprise Architecture was enhanced and updated in the Australia release.

## Enterprise Architecture Workspace highlights for the Australia release

[Australia Patch 2](../quality/australia-patch-2.md)

-   Associate AI systems from AI Control Tower with business applications in the Enterprise Architecture Workspace to track AI adoption, governance status, and business context across your application portfolio. You can also associate one or more business applications when submitting an AI use case request in the Service Portal.
-   You can use the Now Assist panel to search your published TRM catalog records using natural language queries.

[Australia Patch 1](../quality/australia-patch-1.md)

-   When you compare two versions of an Enterprise Modeling and Visualization diagram, the diagram canvas highlights the differences visually. This makes it easier to identify what has changed at a glance, without relying solely on the Now Assist change summary panel.
-   Support for models OpenAI GPT-5 mini, Claude Haiku 4.5, and Google Gemini 3.0 Flash added for any Now Assist for Enterprise Architecture \(EA\) skill.

Australia Early Availability

-   Publish a Technology Reference Model \(TRM\) catalog using the ServiceNow Knowledge Management product to easily find, adopt, and share approved technology standards through a centralized, risk‑managed TRM catalog. The published TRM catalog is accessible across the organization or beyond, as needed. You can use the Now Assist panel to search your published TRM catalog records using natural language queries.
-   Create documents for Enterprise Modeling and Visualization diagrams to publish, share, and archive diagrams together with their associated data. With a single action, you can transform diagrams into ready‑to‑use documents, reducing manual copy‑and‑paste effort. The generated documents support collaboration and editing, can be exported to PDF, and can support approval workflows for governed review and lifecycle management.
-   Add and manage labels on the relationship lines more easily in empty diagrams, hierarchy diagrams, and Business Process Modeling Notation \(BPMN\) diagrams.
-   Visually explore and analyze architecture data modeled using the Architecture Analyzer feature in the Enterprise Architecture Workspace.
-   Store and manage architectural documents, including documents generated from diagrams in the modeling tool using the Architectural Documents under Information Portfolio.
-   Explore and analyze Common Service Data Model \(CSDM\) architecture relationships directly on a visual canvas in the Enterprise Architecture Workspace. You can assess current state of an entity, understand dependencies, and share the insights with stakeholders.
-   Apply the granular level admin role changes to provide safer and more controlled approach to manage access in the Enterprise Architecture Workspace.
-   Determine the bubble size using the Overall score indicator on the Application Rationalization Bubble Chart page.
-   Generate insights for the widgets available on the Enterprise Architecture Dashboard page.
-   Generate a context-sensitive summary for business applications based on the page that you’re generating the summary from.
-   Compare any two versions of a diagram and generate a summary in the Enterprise Modeling and Visualization page.

See [Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ea-workspace.md) for more information.

## New in the Australia release

[Australia Patch 2](../quality/australia-patch-2.md)

-   **[AI systems on business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-aict.md)**

    View and manage AI systems associated with a business application from the **AI Systems** tab on a business application record in the Enterprise Architecture Workspace.

    -   View all AI systems linked to a business application, organized by governance status as **Managed** \(submitted for AI Steward review\) or **Unmanaged** \(created but not yet submitted for review\).
    -   Add an existing AI system to a business application record.
    -   Remove an AI system association from a business application record without deleting the AI system record in AI Control Tower.
    -   Open the full AI system record in AI Control Tower directly from the **AI Systems** tab of a business application record in Enterprise Architecture Workspace, to review governance details, lifecycle status, and related assets.
    Associate a business application with a new AI use case at intake using the **Business Applications** field on the **Request an AI use case** catalog item in the service portal. The association is established on submission, and the AI system appears as unmanaged on the corresponding business application records in the Enterprise Architecture Workspace.

-   **[AI Search on the TRM catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ai-search-trm-cat.md)**

    Search published TRM catalog records using natural language queries in the Now Assist panel. EA Workspace ships default AI Search configuration that automatically indexes TRM catalog records you publish. To make previously published TRM catalog records searchable, you can manually trigger indexing. For information, see [Index previously published TRM catalog records for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/index-archive-pub-trm-cat.md) or [AI Search on the TRM catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ai-search-trm-cat.md).


[Australia Patch 1](../quality/australia-patch-1.md)

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Exploring the architecture analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-explore-arch-analyzer.md)Architecture Analyzer**
    -   Added support for analyzing all EA extended entities that are part of Enterprise Modeling and Visualization, such as
        -   Control
        -   Digital integration
        -   Digital interface
        -   GRC risk
        -   Product capability
        -   TRM product
    -   The **Clear** button clears all the selections made in the **Add to canvas** boxes.

Australia Early Availability

-   **[Enterprise Modeling and Visualization enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-ent-model-and-visual.md)**

    Label management improvements for diagrams:

    -   Add labels: Double-click empty areas or use the adornment tool to automatically place labels in optimal positions. You can add multiple labels to relationship lines.
    -   Edit and delete labels: Change existing labels or remove them as needed.
    -   Move with shapes: Labels maintain their relative position when you move associated shapes.

        **Note:** After submitting the diagram for approval, the labels can’t be edited.

    Accessibility enhancements in Enterprise Modeling and Visualization:

    -   Magnify content up to 400% while maintaining full access to all information and features.
    -   Navigate the interface using the keyboard.
    -   Access the shape context menu using the keyboard.
    -   See pop-over menus when hovering over connector lines.
    ArchiMate shape library enhancements:

    The ArchiMate shape library has been enhanced to align with ArchiMate 3.2 standards, with new categories, elements, and updates to existing shapes.

    -   Implementation and Migration category: Added this category with the following shape elements:
        -   Implementation event
        -   Gap
        -   Work package
        -   Deliverable
        -   Plateau
        -   Location
        -   Group
    -   Relationship Type category- Added this category with the following shape elements:
        -   And junction
        -   Or junction
-   **[Exploring the publishing center in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/publishing-center-in-ea-workspace.md)**

    Use the Publishing Center to control publishing workflows, monitor status, and view publishing history from a single location.

-   **[Publish TRM catalog to a knowledge base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/working-with-publishing-center.md)**
    -   Configure TRM catalogs and apply filters for products and lifecycle phases.
    -   Manage publishing workflows with status updates from Draft to Published.
    -   View publishing job history in the Run logs tab.
    -   Access the published TRM catalog using the generated knowledge base URL.
-   **Enhancements to the [Value stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-manage-value-streams.md) and [Value stream stage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-manage-value-stream-stages.md) related lists**
    -   Value stream: View associated value stream stages and application models as related lists. You can add, edit, or remove the associated value stream stages and application models.
    -   Value stream stage: View associated business processes and business capabilities. Add or remove business processes and business capabilities. You can also view the value stream stage as a related list in the business process and business capability records.
-   **[Enhancements to the Business Process related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-manage-business-processes.md)**

    View the value stream stage as a related list of a business process.

-   **[Enhancements to the Business Capability related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-manage-business-capabilities.md)**

    View the value stream stage as a related list of a business capability.

-   **[Create documents for the Enterprise Modeling and Visualization diagrams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/create-documents-for-diagrams.md)**
    -   Save diagram as a document using the Generate document option from the Enterprise Modeling and Visualization diagrams page.
    -   Define templates for the documents that can be created and used from the Diagrams page.
    -   Tag components that can be included in the templates to generate documents.
    -   View associated documents from the Diagrams page.
-   **[Exploring the architecture analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-explore-arch-analyzer.md)Architecture Analyzer**
    -   The Architectural Analyzer helps you to analyze architecture data without creating or maintaining custom diagrams. You can visually explore relationships across applications, services, and infrastructure to quickly understand dependencies and collaborate on architecture decisions. You can also understand the potential impact of architectural changes across applications and services.
-   **[Application rationalization page enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-rationalize-business-applications.md)**

    Added an Overall score indicator to show the overall average score of a business application. Use this indicator to determine the bubble size of a business application on the Bubble Chart page. You can compare the overall scores of different business applications using their individual bubble sizes.

-   **[Business application summarization skill enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/generate-insights-into-ba.md)**

    Generate context-sensitive business application summaries from the following pages:

    -   Business capability hierarchy page: On generating a business application summary from this page, information such as the associated primary and secondary capabilities and the position in the capability hierarchy are displayed along with the general information about the business application.
    -   Application rationalization list view page: On generating a business application summary from this page, information such as the indicator scores \(actual and normalized scores\), and associated demand details are displayed along with the general information about the business application.
    -   Application rationalization bubble chart page: On generating a business application summary from this page, information such as x and y-axis details, and planned disposition details are displayed along with the general information about the business application.
-   **[Generate insights for Enterprise Architecture Workspace dashboard widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/generate-insights-ea-dashboard.md)Now Assist**

    Generate insights for the widgets available on the Enterprise Architecture Dashboard page using the Now Assist Explorer icon available on the header of each widget.

-   **[Diagram change analysis skill enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/compare-modeling-diagrams.md)**
    -   Compare any two versions of a diagram and generate a summary of the changes.
    -   Select any version as a primary or secondary version to compare.
    -   Generate a summary for real-time changes made to the primary version while already comparing it to another diagram version.
    -   Modify diagram versions to compare using the Diagram comparison icon on the diagram comparison page.
    -   Identify differences faster when comparing two versions of a diagram, by using the color-coded highlights on the canvas. Newly added shapes and relationship lines appear in green and modified ones appear in yellow.

## UI changes

[Australia Patch 2](../quality/australia-patch-2.md)

-   Added the **AI Systems** tab to business application records in the Enterprise Architecture Workspace. The tab displays **Managed** and **Unmanaged** sections, each listing associated AI systems.
-   Added the **Business Applications** field to the **Request an AI use case** catalog item in the service portal. The field is available only when the Enterprise Architecture application is installed and business applications are configured. You can select multiple business applications. Retired business applications are not available for selection.
-   Added a read-only **Business applications** related list under **Related assets** on AI system records in AI Control Tower. This list shows the business applications associated with each AI system.

[Australia Patch 1](../quality/australia-patch-1.md)

-   The diagram comparison canvas displays visual indicators to highlight new or modified shapes and entities. Newly added shapes and relationship lines appear in green and modified ones appear in yellow.

Australia Early Availability

-   Added the Publishing center section in the Setup page.
-   Changed the label of Publisher to Manufacturer in the TRM page.
-   Added the Business process and Business capability related lists to the Value stream and Value stream stage records.
-   Added the Value stream stage as a related list to the Business Capability and Business Process records.
-   Added the following two menu options in the More actions menu of the Diagrams page in the Enterprise Modeling and Visualization:
    -   Generate document
    -   View all documents
-   Added the Documents section in the Setup page to create templates for documents that are created from the Enterprise Modeling and Visualization diagrams page.
-   Renamed the **Certifications** tab on the Enterprise Architecture Workspace Home page to **My Certifications**.
-   Introduced **Document** as a new format or file type replacing **ADR** file type. The **File type** drop-down label is changed to **Format**.
-   Added the **Architectural Documents** section under the Information Portfolio on the Portfolio page.
-   Added the Architecture Analyzer icon \(add image\) to the left navigation menu of the Enterprise Architecture Workspace.
-   The Now Assist icon is added to the header of each widget on the Enterprise Architecture Dashboard page.
-   The Now Assist icon is removed from the side panel of the Enterprise Modeling and Visualization diagram page. It’s added to the Compare diagrams page, which opens when you select the **Compare versions** button in the diagram canvas header.
-   The **Compare versions** button is added to the header of the canvas on the diagram comparison page.

## Changed in this release

-   **[Granular admin role changes in Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-gran-admin-role-changes.md)**

    Added the granular level admin role \(sn\_apm.apm\_admin\) to the following system properties in the Enterprise Architecture:

    -   **sn\_apm\_trm.is\_product\_life\_cycle\_tech\_debt\_enabled**: Make this property false to disable calculating level 2 technical debt.
    -   **glide.ui.sn\_apm\_trm\_product\_request\_activity.fields**: TRM Product Request activity formatter fields.
    -   **sn\_apm\_trm.noOfPublishersPerTRMPage**: The number of publishers to show per page.
    -   **glide.ui.sn\_apm\_trm\_product\_lifecycle\_request\_activity.fields**: TRM Product Lifecycle Request activity formatter fields.
    -   **sn\_apm.noOfSoftwareModelsPerTPMPage**: The number of software models to show per page. This property is used for client-side pagination.
    -   **sn\_apm.discoveryModelProductTypesForTPMSuggestions**: Product types of discovery models to consider for TPM software suggestions.
    -   **sn\_apm.noOfSDLCComponentPerTPMPage**: The number of Agile Development components to show per page.
    -   **glide.ui.cmdb\_ci\_business\_app\_activity.fields**: Business application activity formatter fields.
    -   **sn\_apm.startRangeOfTPMLifecycle**: The number of years before the current date is included when displaying software model lifecycle phases in the TPM timeline.
    -   **sn\_apm.endRangeOfTPMLifecycle**: The number of years beyond the current date is included when displaying software model lifecycle phases in the TPM timeline.
    -   **noOfBusinessAppsPerTPMPage**: The number of business applications to show per page.

-   **[Enhancements to the My certifications section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/manage-requests-certs-assessments.md)**

    View only the certifications that are relevant to you in the **My certifications** tab on the Enterprise Architecture Workspace home page.


-   **[Enhancements to the Application Portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-application-portfolio.md)**

    Business applications with the Retired state or Lifecycle stage as End of life are no longer displayed in the Business Portfolio section.


## Activation information

Enterprise Architecture \(formerly Application Portfolio Management\) is available with activation of the Enterprise Architecture \(com.snc.apm\), which requires a separate subscription. For details, see [Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/application-portfolio-management-landing-page.md).

Now Assist features are available with activation of the Now Assist for Enterprise Architecture \(EA\) plugin. For more information, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

## Accessibility information

-   Navigate the interface using the keyboard on the Enterprise Modeling and Visualization pages.
-   Access the shape context menu using the keyboard on the Enterprise Modeling and Visualization canvas. On navigating to a particular shape context menu button, the selected button gets highlighted.
-   See pop-over menus when hovering over connector lines on the Enterprise Modeling and Visualization canvas.
-   Reflow- The Enterprise Architecture Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.


## Related ServiceNow applications and Features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)**

    The Now Assist Admin console provides you with quick and effortless access to the important information that you must set up, configure, and monitor in Now Assist applications and features.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use the Now Assist panel to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills.md)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including content summarization in docs.


**Parent Topic:**[Enterprise Architecture release notes](enterprise-architecture-rn-landing.md)

