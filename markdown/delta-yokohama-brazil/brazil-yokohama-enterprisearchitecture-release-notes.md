---
title: Combined Enterprise Architecture release notes for upgrades from Yokohama to Brazil
description: Consolidated page of all release notes for Enterprise Architecture from Yokohama to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-brazil/brazil-yokohama-enterprisearchitecture-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 49
breadcrumb: [Products combined by family]
---

# Combined Enterprise Architecture release notes for upgrades from Yokohama to Brazil

Consolidated page of all release notes for Enterprise Architecture from Yokohama to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Enterprise Architecture release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Enterprise Architecture to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

-   **Yokohama Patch 6 [Application rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&family=yokohama&ft:locale=en-US)**
    -   Apply the fiscal period filter to filter and view business applications for a specific fiscal period.
    -   Apply the application rationalization filters to filter and view specific business applications on the bubble chart or list view page. An indicator is displayed on top of the filter icon to show the number of filters currently applied.
    -   View the business application technical debt indicator score on the application rationalization list view page. On the application rationalization bubble chart view page, you can use the TRM technical debt indicator to form the bubble size based on the indicator score.
    -   Export the list view of application rationalization data to Excel or CSV file format. You can use the data to obtain insights, share with stakeholders, and prepare for analysis.
    -   Business applications with Retired or End of Life lifecycle stage aren’t displayed on the Application Rationalization bubble chart page.

 -   **[Business application related list enhancements](https://www.servicenow.com/docs/access?context=eaw-app-portfolio&family=yokohama&ft:locale=en-US)**

In the **Architectural Artifacts** tab of the business application related list, selecting the **New** button displays a modal to create an architectural artifact.

-   **[Architectural Decision Records \(ADR\) enhancements](https://www.servicenow.com/docs/access?context=eaw-managing-arch-decision-records&family=yokohama&ft:locale=en-US)**
    -   Create artifact type Architectural Decision Records \(ADR\) in one step.
    -   Create and add multiple pages to the Architectural Decision Records \(ADR\) from the Artifact content tab.
    -   In the Architectural Decision Records \(ADR\) page, you can tag the following:
        -   Tag a user
        -   Tag a record
            -   Architectural artifact
            -   Business application
            -   Business capability
            -   Business process
            -   Digital integration \(requires the digital integration plugin\)
            -   Digital interface \(requires the digital integration plugin\)
            -   Information object
            -   TRM product \(requires the TRM plugin\)
            -   Value stream \(requires the value stream plugin\)
    -   Request approval workflow for Architectural Decision Records \(ADR\).
    -   The version drop-down list is added to the Architectural Decision Records \(ADR\) page header. Select a version from the drop-down list to open the specific ADR version.
-   **[Data Certification changes](https://www.servicenow.com/docs/access?context=eaw-config-cert-schedules&family=yokohama&ft:locale=en-US)**

In the Enterprise Architecture Workspace, the certifications data is saved to and fetched from the CMDB Data Management Task Control \(cmdb\_data\_management\_task\) table.If your certification data is still fetched from the Certification Schedules \(cert\_schedule\) table, you might consider migrating your certification policies to the CMDB Data Management Task Control \(cmdb\_data\_management\_task\) table. For more information, see [Convert legacy certification schedules into Data Manager Certification policies](https://www.servicenow.com/docs/access?context=convert-data-cert-definitions&family=yokohama&ft:locale=en-US)and[Publish a draft Data Manager policy in CMDB Workspace](https://www.servicenow.com/docs/access?context=data-manager-publish-draft-policy&family=yokohama&ft:locale=en-US)


 -   **[Regenerate indicator scores in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-regenerate-indicator-score&family=yokohama&ft:locale=en-US)**

Generate a score for application and capability indicators for a particular period. Also, generate scores for an application scoring profile and capability scoring profile, to calculate scores for all indicators attached to that particular scoring profile.

-   **[Business stakeholder role for Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-business-stakeholder-role&family=yokohama&ft:locale=en-US)**

Read-only access to the  Enterprise Architecture Workspace is added to the business stakeholder role \(sn\_apm.apm\_read\).

-   **[TRM technical debt form](https://www.servicenow.com/docs/access?context=eaw-trm-technical-debt-form&family=yokohama&ft:locale=en-US)**

The **TPM Discovered Technologies and Lifecycles** scheduled job fetches the server details for the TRM products.


 -   **[Enterprise Modeling and Visualization in the EA Workspace](https://www.servicenow.com/docs/access?context=eaw-modeling&family=yokohama&ft:locale=en-US)**
    -   Create diagrams for business process maps using the specific shapes related to the business processes.
    -   Search shapes within the shape libraries.
    -   Reorganize the order of shapes in a shape library according to your requirement.
    -   Show or hide shapes in different diagram types.
    -   General shapes can be rotated.
    -   Enhanced the overall appearance of the diagram by hiding the connector ports and displaying them only when hovering over the shapes.
    -   Open the Enterprise Modeling and Visualization diagrams from the following sections:
        -   From the Architectural Artifacts related list of a business application, business capability, or a business process record.
        -   From the My approvals tab of the Needs Attention section on the EA Workspace home page.
        -   From the Architectural Artifacts section of the Portfolio page.
    -   Added support for all ArchiMate shapes.
    -   Model Value stream diagrams.
    -   Create diagram actions for newly added custom shapes that can be used in Enterprise Modeling and Visualization to create diagrams.
    -   Add custom shapes to use in the Enterprise Modeling and Visualization.
    -   Create your own modeling diagrams using the Blank diagram option.
-   **[Technology portfolio management \(TPM\) enhancements](https://www.servicenow.com/docs/access?context=eaw-tpm&family=yokohama&ft:locale=en-US)**
    -   Added a restart button on the TPM Logs page to restart the Populate TPM Discovered Technologies and Lifecycles scheduled job, in case the job is stuck and doesn’t refresh the log data for more than an hour. For more information, see [View TPM logs](https://www.servicenow.com/docs/access?context=eaw-view-tpm-logs&family=yokohama&ft:locale=en-US) and [Restart scheduled job](https://www.servicenow.com/docs/access?context=eaw-restart-tpm-scheduled-job&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

-   **[Data certification in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-work-with-data-cert&family=zurich&ft:locale=en-US)**
    -   Use the Data Certification workflow in Enterprise Architecture Workspace to ensure the accuracy, completeness, and reliability of critical data within your organization. For details, see [Exploring data certification in the Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-explore-data-cert&family=zurich&ft:locale=en-US).
    -   Create a data certification policy directly from the Enterprise Architecture Workspace using the Data certification workflow. For details, see [Create a certification policy](https://www.servicenow.com/docs/access?context=eaw-create-policy&family=zurich&ft:locale=en-US).
    -   Run certification on demand for published policies to generate a new certification instance for an active policy. For details, see [Run certification for a policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-run-certification&family=zurich&ft:locale=en-US).
    -   Activate a certification policy to add it to the active certification runs. This process ensures that the policy is active and can be used for certifications. You can deactivate a policy to remove it from active certification runs. For details, see [Activate a certification policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-activate&family=zurich&ft:locale=en-US).
-   **[TRM catalog enhancement](https://www.servicenow.com/docs/access?context=eaw-export-trm-prod-cat-data&family=zurich&ft:locale=en-US)**

Export the TRM catalog data to Microsoft Excel or CSV format.

-   **[Business Portfolio enhancement](https://www.servicenow.com/docs/access?context=eaw-export-business-portfolio-data&family=zurich&ft:locale=en-US)**

Export the Business Portfolio data to Microsoft Excel or CSV format.

-   **[TRM category enhancements](https://www.servicenow.com/docs/access?context=eaw-create-new-trm-category&family=zurich&ft:locale=en-US)**

Assign an owner to a TRM category to ensure clear accountability and improved governance standards. The owner is responsible for maintaining consistent technology compliance standards for that TRM category.

-   **[TPM lifecycle record enhancements](https://www.servicenow.com/docs/access?context=eaw-tpm&family=zurich&ft:locale=en-US)**
    -   TLM lifecycle records are now assigned unique identifiers are automatically,while creating the TLM lifecycle record. These identifiers serve as clickable links that provide direct access to full record details.
    -   Run the Populate Number field in TPM Discovered Technologies scheduled job to populate the TPM lifecycle record identifiers of existing records created using previous versions \(before version 1.9.0\) of the TLM plugin. For details, [Run a scheduled job to populate TLM lifecycle record identifier](https://www.servicenow.com/docs/access?context=eaw-run-job-to-populate-tpm-lifecycle-identifier&family=zurich&ft:locale=en-US).
-   **[Working with Portfolio list view](https://www.servicenow.com/docs/access?context=eaw-work-with-portfolio-list-view&family=zurich&ft:locale=en-US)[AI Portfolio section enhancements](https://www.servicenow.com/docs/access?context=eaw-exploring-the-ai-portfolio&family=zurich&ft:locale=en-US)**

The following AI product models added to the AI Portfolio section:

    -   AI System Product Models
    -   AI Model Product Models
    -   AI Dataset Product Models
    -   AI Prompt Product Models

 -   **[Enterprise Architecture Workspace home page enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-ea-workspace-homepage&family=zurich&ft:locale=en-US)**

Apply the Portfolio Overview and Health filters to filter and view specific business applications and business capabilities information. An indicator is displayed on top of the filter icon to show the number of filters currently applied.

-   **[TRM product related list enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-trm&family=zurich&ft:locale=en-US)**
    -   Added the **Product capability** tab as a related list. In the tab, you can:
        -   Select **New** to create a new product capability and associate it with the TRM product.
        -   Select **Add** to add an existing product capability to the TRM product.
        -   Select **Remove** to remove a product capability from a TRM product.
    -   Added the **Business Applications** tab as a related list. In the tab, you can:
        -   Select **New** to create a new business application and associate it with the TRM product.
        -   Select **Add** to add an existing business application to the TRM product.
        -   Select **Remove** to remove a business application from a TRM product.

 -   **[Application rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&family=zurich&ft:locale=en-US)**
    -   View business application bubbles whose X and Y-axis values are within the value range of +/-0.25 of each other as a grouped bubble. The grouped bubble displays the total number of business application bubbles that it contains. This grouping helps in clearing the clutter on bubble chart when there are too many business applications with similar values. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&family=zurich&ft:locale=en-US).
    -   Zoom in, zoom out, or pan on the Bubble chart page using either on-screen buttons or by using a mouse device or trackpad interactions. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&family=zurich&ft:locale=en-US).
    -   View the calculation logic behind the total number of business applications displayed on the Bubble chart page. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&family=zurich&ft:locale=en-US).
    -   Select a single bubble on the Bubble chart page to view the associated business application details. Select a grouped bubble to view the list of business applications that are part of that grouped bubble. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&family=zurich&ft:locale=en-US).
    -   View actual scores of business applications and compare them with their normalized scores. For details, see [List view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-list-view&family=zurich&ft:locale=en-US).
    -   Increased maximum number of bubbles displayed on the Bubble chart to 500.
    -   Apply the fiscal period filter to filter and view business applications for a specific fiscal period.
    -   Apply the application rationalization filters to filter and view specific business applications on the bubble chart or list view page. An indicator is displayed on top of the filter icon to show the number of filters currently applied.
    -   View the business application technical debt indicator score on the application rationalization list view page. On the application rationalization bubble chart view page, you can use the TRM technical debt indicator to form the bubble size based on the indicator score.
    -   Export the list view of application rationalization data to Excel or CSV file format. You can use the data to obtain insights, share with stakeholders, and prepare for analysis.
    -   Business applications with Retired or End of Life lifecycle stage aren’t displayed on the Application Rationalization bubble chart page.

 -   **[Manage Enterprise Modeling and Visualization](https://www.servicenow.com/docs/access?context=eaw-config-modeling&family=zurich&ft:locale=en-US)**
    -   Create a diagrams using CSDM shapes to ensure consistency in how services, applications, and infrastructure are represented. Aligning with CMDB 5 standards, helps you in accurate reporting, impact analysis, and compliance across the enterprise. For details, see [Common Service Data Model \(CSDM\) shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-csdm-shapes&family=zurich&ft:locale=en-US).
    -   Use the modified Enterprise Architecture shapes that are aligned with CSDM 5 standards for better modeling, accurate impact analysis, and reporting. For details, see [Create a diagram using CSDM shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-create-diagram-csdm&family=zurich&ft:locale=en-US).
    -   Create diagrams using AWS shapes. The AWS shapes enable you to visualize AWS cloud components, model hybrid architectures, support cloud migration planning. For details, see [Amazon Web Services \(AWS\) shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-aws-shapes&family=zurich&ft:locale=en-US) and [Create a diagram using AWS shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-create-diagram-aws&family=zurich&ft:locale=en-US).
    -   Group or ungroup a general shape object. You can combine multiple related shapes into a single container for better organization and clarity in diagrams. For details, see [Convert a shape to a group shape](https://www.servicenow.com/docs/access?context=eaw-modeling-group-ungroup-shape&family=zurich&ft:locale=en-US).
    -   Expand or collapse a group shape to simplify visualization, improve focus, and supports hierarchical modeling. For details, see [Expand or collapse a group shape](https://www.servicenow.com/docs/access?context=eaw-modeling-expand-collapse-shape&family=zurich&ft:locale=en-US).
    -   View Business Process details for which the BPMN diagram is being created. Modify details such as name, parent, and description. For details, see [Modify BPMN diagram details](https://www.servicenow.com/docs/access?context=eaw-modeling-modify-bpmn&family=zurich&ft:locale=en-US).
    -   Reorder shape categories within the Shapes panel to customize the panel for faster access to frequently used shapes. For details, see [Reorder shapes categories](https://www.servicenow.com/docs/access?context=eaw-modeling-reorder-shapes-cat&family=zurich&ft:locale=en-US).
    -   Show or hide the Shapes panel to optimize your workspace for different tasks. For details, see [Show or hide shapes panel](https://www.servicenow.com/docs/access?context=eaw-modeling-show-hide-shapes-panel&family=zurich&ft:locale=en-US).
    -   Switch between List view and Grid view in the shapes panel according to your modeling needs. For details, see [Switch to list or grid view of shapes panel](https://www.servicenow.com/docs/access?context=eaw-modeling-shapes-grid-list-view&family=zurich&ft:locale=en-US).
    -   Download a diagram as an image to share it with other stakeholders with offline access or use it in the presentations. For details, see [Download a modeling diagram as an image](https://www.servicenow.com/docs/access?context=eaw-modeling-download-diagram&family=zurich&ft:locale=en-US).
    -   Select and delete diagrams from the Diagrams page.
    -   Select upstream or downstream entities when adding related records for shapes. The upstream entities appear as a parent for the selected shape in the diagram while the downstream entities appear as a child for the selected shape in the diagram.
    -   Add version label, version description, and planned rollout date details for diagram versions.
    -   On duplicating a business process map, you can choose to associate the duplicated process map with a new or an existing business process.
    -   Added support for shapes that enable AI governance. The shapes are added under the Enterprise Architecture category in the shapes palette. The shapes are:
        -   AI Dataset Digital Asset
        -   AI Model Digital Asset
        -   AI Prompt Digital Asset
        -   AI System Digital Asset
    -   Perform undo and redo actions using buttons on the diagram page or using keyboard shortcuts.
    -   Resize the shapes added to a canvas.
    -   Drag shapes from the **Shapes** palette on to the canvas.
    -   Add labels on the connector lines between shapes in a diagram.
    -   Create diagrams for business process maps using the specific shapes related to the business processes.
    -   Search shapes within the shape libraries.
    -   Reorganize the order of shapes in a shape library according to your requirement.
    -   Show or hide shapes in different diagram types.
    -   General shapes can be rotated.
    -   Enhanced the overall appearance of the diagram by hiding the connector ports and displaying them only when hovering over the shapes.
    -   Open the Enterprise Modeling and Visualization diagrams from the following sections:
        -   From the Architectural Artifacts related list of a business application, business capability, or a business process record.
        -   From the **My approvals** tab of the Needs Attention section on the EA Workspace home page.
        -   From the Architectural Artifacts section of the Portfolio page.
    -   Added support for all ArchiMate shapes.
    -   Model Value stream diagrams.
-   **[Business application related list enhancements](https://www.servicenow.com/docs/access?context=eaw-app-portfolio&family=zurich&ft:locale=en-US)**

Added the AI Product Models as a related list. In the tab, you can:

    -   Select **Add** to associate an existing AI system product model to the business application.
    -   Select **Remove** to remove a AI system product model from a business application.
For details, see [Add AI systems to business applications](https://www.servicenow.com/docs/access?context=eaw-add-ai-systems&family=zurich&ft:locale=en-US).

    -   Added the **Product capability** tab as a related list. In the tab, you can:
        -   Select **New** to create a new product capability and associate it with the business application.
        -   Select **Add** to add an existing product capability to the business application.
        -   Select **Remove** to remove a product capability from a business application.
    -   Added the TRM products tab as a related list. In the tab, you can:
        -   Select **New** to create a new TRM product and associate it with the business application.
        -   Select **Add** to add an existing TRM product to the business application.
        -   Select **Remove** to remove a TRM product from a business application.
    -   In the **Architectural Artifacts** tab of the business application related list, selecting the **New** button displays a modal to create an architectural artifact.
-   **[Architectural Decision Records \(ADR\) enhancements](https://www.servicenow.com/docs/access?context=eaw-managing-arch-decision-records&family=zurich&ft:locale=en-US)**
    -   Create artifact type Architectural Decision Records \(ADR\) in one step.
    -   Create and add multiple pages to the Architectural Decision Records \(ADR\) from the **Artifact content** tab.
    -   In the Architectural Decision Records \(ADR\) page, you can tag the following:
        -   Tag a user
        -   Tag a record
            -   Architectural artifact
            -   Business application
            -   Business capability
            -   Business process
            -   Digital integration \(requires the digital integration plugin\)
            -   Digital interface \(requires the digital integration plugin\)
            -   Information object
            -   TRM product \(requires the TRM plugin\)
            -   Value stream \(requires the value stream plugin\)
    -   Request approval workflow for Architectural Decision Records \(ADR\).
    -   The version drop-down list is added to the Architectural Decision Records \(ADR\) page header. Select a version from the drop-down list to open the specific ADR version.
-   **[Data Certification changes](https://www.servicenow.com/docs/access?context=eaw-config-cert-schedules&family=zurich&ft:locale=en-US)**

In the Enterprise Architecture Workspace, the certifications data is saved to and fetched from the CMDB Data Management Task Control \[cmdb\_data\_management\_task\] table.If your certification data is still fetched from the Certification Schedules \[cert\_schedule\] table, you might consider migrating your certification policies to the CMDB Data Management Task Control \[cmdb\_data\_management\_task\] table. For more information, see [Convert legacy certification schedules into Data Manager Certification policies](https://www.servicenow.com/docs/access?context=convert-data-cert-definitions&family=zurich&ft:locale=en-US)and[Publish a draft Data Manager policy in CMDB Workspace](https://www.servicenow.com/docs/access?context=data-manager-publish-draft-policy&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

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

Yokohama

</td><td>

-   **[Application Rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&family=yokohama&ft:locale=en-US)**
    -   Added the **Score for fiscal period** filter drop-down.
    -   Added a filter button.
    -   Removed the previously available filter drop-downs.
    -   Added the export icon.
    -   Added the technical debt column on the list view page.
    -   Added the technical debt indicator in the bubble size list under the settings of the bubble chart page.

 -   **[View business capabilities for a business application](https://www.servicenow.com/docs/access?context=eaw-view-business-capabilities-assoc-with-ba&family=yokohama&ft:locale=en-US)**

Added the **Business Capabilities** tab in the business application related list. **Add** and **Remove** buttons are added to associate or dissociate a business capability with a business application.

-   **[Business application related list enhancements](https://www.servicenow.com/docs/access?context=eaw-app-portfolio&family=yokohama&ft:locale=en-US)**

The business application related list is reorganized and the available tabs are:

    -   Business Capabilities
    -   Information Objects
    -   Architectural Artifacts
    -   Digital Interfaces
    -   Digital Integrations
    -   Application Model Lifecycle
    -   CI Scores
    -   Architecture Reviews
-   **[Insights section enhancements](https://www.servicenow.com/docs/access?context=eaw-insights&family=yokohama&ft:locale=en-US)**

A new card "Past due certification tasks for business applications" is added in the **Application Portfolio** tab of the Insights section. The following cards are removed the **Application Portfolio** tab of the Insights section:

    -   Open quarterly certifications for business applications
    -   Open on demand certifications for business applications
-   **[Enterprise Modeling and Visualization](https://www.servicenow.com/docs/access?context=eaw-modeling&family=yokohama&ft:locale=en-US) enhancements**
    -   In the Diagrams page, added an option to create a business process map.
    -   Added a field in the shape library element form to show or hide the shape for different diagram types.
    -   The following categories are added for the ArchiMate shapes:
        -   ArchiMate- Application Layer
        -   ArchiMate- Business Layer
        -   ArchiMate- Technology Layer
        -   ArchiMate- Relationships
    -   Enhanced the Enterprise Architecture shape library with new shapes for Value Stream and Value Stream Stage.
-   **[Architectural Artifacts](https://www.servicenow.com/docs/access?context=eaw-managing-architectural-artifacts&family=yokohama&ft:locale=en-US) enhancements**
    -   In the Architectural Artifacts list of the Portfolio page, selecting the **New** button displays a modal to create an architectural artifact.
    -   In the architectural artifact details page, the **Upload Version** button is renamed to **New version** version.
    -   In the architectural artifact related list, the following tabs are removed:
        -   Role permissions
        -   User Criteria permissions
        -   User permissions
        -   Group permissions
    -   Added the **Share** button in the architectural artifacts **Details** tab in the Portfolio page to share the architectural artifacts with users and groups.
    -   In the architectural artifact related list, renamed the Architectural Artifact Versions tab to Artifact versions.
    -   In the **Artifact versions** tab, the New button is removed.
    -   In the Portfolio page, the Architectural Artifact Versions section is removed from the Information Portfolio. Added the **New version** button at the artifact version details page.
    -   In the architectural artifact **Details** tab, the Access Setting section is removed.
    -   In the architectural artifact **Details** tab, the **Download artifact** button is removed. Added the **Download** button on the artifact version page.
-   **[Configure certification policies](https://www.servicenow.com/docs/access?context=eaw-config-cert-schedules&family=yokohama&ft:locale=en-US)**

In the Setup page, the Certification Schedules section is renamed to Certification Policies.


 -   **[Create diagram action](https://www.servicenow.com/docs/access?context=eaw-modeling-create-diagram-action&family=yokohama&ft:locale=en-US)**

An option to open diagram actions list for the Enterprise Modeling and Visualization in the Setup page.

-   **[Create a blank diagram using modeling in the EA Workspace](https://www.servicenow.com/docs/access?context=eaw-modeling-create-diagram&family=yokohama&ft:locale=en-US)**

In the Enterprise Modeling and Visualization, an option to create blank diagrams is added.

-   **[Restart scheduled job](https://www.servicenow.com/docs/access?context=eaw-restart-tpm-scheduled-job&family=yokohama&ft:locale=en-US)**

The **Restart** button added on the TPM Logs page to restart the Populate TPM Discovered Technologies and Lifecycles scheduled job.

-   **[TRM technical debt form](https://www.servicenow.com/docs/access?context=eaw-trm-technical-debt-form&family=yokohama&ft:locale=en-US)**

The technical debts table \[sn\_apm\_trm\_standards\_technical\_debt\] displays the server details for the TRM products along with the associated business applications details, and the reason for the technical debt.


 -   **[Regenerate indicator scores in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-regenerate-indicator-score&family=yokohama&ft:locale=en-US)**

The following buttons are added to generate scores for indicators and scoring profiles:

    -   The **Regenerate indicator score** button is added in the Indicator record.
    -   The **Generate scores** button is added in the Scoring Profile record.
-   **[Portfolio list view](https://www.servicenow.com/docs/access?context=portfolio-list-view&family=yokohama&ft:locale=en-US)**

New modules and features have been added in the Portfolio section.

-   **[Add additional category details for TRM products](https://www.servicenow.com/docs/access?context=eaw-request-a-trm-products&family=yokohama&ft:locale=en-US)**

The **Other Category** field is added in the Request TRM Product form and the Create TRM product form. Using this data, you can filter for TRM products using additional categories details.


</td></tr><tr><td>

Zurich

</td><td>

-   **Granular level admin role changes**

Added granular level admin role \(sn\_apm.apm\_admin\) to the following system properties in the Enterprise Architecture Workspace:

    -   glide.ui.sn\_apm\_di\_digital\_interface\_activity.fields- Digital Interface activity formatter fields.
    -   glide.ui.sn\_apm\_di\_digital\_integration\_activity.fields- Digital Integration activity formatter fields.
    -   sn\_apm\_tpm.discoveryModelProductTypesForTPM- Product types of discovery models to consider for TPM software suggestions.
    -   sn\_apm\_tpm.configurationItemsWithSoftwareInstalls- Non hardware configuration items which have software models for TPM discovery process.

 -   **[Data certification](https://www.servicenow.com/docs/access?context=eaw-work-with-data-cert&family=zurich&ft:locale=en-US)**

Added the Data Certification section to the Enterprise Architecture Workspace. Also, added the Data Certification icon to the navigation menu of the Enterprise Architecture Workspace.

-   **[Enterprise Modeling and Visualization enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-ent-model-and-visual&family=zurich&ft:locale=en-US)**
    -   Added AWS, CSDM, and EA Extended shape libraries.
    -   Added the Toggle Shape Library icon to show or hide the shapes panel.
    -   Added the expand and collapse icons to the shapes categories within the shapes panel.
    -   Added a view modes icon to switch between list and grid views for shape libraries.
    -   Added a download icon to download the diagram as a PNG image.
    -   Added the Modify business process details icon on the business process diagram page.
-   **[TRM catalog](https://www.servicenow.com/docs/access?context=eaw-export-trm-prod-cat-data&family=zurich&ft:locale=en-US)**

Added an export icon to the TRM catalog page under Technology Portfolio.

-   **[Business Portfolio](https://www.servicenow.com/docs/access?context=eaw-export-business-portfolio-data&family=zurich&ft:locale=en-US)**

Added an export icon to the Business Portfolio page.

-   **[TRM category](https://www.servicenow.com/docs/access?context=trm-category-form&family=zurich&ft:locale=en-US)**

Added the Owner field in the TRM category form.

-   **[TPM lifecycle identifier](https://www.servicenow.com/docs/access?context=eaw-tpm&family=zurich&ft:locale=en-US)**

Added the TPM lifecycle record identifier on the **TPM lifecyles** tab on the Technology Portfolio page.


 -   **[Application Rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&family=zurich&ft:locale=en-US)**
    -   Changed the landing page for application rationalization from Bubble chart view to List view.
    -   Enhanced the Bubble chart view to group the business application bubbles whose X and Y-axis values are within the range of +/-0.25 of each other.
    -   Added zoom in, zoom out, and zoom reset buttons to the Bubble chart page.
    -   Moved the planned disposition legend to the bottom of the Bubble chart page.
    -   Display the business application details in the side panel on selecting a single bubble on the Bubble chart page.
    -   Display the list of business application applications in the side panel on selecting a grouped bubble on the Bubble chart page.
    -   Added the bubble count details icon on the Bubble chart page to show the calculation logic for number of bubbles displayed on the Bubble chart.
    -   Added the Data visibility icon to show or hide the Data visibility side panel on the List view page. On enabling the **Show actual score data** toggle on the Data visibility side panel, the **Actuals** column appears to display the non normalized indicator scores.
    -   Added the **Score for fiscal period** filter drop-down.
    -   Added a filter button.
    -   Removed the previously available filter drop-downs.
    -   Added the export icon.
    -   Added the technical debt column on the list view page.
    -   Added the technical debt indicator in the bubble size list under the settings of the bubble chart page.
    -   Updated the color palette of the bubbles in the bubble chart view with bolder hues to enhance the usability and legibility of the bubbles.
-   **[Business applications by TCO score widget](https://www.servicenow.com/docs/access?context=eaw-workspace-dashboard&family=zurich&ft:locale=en-US)**
    -   Added X and Y-axis details for the Business applications by TCO score widget in the **Portfolio TCO** tab of the Enterprise Architecture Workspace page. The X-axis denotes the TCO scores while the Y-axis denotes the number of business applications.
    -   Score calculations are denoted by integers.
-   **[Portfolio page enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-portfolio-list-view&family=zurich&ft:locale=en-US)**
    -   Added the AI Portfolio module.
    -   Added the Product Capabilities section to the Application Portfolio module.
-   **[Portfolio Overview and Health section enhancements on Enterprise Architecture Workspace home page](https://www.servicenow.com/docs/access?context=eaw-apply-filters-portfolio-overview-and-health&family=zurich&ft:locale=en-US)**
    -   Added a filter button to the Portfolio Overview and Health section.
    -   Removed the previously available filter drop-downs.
    -   Added an indicator on the filter button to show the number of applied filters.

 -   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[View business capabilities for a business application](https://www.servicenow.com/docs/access?context=eaw-view-business-capabilities-assoc-with-ba&family=zurich&ft:locale=en-US)**

Added the **Business Capabilities** tab in the business application related list. **Add** and **Remove** buttons are added to associate or dissociate a business capability with a business application.

-   **[Business application related list enhancements](https://www.servicenow.com/docs/access?context=eaw-app-portfolio&family=zurich&ft:locale=en-US)**

The business application related list is reorganized, and includes the following available tabs:

    -   Business capabilities
    -   Product capabilities
    -   Information Objects
    -   Architectural Artifacts
    -   Digital Interfaces
    -   Digital Integrations
    -   Total Cost of Ownership
    -   Application Model Lifecycle
    -   TLM Discovered Technologies
    -   TRM Technical Debts
    -   TRM Products
    -   CI Scores
    -   Architecture Reviews
    -   Lifecycle Timelines
-   **[Insights section enhancements on Enterprise Architecture Workspace home page](https://www.servicenow.com/docs/access?context=eaw-insights&family=zurich&ft:locale=en-US)**

A new card "Past due certification tasks for business applications" is added in the **Application Portfolio** tab of the Insights section. The following cards are removed from the **Application Portfolio** tab of the Insights section:

    -   Open quarterly certifications for business applications
    -   Open on demand certifications for business applications
-   **[Enterprise Modeling and Visualization enhancements](https://www.servicenow.com/docs/access?context=eaw-modeling&family=zurich&ft:locale=en-US)**
    -   Added an option to select upstream related records in the Add related records pop-up window.
    -   Added new fields to the Duplicate pop-up window, when trying to duplicate a business process map. The fields are to associate the duplicated business process map with a new business process or an existing business process.
    -   Added an adornment to add text to the connector line between shapes in a diagram.
    -   In the Diagrams page, added a button to delete existing diagrams.
    -   Enhanced the Enterprise Architecture shape library with new shapes for:
        -   Value Stream
        -   Value Stream Stage
        -   AI Model Digital Asset
        -   AI Dataset Digital Asset
        -   AI Prompt Digital Asset
        -   AI System Digital Asset
    -   The **View details** button for a diagram displays the version label, planned rollout date, and description details of that diagram version. Also, added an **Edit** button on the View details pop-up window, to modify the version label, planned rollout date, and description details.
    -   Added new fields to the **Save as new version** pop-up window.
    -   Added **Undo** and **Redo** buttons to the diagram canvas page.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Enterprise Architecture \(formerly Application Portfolio Management\) is available with activation of the Enterprise Architecture \(com.snc.apm\), which requires a separate subscription. For details, see [Enterprise Architecture](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&family=zurich&ft:locale=en-US).


**Important:** Enterprise Architecture is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Define and track data certifications using the Data Certification workflow in the Enterprise Architecture Workspace to ensure the accuracy, completeness, and reliability of critical data within your organization.
-   Design the future-state cloud modeling using the standardized AWS components in the Enterprise Modeling and Visualization to reflect AWS infrastructure and services.
-   Perform end-to-end modeling with full alignment to CSDM \(Common Service Data Model\)5.0 standards including standardized shapes, colors, and relationships.
-   Group business application bubbles on the Application Rationalization Bubble chart page whose X and Y-axis values are within the value range of +/-0.25 of each other.
-   Export the TRM catalog data and Business Portfolio data to Microsoft Excel or CSV format.
-   Apply filters to the Application Rationalization bubble chart and list views pages, using the new filter options to filter for specific business applications. Also, select a fiscal period on the Application Rationalization pages using the new fiscal period filter option.
-   Evaluate the technical debt score for business applications using the Technology Reference Model \(TRM\) technical debt indicator. This helps you to identify high-risk business applications and enables you to prioritize modernization and rationalization.

 See [Enterprise Architecture \(formerly Application Portfolio Management\)](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-yokohama-brazil/rn-combined-intro.md)

