---
title: Combined Enterprise Architecture release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Enterprise Architecture from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-enterprisearchitecture-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 27
breadcrumb: [Products combined by family]
---

# Combined Enterprise Architecture release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Enterprise Architecture from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Enterprise Architecture release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Enterprise Architecture to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Enterprise Architecture.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[New business architecture entities](https://www.servicenow.com/docs/access?context=eaw-using-business-architecture&family=australia&ft:locale=en-US)**

Model additional layers of your business architecture using five new entity types in the Business Architecture section of the Portfolio List view:

    -   [Business actors](https://www.servicenow.com/docs/access?context=eaw-business-actors&family=australia&ft:locale=en-US) represent the people, teams, or organizational units that perform business processes and activities.
    -   [Business roles](https://www.servicenow.com/docs/access?context=eaw-business-roles&family=australia&ft:locale=en-US) represent the responsibilities, rights, and duties associated with performing specific business behavior, independently of who holds the role. Business roles can have a parent role, letting you build a role hierarchy.
    -   [Stakeholders](https://www.servicenow.com/docs/access?context=eaw-stakeholders&family=australia&ft:locale=en-US) represent the individuals or teams with an interest in your enterprise architecture outcomes, rated by influence and interest level.
    -   [Drivers](https://www.servicenow.com/docs/access?context=eaw-drivers&family=australia&ft:locale=en-US) represent the internal or external conditions that motivate your organization to define goals and implement changes, rated by urgency.
    -   [Business process activities](https://www.servicenow.com/docs/access?context=eaw-business-process-activities&family=australia&ft:locale=en-US) represent discrete units of work, such as a manual task, an approval step, or a system-triggered action, associated with the business actors who perform them.
You can create, edit, and associate each entity with related business actors, roles, stakeholders, drivers, goals, value streams, and business processes from the Portfolio List view.

-   **[Connections between business architecture entities](https://www.servicenow.com/docs/access?context=portfolio-list-view&family=australia&ft:locale=en-US)**

Associate related records between existing and new business architecture entities directly from their related lists in the Portfolio page of Enterprise Architecture Workspace:

    -   Add or remove business capabilities on a business unit.
    -   Add or remove business units on a business capability.
    -   Add or remove business processes on a business unit.
    -   Add or remove business units on a business process.
    -   Add or remove business processes on a goal.
    -   Add or remove goals on a business process.
    -   Add or remove business capabilities on a goal.
    -   Add or remove goals on a business capability.
You can also create related record directly from the related list instead of searching for an existing one.

-   **[Exploring Enterprise Architecture query agent](https://www.servicenow.com/docs/access?context=ea-qna-overview&family=australia&ft:locale=en-US)**

When an Enterprise Architecture query agent response references a specific record, such as a business application or a capability, the record name now appears as linked text. Select the linked text to navigate directly to that record in Enterprise Architecture Workspace.


 -   **[Now Assist for Enterprise Architecture \(EA\) enhancements](https://www.servicenow.com/docs/access?context=now-assist-ea&family=australia&ft:locale=en-US)**

Added support for third-party LLM models: GPT-5.4 mini and Gemini 3.5 Flash


 -   **[Enterprise Modeling and Visualization enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-ent-model-and-visual&family=australia&ft:locale=en-US)**
    -   Align and distribute shapes in a modeling diagram:
        -   Align two or more selected shapes using the alignment options on the diagram toolbar \(**Align left**, **Align center horizontally**, **Align right**\) or the **More alignment options** menu \(**Align top**, **Align center vertically**, **Align bottom**\).
        -   Distribute three or more selected shapes at equal horizontal or vertical spacing using the **Distribute horizontally** and **Distribute vertically** options.

For information, see [Align and distribute shapes in a modeling diagram](https://www.servicenow.com/docs/access?context=eaw-align-distribute-shapes&family=australia&ft:locale=en-US).

    -   Shape preview popover in the **Shapes** panel: When you hover over a shape icon in the **Shapes** panel, a preview popover appears to the right of the panel showing a larger view of the shape and its label.
    -   Bi-directional connector ports across shape libraries: Connector ports on the following shape libraries are bi-directional. You can use any connector port—top, bottom, left, or right—as either an input or an output when connecting shapes in a diagram:
        -   ArchiMate shapes
        -   AWS shapes, including AWS Group shapes
        -   CSDM shapes
        -   EA Extended shapes
    -   Add specific related records to a shape: When adding related records to a shape in a modeling diagram, expand the upstream or downstream entity types to view their individual records, and select only the specific records you want to add to the diagram. For information, see [Add related records in the modeling diagram](https://www.servicenow.com/docs/access?context=eaw-modeling-add-related-records&family=australia&ft:locale=en-US).
    -   Shape connector properties: Configure the connector between two shapes in a modeling diagram by using the connector toolbar. The toolbar shows different controls depending on the notation of the connected shapes:

        -   For ArchiMate connectors \(both shapes are ArchiMate\), use the **Relationship type** drop-down to select an ArchiMate 3.2 relationship. The drop-down now includes **Access** \(with single-direction, bidirectional, and unspecified variants\), **Serving**, **Association**, and **Triggering**. **Influence** is now available in the drop-down \(previously a shape in the ArchiMate shape library\) and displays a +/- adornment on the connector to indicate the direction of influence. The **Assignment** arrow icon is corrected to match the ArchiMate 3.2 specification.
        -   For non-ArchiMate and mixed connectors \(at least one shape is non-ArchiMate\), set the **Line style** \(solid, dashed, or dotted\), **Start arrow** and **End arrow** styles, and **Icon** \(BPMN message flow decorator\).
        -   For any connector, add a text label by using the **T+** control.
For information, see [Shape connector properties in Enterprise Modeling and Visualization](https://www.servicenow.com/docs/access?context=eaw-connector-properties&family=australia&ft:locale=en-US) and [Set shape connector properties](https://www.servicenow.com/docs/access?context=eaw-set-connector-properties&family=australia&ft:locale=en-US).

    -   The width of the right side panel on the modeling diagram canvas is saved as a user preference and persists across sessions.
    -   Group shapes stay anchored when child shapes are added: Dropping a child shape into an EA group shape no longer shifts the group's position on the canvas. The group stays at its current position and resizes its bounds to accommodate the new child shape.
    -   Replace an existing shape or entity in a modeling diagram with a different shape type. Existing connections and relationship lines associated with the shape are preserved after the replacement. For information, see [Replace a shape in a diagram](https://www.servicenow.com/docs/access?context=eaw-modeling-replace-shape&family=australia&ft:locale=en-US).
    -   Upload an image of an existing process diagram to generate a new, editable business process map \(BPM\) diagram in Enterprise Modeling and Visualization, using the ServiceNow AI Lens Now Assist skill. AI Lens identifies shapes, pools, lanes, gateways, and connections from the image, maps recognized shapes to existing records where matching records exist, and stages new records for shapes with no match.

The generated diagram opens in review state on a split canvas: the upper pane displays the generated diagram and the lower pane displays the source image for reference. Shapes identified with a confidence score below 50% are marked with an orange border on the canvas and listed in the Shapes with low confidence scores drop-down in the canvas banner. For information, see [Create business process map diagram from image using ServiceNow Otto](https://www.servicenow.com/docs/access?context=eaw-create-bpm-diag-from-image&family=australia&ft:locale=en-US) and [Review ServiceNow Otto generated business process map diagram](https://www.servicenow.com/docs/access?context=eaw-review-ai-generated-bpm-diag&family=australia&ft:locale=en-US)

-   **[Sync TRM product names with software product names](https://www.servicenow.com/docs/access?context=eaw-schedule-job-sync-trm-product-names&family=australia&ft:locale=en-US)**

Run the **Sync TRM Product Names with Software Products** scheduled job to update TRM product names in EA Workspace with the latest names of their linked software products.

-   **[BPMN 2.0 shape library enhancements](https://www.servicenow.com/docs/access?context=eaw-modeling-bpmn-shapes&family=australia&ft:locale=en-US)**

The BPMN shape library in the Enterprise Modeling and Visualization is expanded with shapes conforming to the BPMN 2.0 standard:

    -   Event shapes: The library now includes all standard BPMN 2.0 event types organized into start, non-interrupting start, intermediate catching, intermediate throwing, end, and boundary events, with trigger configurations for message, timer, conditional, signal, escalation, compensation, error, cancel, link, and terminate.
    -   Gateway shapes: Expanded to include event-based, instantiating, and complex gateway types. Gateway shapes can be resized on the canvas.
    -   Activity shapes: Expanded to include eight task types \(task, user task, service task, manual task, script task, business rule task, send task, and receive task\) and call activity shapes. Four existing shape names are updated to align with the BPMN 2.0 standard: Default → Task, System → Service task, User → User task, Manual → Manual task.
BPMN shapes in the **Shapes** panel are organized into four sub-categories: **Event**, **Activity**, **Gateway**, and **General**. When you drag a shape from the panel onto the canvas, the shape displays its actual icon while dragging.ArchiMate Technology layer shape names are updated to match the ArchiMate 3.2 specification: Infrastructure Function → Technology Function, Communication Path → Path, Infrastructure Interface → Technology Interface. The Network Box and Network shapes, which aren't part of the ArchiMate 3.2 standard, are removed.

-   **[AI Portfolio tab on the Enterprise Architecture Workspace dashboard](https://www.servicenow.com/docs/access?context=eaw-exploring-the-ai-portfolio&family=australia&ft:locale=en-US)**

Monitor AI adoption across your enterprise from the **AI Portfolio** tab on the Enterprise Architecture Workspace dashboard. The tab is available when the AI Control Tower workspace is installed and displays two widgets:

    -   **Business Applications by AI System Association**: Shows the total number of business applications, segmented by whether they are linked to an AI system.
    -   **AI Systems by Business Application Association**: Shows the total number of AI systems, segmented by whether they are linked to a business application.
Both widgets source their data from approved AI System–Business Application linkage records. For information, see [Exploring the AI Portfolio](https://www.servicenow.com/docs/access?context=eaw-exploring-the-ai-portfolio&family=australia&ft:locale=en-US).

-   **[Exploring Enterprise Architecture query agent](https://www.servicenow.com/docs/access?context=ea-qna-overview&family=australia&ft:locale=en-US)**

The Enterprise Architecture query agent is a new Now Assist agentic AI skill that lets you ask natural language questions about your enterprise architecture portfolio directly from EA Workspace.

Use the agent to retrieve and analyze information across business applications, business capabilities, value streams, TRM standards, and information objects. It supports multi-condition queries, trend comparisons, and impact analysis. After answering, the agent suggests related questions to help you explore further.

-   **[Exploring the AI Portfolio tab on the Enterprise Architecture Workspace dashboard](https://www.servicenow.com/docs/access?context=eaw-dashboard-exploring-ai-portfolio-tab&family=australia&ft:locale=en-US)**

Monitor AI adoption across your enterprise from the AI Portfolio tab on the EA Workspace dashboard. The tab is available when the AI Control Tower workspace is installed and displays two widgets: Business Applications by AI System Association and AI Systems by Business Application Association.


 -   **[AI systems on business applications](https://www.servicenow.com/docs/access?context=eaw-aict&family=australia&ft:locale=en-US)**

View and manage AI systems associated with a business application from the **AI Systems** tab on a business application record in the Enterprise Architecture Workspace.

    -   View all AI systems linked to a business application, organized by governance status as **Managed** \(submitted for AI Steward review\) or **Unmanaged** \(created but not yet submitted for review\).
    -   Add an existing AI system to a business application record.
    -   Remove an AI system association from a business application record without deleting the AI system record in AI Control Tower.
    -   Open the full AI system record in AI Control Tower directly from the **AI Systems** tab of a business application record in Enterprise Architecture Workspace, to review governance details, lifecycle status, and related assets.
Associate a business application with a new AI use case at intake using the **Business Applications** field on the **Request an AI use case** catalog item in the service portal. The association is established on submission, and the AI system appears as unmanaged on the corresponding business application records in the Enterprise Architecture Workspace.

-   **[AI Search on the TRM catalog](https://www.servicenow.com/docs/access?context=ai-search-trm-cat&family=australia&ft:locale=en-US)**

Search published TRM catalog records using natural language queries in the Now Assist panel. EA Workspace ships default AI Search configuration that automatically indexes TRM catalog records you publish. To make previously published TRM catalog records searchable, you can manually trigger indexing. For information, see [Index previously published TRM catalog records for AI Search](https://www.servicenow.com/docs/access?context=index-archive-pub-trm-cat&family=australia&ft:locale=en-US) or [AI Search on the TRM catalog](https://www.servicenow.com/docs/access?context=ai-search-trm-cat&family=australia&ft:locale=en-US).


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   **[Enterprise Modeling and Visualization enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-ent-model-and-visual&family=australia&ft:locale=en-US)**

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
-   **[Exploring the publishing center in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=publishing-center-in-ea-workspace&family=australia&ft:locale=en-US)**

Use the Publishing Center to control publishing workflows, monitor status, and view publishing history from a single location.

-   **[Publish TRM catalog to a knowledge base](https://www.servicenow.com/docs/access?context=working-with-publishing-center&family=australia&ft:locale=en-US)**
    -   Configure TRM catalogs and apply filters for products and lifecycle phases.
    -   Manage publishing workflows with status updates from Draft to Published.
    -   View publishing job history in the Run logs tab.
    -   Access the published TRM catalog using the generated knowledge base URL.
-   **Enhancements to the [Value stream](https://www.servicenow.com/docs/access?context=eaw-manage-value-streams&family=australia&ft:locale=en-US) and [Value stream stage](https://www.servicenow.com/docs/access?context=eaw-manage-value-stream-stages&family=australia&ft:locale=en-US) related lists**
    -   Value stream: View associated value stream stages and application models as related lists. You can add, edit, or remove the associated value stream stages and application models.
    -   Value stream stage: View associated business processes and business capabilities. Add or remove business processes and business capabilities. You can also view the value stream stage as a related list in the business process and business capability records.
-   **[Enhancements to the Business Process related lists](https://www.servicenow.com/docs/access?context=eaw-manage-business-processes&family=australia&ft:locale=en-US)**

View the value stream stage as a related list of a business process.

-   **[Enhancements to the Business Capability related lists](https://www.servicenow.com/docs/access?context=eaw-manage-business-capabilities&family=australia&ft:locale=en-US)**

View the value stream stage as a related list of a business capability.

-   **[Create documents for the Enterprise Modeling and Visualization diagrams](https://www.servicenow.com/docs/access?context=create-documents-for-diagrams&family=australia&ft:locale=en-US)**
    -   Save diagram as a document using the Generate document option from the Enterprise Modeling and Visualization diagrams page.
    -   Define templates for the documents that can be created and used from the Diagrams page.
    -   Tag components that can be included in the templates to generate documents.
    -   View associated documents from the Diagrams page.
-   **[Exploring the architecture analyzer](https://www.servicenow.com/docs/access?context=eaw-explore-arch-analyzer&family=australia&ft:locale=en-US)Architecture Analyzer**
    -   The Architectural Analyzer helps you to analyze architecture data without creating or maintaining custom diagrams. You can visually explore relationships across applications, services, and infrastructure to quickly understand dependencies and collaborate on architecture decisions. You can also understand the potential impact of architectural changes across applications and services.
-   **[Application rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&family=australia&ft:locale=en-US)**

Added an Overall score indicator to show the overall average score of a business application. Use this indicator to determine the bubble size of a business application on the Bubble Chart page. You can compare the overall scores of different business applications using their individual bubble sizes.

-   **[Business application summarization skill enhancements](https://www.servicenow.com/docs/access?context=generate-insights-into-ba&family=australia&ft:locale=en-US)**

Generate context-sensitive business application summaries from the following pages:

    -   Business capability hierarchy page: On generating a business application summary from this page, information such as the associated primary and secondary capabilities and the position in the capability hierarchy are displayed along with the general information about the business application.
    -   Application rationalization list view page: On generating a business application summary from this page, information such as the indicator scores \(actual and normalized scores\), and associated demand details are displayed along with the general information about the business application.
    -   Application rationalization bubble chart page: On generating a business application summary from this page, information such as x and y-axis details, and planned disposition details are displayed along with the general information about the business application.
-   **[Generate insights for Enterprise Architecture Workspace dashboard widgets](https://www.servicenow.com/docs/access?context=generate-insights-ea-dashboard&family=australia&ft:locale=en-US)Now Assist**

Generate insights for the widgets available on the Enterprise Architecture Dashboard page using the Now Assist Explorer icon available on the header of each widget.

-   **[Diagram change analysis skill enhancements](https://www.servicenow.com/docs/access?context=compare-modeling-diagrams&family=australia&ft:locale=en-US)**
    -   Compare any two versions of a diagram and generate a summary of the changes.
    -   Select any version as a primary or secondary version to compare.
    -   Generate a summary for real-time changes made to the primary version while already comparing it to another diagram version.
    -   Modify diagram versions to compare using the Diagram comparison icon on the diagram comparison page.
    -   Identify differences faster when comparing two versions of a diagram, by using the color-coded highlights on the canvas. Newly added shapes and relationship lines appear in green and modified ones appear in yellow.

 -   **[Exploring the architecture analyzer](https://www.servicenow.com/docs/access?context=eaw-explore-arch-analyzer&family=australia&ft:locale=en-US)Architecture Analyzer**
    -   Added support for analyzing all EA extended entities that are part of Enterprise Modeling and Visualization, such as
        -   Control
        -   Digital integration
        -   Digital interface
        -   GRC risk
        -   Product capability
        -   TRM product
    -   The **Clear** button clears all the selections made in the **Add to canvas** boxes.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Enterprise Architecture features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Added **Business Actors**, **Business Roles**, **Stakeholders**, **Drivers**, and **Business Process Activities** options to the **Business Architecture** section of the Portfolio List view.
-   Added the **Related business capabilities** and **Related business processes** tabs to business unit records page.
-   Added the **Business capabilities** and **Business processes** tabs to goal records page.
-   Updated Now Assist icons and text across the Enterprise Architecture Workspace to ServiceNow Otto branding.
-   Record names referenced in Enterprise Architecture query agent responses now appear as selectable linked text.

 -   **[Renamed Technology Portfolio Management](https://www.servicenow.com/docs/access?context=eaw-tpm&family=australia&ft:locale=en-US)**

Technology Portfolio Management \(TPM\) is renamed Technology Lifecycle Management \(TLM\) in the Enterprise Architecture Workspace.

-   **[Renamed Now Assist](https://www.servicenow.com/docs/access?context=exploring-now-assist-for-ea&family=australia&ft:locale=en-US)**

ServiceNow Otto for Enterprise Architecture \(EA\) is rebranded to ServiceNow Otto. User-facing text and icons across the Enterprise Modeling and Visualization tool are updated to reflect the new branding.


 -   **[ServiceNow Otto for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&family=australia&ft:locale=en-US)**
    -   The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.
    -   Changed the default LLM model for all ServiceNow Otto for Enterprise Architecture \(EA\) is to Azure OpenAI.

 -   Added the alignment options \(**Align left**, **Align center horizontally**, **Align right**\) to the toolbar on the modeling diagram canvas page. The **More alignment options** menu was added to access **Align top**, **Align center vertically**, **Align bottom**, **Distribute horizontally**, and **Distribute vertically** options.
-   Added a preview popover that appears to the right of the **Shapes** panel when you hover over a shape icon with the mouse or focus on it with the arrow keys.
-   Added the connector toolbar in modeling diagrams to show different controls depending on the notation of the connected shapes. For ArchiMate connectors, the toolbar provides the **Relationship type** drop-down, **Swap direction**, and **T+**. For non-ArchiMate and mixed connectors, the toolbar provides **Line style**, **Start arrow**, **Swap direction**, **End arrow**, **Icon**, and **T+** controls.
-   Added **Access**, **Serving**, **Association**, and **Triggering** entries to the **Relationship type** drop-down on the ArchiMate connector toolbar.
-   The width of the right side panel on the modeling diagram canvas is saved as a user preference and persists across sessions.
-   Added the **Import image** icon on the Enterprise Modeling and Visualization homepage.
-   Added the Now Assist icon in the navigation bar and the **Ask Now Assist** button on the Enterprise Architecture Workspace homepage.
-   Added the **AI Portfolio** tab to the Enterprise Architecture Workspace dashboard. The tab includes the **Business Applications by AI System Association** and **AI Systems by Business Application Association** widgets. The tab is visible when the AI Control Tower workspace is installed.

 -   Added the **AI Systems** tab to business application records in the Enterprise Architecture Workspace. The tab displays **Managed** and **Unmanaged** sections, each listing associated AI systems.
-   Added the **Business Applications** field to the **Request an AI use case** catalog item in the service portal. The field is available only when the Enterprise Architecture application is installed and business applications are configured. You can select multiple business applications. Retired business applications aren't available for selection.
-   Added a read-only **Business applications** related list under **Related assets** on AI system records in AI Control Tower. This list shows the business applications associated with each AI system.

 -   The diagram comparison canvas displays visual indicators to highlight new or modified shapes and entities. Newly added shapes and relationship lines appear in green and modified ones appear in yellow.

 -   Generate document
-   View all documents

 -   Added the Publishing center section in the Setup page.
-   Changed the label of Publisher to Company in the TRM page.
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

 -   **[Enhancements to the My certifications section](https://www.servicenow.com/docs/access?context=manage-requests-certs-assessments&family=australia&ft:locale=en-US)**

View only the certifications that are relevant to you in the **My certifications** tab on the Enterprise Architecture Workspace home page.


 -   **[Enhancements to the Application Portfolio](https://www.servicenow.com/docs/access?context=eaw-work-with-application-portfolio&family=australia&ft:locale=en-US)**

Business applications with the Retired state or Lifecycle stage as End of life are no longer displayed in the Business Portfolio section.


 Australia Early Availability

 -   **[Granular admin role changes in Enterprise Architecture](https://www.servicenow.com/docs/access?context=eaw-gran-admin-role-changes&family=australia&ft:locale=en-US)**

Added the granular level admin role \(sn\_apm.apm\_admin\) to the following system properties in the Enterprise Architecture:

    -   **sn\_apm\_trm.is\_product\_life\_cycle\_tech\_debt\_enabled**: Make this property false to disable calculating level 2 technical debt.
    -   **glide.ui.sn\_apm\_trm\_product\_request\_activity.fields**: TRM Product Request activity formatter fields.
    -   **sn\_apm\_trm.noOfPublishersPerTRMPage**: The number of publishers to show per page.
    -   **glide.ui.sn\_apm\_trm\_product\_lifecycle\_request\_activity.fields**: TRM Product Lifecycle Request activity formatter fields.
    -   **sn\_apm.noOfSoftwareModelsPerTPMPage**: The number of software models to show per page. This property is used for client-side pagination.
    -   **sn\_apm.discoveryModelProductTypesForTPMSuggestions**: Product types of discovery models to consider for TPM software suggestions.
    -   **sn\_apm.noOfSDLCComponentPerTPMPage**: The number of Agile Development components to show per page.
    -   **glide.ui.cmdb\_ci\_business\_app\_activity.fields**: Business application activity formatter fields.
    -   **sn\_apm.startRangeOfTPMLifecycle**: The number of years before the current date is included when displaying software model lifecycle phases in the TLM timeline.
    -   **sn\_apm.endRangeOfTPMLifecycle**: The number of years beyond the current date is included when displaying software model lifecycle phases in the TLM timeline.
    -   **noOfBusinessAppsPerTPMPage**: The number of business applications to show per page.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Enterprise Architecture features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Enterprise Architecture features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Enterprise Architecture.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Enterprise Architecture \(formerly Application Portfolio Management\) is available with activation of the Enterprise Architecture \(com.snc.apm\), which requires a separate subscription. For details, see [Enterprise Architecture](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&family=australia&ft:locale=en-US).

Now Assist features are available with activation of the ServiceNow Otto for Enterprise Architecture \(EA\) plugin. For more information, see [Install plugins for ServiceNow Otto](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Enterprise Architecture is available with activation of the Enterprise Architecture \(com.snc.apm\) plugin, which requires a separate subscription.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Enterprise Architecture we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Additional requirements**

ServiceNow Otto features are available with activation of the ServiceNow Otto for Enterprise Architecture \(EA\) plugin. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Enterprise Architecture we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Enterprise Architecture, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Accessibility information**
    -   Navigate the interface using the keyboard on the Enterprise Modeling and Visualization pages.
    -   Access the shape context menu using the keyboard on the Enterprise Modeling and Visualization canvas. On navigating to a particular shape context menu button, the selected button gets highlighted.
    -   See pop-over menus when hovering over connector lines on the Enterprise Modeling and Visualization canvas.
    -   Keep connector ports visible on all shapes in the diagram canvas without hovering by enabling the **Show all buttons without the need to hover** option in **Preferences** &gt; **Accessibility**. When enabled, connector ports remain visible at all times on General, ArchiMate®, AWS, CSDM, and Group shapes. For more information, see [Show shape controls without hovering](https://www.servicenow.com/docs/access?context=eaw-show-shape-ports&family=australia&ft:locale=en-US).
    -   Reflow- The Enterprise Architecture Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Enterprise Architecture we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Enterprise Architecture we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   Model your business architecture using five new entities in the Business Architecture section: Business Actor, Business Role, Stakeholder, Driver, and Business Process Activity.
-   Technology Portfolio Management \(TPM\) is renamed Technology Lifecycle Management \(TLM\) in the Enterprise Architecture Workspace. Table and scheduled job names continue to use TPM.
-   Select a linked record name in an Enterprise Architecture query agent response to navigate directly to that record in Enterprise Architecture Workspace.
-   ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

 [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)

-   Support added for third-party AI models: GPT-5.4 mini and Gemini 3.5 Flash
-   Third-party AI models are the default models for all ServiceNow Otto for EA skills.
-   The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Align two or more shapes to a common edge or center, and distribute three or more shapes at equal spacing on the modeling diagram canvas.
-   Preview shapes in the **Shapes** panel by hovering over a shape icon or using arrow keys to see a larger view and label.
-   Connect shapes from any direction by using bi-directional connector ports on ArchiMate, AWS, CSDM, and EA Extended shape libraries.
-   Add specific records of upstream or downstream entities to a shape in a modeling diagram instead of all records of an entity type.
-   Run a scheduled job to sync TRM product names in EA Workspace with the latest names of their linked software products.
-   Configure shape connector properties from the connector toolbar in a modeling diagram.
-   Replace an existing shape or entity in a modeling diagram with a different shape type while preserving existing connections.
-   Generate a business process map \(BPM\) diagram from an uploaded image of an existing process diagram.
-   Monitor AI adoption across your enterprise from the AI Portfolio tab on the EA Workspace dashboard.
-   Use an expanded BPMN 2.0 shape library in the Enterprise Modeling and Visualization with new event shapes, additional gateway types, and expanded activity shapes. BPMN shapes are organized into sub-categories in the **Shapes** panel.
-   Use the Enterprise Architecture query agent to ask natural language questions about your enterprise architecture portfolio directly from Enterprise Architecture Workspace.

 [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

-   Associate AI systems from AI Control Tower with business applications in the Enterprise Architecture Workspace to track AI adoption, governance status, and business context across your application portfolio. You can also associate one or more business applications when submitting an AI use case request in the Service Portal.
-   You can use the Now Assist panel to search your published TRM catalog records using natural language queries.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

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

 See [Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=ea-workspace&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Unite strategic and operational teams around a single enterprise architecture practice for managing business capabilities, application portfolios, information portfolios, and technology portfolios.
-   Decide whether to invest in, sustain, or replace business applications based on business need and organizational goals, using indicators such as cost, risk, value, and technical debt.
-   Model, visualize, and analyze your architecture using industry-aligned standards such as CSDM, ArchiMate, and AWS, and explore relationships and dependencies using Architecture Analyzer.
-   Work from a single Enterprise Architecture Workspace home page with role-based views for enterprise architects, administrators, and analysts, including portfolio insights, tasks that need your attention, and portfolio health.
-   Ensure the accuracy, completeness, and reliability of enterprise architecture data with configurable Data Certification policies.

 See [Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=ea-workspace&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

