---
title: Enterprise Architecture release notes
description: The ServiceNow Enterprise Architecture application unites strategic and operational teams, enabling organizations to achieve their business objectives. Enterprise Architecture was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 15
---

# Enterprise Architecture release notes

The ServiceNow® Enterprise Architecture application unites strategic and operational teams, enabling organizations to achieve their business objectives. Enterprise Architecture was enhanced and updated in the Zurich release.

## Enterprise Architecture highlights for the Zurich release

-   Define and track data certifications using the Data Certification workflow in the Enterprise Architecture Workspace to ensure the accuracy, completeness, and reliability of critical data within your organization.
-   Design the future-state cloud modeling using the standardized AWS components in the Enterprise Modeling and Visualization to reflect AWS infrastructure and services.
-   Perform end-to-end modeling with full alignment to CSDM \(Common Service Data Model\)5.0 standards including standardized shapes, colors, and relationships.
-   Group business application bubbles on the Application Rationalization Bubble chart page whose X and Y-axis values are within the value range of +/-0.25 of each other.
-   Export the TRM catalog data and Business Portfolio data to Microsoft Excel or CSV format.
-   Apply filters to the Application Rationalization bubble chart and list views pages, using the new filter options to filter for specific business applications. Also, select a fiscal period on the Application Rationalization pages using the new fiscal period filter option.
-   Evaluate the technical debt score for business applications using the Technology Reference Model \(TRM\) technical debt indicator. This helps you to identify high-risk business applications and enables you to prioritize modernization and rationalization.

See [Enterprise Architecture \(formerly Application Portfolio Management\)](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US) for more information.

**Important:** Enterprise Architecture is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Application rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   View business application bubbles whose X and Y-axis values are within the value range of +/-0.25 of each other as a grouped bubble. The grouped bubble displays the total number of business application bubbles that it contains. This grouping helps in clearing the clutter on bubble chart when there are too many business applications with similar values. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Zoom in, zoom out, or pan on the Bubble chart page using either on-screen buttons or by using a mouse device or trackpad interactions. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   View the calculation logic behind the total number of business applications displayed on the Bubble chart page. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Select a single bubble on the Bubble chart page to view the associated business application details. Select a grouped bubble to view the list of business applications that are part of that grouped bubble. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   View actual scores of business applications and compare them with their normalized scores. For details, see [List view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-list-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Increased maximum number of bubbles displayed on the Bubble chart to 500.
    -   Apply the fiscal period filter to filter and view business applications for a specific fiscal period.
    -   Apply the application rationalization filters to filter and view specific business applications on the bubble chart or list view page. An indicator is displayed on top of the filter icon to show the number of filters currently applied.
    -   View the business application technical debt indicator score on the application rationalization list view page. On the application rationalization bubble chart view page, you can use the TRM technical debt indicator to form the bubble size based on the indicator score.
    -   Export the list view of application rationalization data to Excel or CSV file format. You can use the data to obtain insights, share with stakeholders, and prepare for analysis.
    -   Business applications with Retired or End of Life lifecycle stage aren’t displayed on the Application Rationalization bubble chart page.

-   **[Data certification in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-work-with-data-cert&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Use the Data Certification workflow in Enterprise Architecture Workspace to ensure the accuracy, completeness, and reliability of critical data within your organization. For details, see [Exploring data certification in the Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-explore-data-cert&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Create a data certification policy directly from the Enterprise Architecture Workspace using the Data certification workflow. For details, see [Create a certification policy](https://www.servicenow.com/docs/access?context=eaw-create-policy&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Run certification on demand for published policies to generate a new certification instance for an active policy. For details, see [Run certification for a policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-run-certification&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Activate a certification policy to add it to the active certification runs. This process ensures that the policy is active and can be used for certifications. You can deactivate a policy to remove it from active certification runs. For details, see [Activate a certification policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-activate&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
-   **[Enterprise Architecture Workspace home page enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-ea-workspace-homepage&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Apply the Portfolio Overview and Health filters to filter and view specific business applications and business capabilities information. An indicator is displayed on top of the filter icon to show the number of filters currently applied.

-   **[Manage Enterprise Modeling and Visualization](https://www.servicenow.com/docs/access?context=eaw-config-modeling&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Create a diagrams using CSDM shapes to ensure consistency in how services, applications, and infrastructure are represented. Aligning with CMDB 5 standards, helps you in accurate reporting, impact analysis, and compliance across the enterprise. For details, see [Common Service Data Model \(CSDM\) shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-csdm-shapes&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Use the modified Enterprise Architecture shapes that are aligned with CSDM 5 standards for better modeling, accurate impact analysis, and reporting. For details, see [Create a diagram using CSDM shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-create-diagram-csdm&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Create diagrams using AWS shapes. The AWS shapes enable you to visualize AWS cloud components, model hybrid architectures, support cloud migration planning. For details, see [Amazon Web Services \(AWS\) shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-aws-shapes&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US) and [Create a diagram using AWS shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-create-diagram-aws&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Group or ungroup a general shape object. You can combine multiple related shapes into a single container for better organization and clarity in diagrams. For details, see [Convert a shape to a group shape](https://www.servicenow.com/docs/access?context=eaw-modeling-group-ungroup-shape&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Expand or collapse a group shape to simplify visualization, improve focus, and supports hierarchical modeling. For details, see [Expand or collapse a group shape](https://www.servicenow.com/docs/access?context=eaw-modeling-expand-collapse-shape&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   View Business Process details for which the BPMN diagram is being created. Modify details such as name, parent, and description. For details, see [Modify BPMN diagram details](https://www.servicenow.com/docs/access?context=eaw-modeling-modify-bpmn&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Reorder shape categories within the Shapes panel to customize the panel for faster access to frequently used shapes. For details, see [Reorder shapes categories](https://www.servicenow.com/docs/access?context=eaw-modeling-reorder-shapes-cat&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Show or hide the Shapes panel to optimize your workspace for different tasks. For details, see [Show or hide shapes panel](https://www.servicenow.com/docs/access?context=eaw-modeling-show-hide-shapes-panel&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Switch between List view and Grid view in the shapes panel according to your modeling needs. For details, see [Switch to list or grid view of shapes panel](https://www.servicenow.com/docs/access?context=eaw-modeling-shapes-grid-list-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Download a diagram as an image to share it with other stakeholders with offline access or use it in the presentations. For details, see [Download a modeling diagram as an image](https://www.servicenow.com/docs/access?context=eaw-modeling-download-diagram&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
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
-   **[TRM catalog enhancement](https://www.servicenow.com/docs/access?context=eaw-export-trm-prod-cat-data&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Export the TRM catalog data to Microsoft Excel or CSV format.

-   **[Business Portfolio enhancement](https://www.servicenow.com/docs/access?context=eaw-export-business-portfolio-data&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Export the Business Portfolio data to Microsoft Excel or CSV format.

-   **[TRM category enhancements](https://www.servicenow.com/docs/access?context=eaw-create-new-trm-category&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Assign an owner to a TRM category to ensure clear accountability and improved governance standards. The owner is responsible for maintaining consistent technology compliance standards for that TRM category.

-   **[TPM lifecycle record enhancements](https://www.servicenow.com/docs/access?context=eaw-tpm&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   TPM lifecycle records are now assigned unique identifiers are automatically,while creating the TPM lifecycle record. These identifiers serve as clickable links that provide direct access to full record details.
    -   Run the Populate Number field in TPM Discovered Technologies scheduled job to populate the TPM lifecycle record identifiers of existing records created using previous versions \(before version 1.9.0\) of the TPM plugin. For details, [Run a scheduled job to populate Technology Portfolio Management lifecycle record identifier](https://www.servicenow.com/docs/access?context=eaw-run-job-to-populate-tpm-lifecycle-identifier&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
-   **[Working with Portfolio list view](https://www.servicenow.com/docs/access?context=eaw-work-with-portfolio-list-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)[AI Portfolio section enhancements](https://www.servicenow.com/docs/access?context=eaw-exploring-the-ai-portfolio&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    The following AI product models added to the AI Portfolio section:

    -   AI System Product Models
    -   AI Model Product Models
    -   AI Dataset Product Models
    -   AI Prompt Product Models
-   **[Business application related list enhancements](https://www.servicenow.com/docs/access?context=eaw-app-portfolio&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Added the AI Product Models as a related list. In the tab, you can:

    -   Select **Add** to associate an existing AI system product model to the business application.
    -   Select **Remove** to remove a AI system product model from a business application.
    For details, see [Add AI systems to business applications](https://www.servicenow.com/docs/access?context=eaw-add-ai-systems&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).

    -   Added the **Product capability** tab as a related list. In the tab, you can:
        -   Select **New** to create a new product capability and associate it with the business application.
        -   Select **Add** to add an existing product capability to the business application.
        -   Select **Remove** to remove a product capability from a business application.
    -   Added the TRM products tab as a related list. In the tab, you can:
        -   Select **New** to create a new TRM product and associate it with the business application.
        -   Select **Add** to add an existing TRM product to the business application.
        -   Select **Remove** to remove a TRM product from a business application.
    -   In the **Architectural Artifacts** tab of the business application related list, selecting the **New** button displays a modal to create an architectural artifact.
-   **[TRM product related list enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-trm&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Added the **Product capability** tab as a related list. In the tab, you can:
        -   Select **New** to create a new product capability and associate it with the TRM product.
        -   Select **Add** to add an existing product capability to the TRM product.
        -   Select **Remove** to remove a product capability from a TRM product.
    -   Added the **Business Applications** tab as a related list. In the tab, you can:
        -   Select **New** to create a new business application and associate it with the TRM product.
        -   Select **Add** to add an existing business application to the TRM product.
        -   Select **Remove** to remove a business application from a TRM product.
-   **[Architectural Decision Records \(ADR\) enhancements](https://www.servicenow.com/docs/access?context=eaw-managing-arch-decision-records&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
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
-   **[Data Certification changes](https://www.servicenow.com/docs/access?context=eaw-config-cert-schedules&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    In the Enterprise Architecture Workspace, the certifications data is saved to and fetched from the CMDB Data Management Task Control \[cmdb\_data\_management\_task\] table.

    If your certification data is still fetched from the Certification Schedules \[cert\_schedule\] table, you might consider migrating your certification policies to the CMDB Data Management Task Control \[cmdb\_data\_management\_task\] table. For more information, see [Convert legacy certification schedules into Data Manager Certification policies](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/convert-data-cert-definitions.html)and[Publish a draft Data Manager policy in CMDB Workspace](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/data-manager-publish-draft-policy.html%22%20HYPERLINK%20%22https:/www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/data-manager-publish-draft-policy.html).


## Changed in this release

-   **Granular level admin role changes**

    Added granular level admin role \(sn\_apm.apm\_admin\) to the following system properties in the Enterprise Architecture Workspace:

    -   glide.ui.sn\_apm\_di\_digital\_interface\_activity.fields- Digital Interface activity formatter fields.
    -   glide.ui.sn\_apm\_di\_digital\_integration\_activity.fields- Digital Integration activity formatter fields.
    -   sn\_apm\_tpm.discoveryModelProductTypesForTPM- Product types of discovery models to consider for TPM software suggestions.
    -   sn\_apm\_tpm.configurationItemsWithSoftwareInstalls- Non hardware configuration items which have software models for TPM discovery process.

## UI changes

-   **[Data certification](https://www.servicenow.com/docs/access?context=eaw-work-with-data-cert&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Added the Data Certification section to the Enterprise Architecture Workspace. Also, added the Data Certification icon to the navigation menu of the Enterprise Architecture Workspace.

-   **[Enterprise Modeling and Visualization enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-ent-model-and-visual&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Added AWS, CSDM, and EA Extended shape libraries.
    -   Added the Toggle Shape Library icon to show or hide the shapes panel.
    -   Added the expand and collapse icons to the shapes categories within the shapes panel.
    -   Added a view modes icon to switch between list and grid views for shape libraries.
    -   Added a download icon to download the diagram as a PNG image.
    -   Added the Modify business process details icon on the business process diagram page.
-   **[Application Rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
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
-   **[TRM catalog](https://www.servicenow.com/docs/access?context=eaw-export-trm-prod-cat-data&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Added an export icon to the TRM catalog page under Technology Portfolio.

-   **[Business Portfolio](https://www.servicenow.com/docs/access?context=eaw-export-business-portfolio-data&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Added an export icon to the Business Portfolio page.

-   **[TRM category](https://www.servicenow.com/docs/access?context=trm-category-form&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Added the Owner field in the TRM category form.

-   **[TPM lifecycle identifier](https://www.servicenow.com/docs/access?context=eaw-tpm&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Added the TPM lifecycle record identifier on the **TPM lifecyles** tab on the Technology Portfolio page.

-   **[Business applications by TCO score widget](https://www.servicenow.com/docs/access?context=eaw-workspace-dashboard&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Added X and Y-axis details for the Business applications by TCO score widget in the **Portfolio TCO** tab of the Enterprise Architecture Workspace page. The X-axis denotes the TCO scores while the Y-axis denotes the number of business applications.
    -   Score calculations are denoted by integers.
-   **[Portfolio page enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-portfolio-list-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Added the AI Portfolio module.
    -   Added the Product Capabilities section to the Application Portfolio module.
-   **[Portfolio Overview and Health section enhancements on Enterprise Architecture Workspace home page](https://www.servicenow.com/docs/access?context=eaw-apply-filters-portfolio-overview-and-health&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Added a filter button to the Portfolio Overview and Health section.
    -   Removed the previously available filter drop-downs.
    -   Added an indicator on the filter button to show the number of applied filters.
-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[View business capabilities associated with a business application](https://www.servicenow.com/docs/access?context=eaw-view-business-capabilities-assoc-with-ba&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    Added the **Business Capabilities** tab in the business application related list. **Add** and **Remove** buttons are added to associate or dissociate a business capability with a business application.

-   **[Business application related list enhancements](https://www.servicenow.com/docs/access?context=eaw-app-portfolio&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    The business application related list is reorganized, and includes the following available tabs:

    -   Business capabilities
    -   Product capabilities
    -   Information Objects
    -   Architectural Artifacts
    -   Digital Interfaces
    -   Digital Integrations
    -   Total Cost of Ownership
    -   Application Model Lifecycle
    -   TPM Discovered Technologies
    -   TRM Technical Debts
    -   TRM Products
    -   CI Scores
    -   Architecture Reviews
    -   Lifecycle Timelines
-   **[Insights section enhancements on Enterprise Architecture Workspace home page](https://www.servicenow.com/docs/access?context=eaw-insights&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

    A new card "Past due certification tasks for business applications" is added in the **Application Portfolio** tab of the Insights section. The following cards are removed from the **Application Portfolio** tab of the Insights section:

    -   Open quarterly certifications for business applications
    -   Open on demand certifications for business applications
-   **[Enterprise Modeling and Visualization enhancements](https://www.servicenow.com/docs/access?context=eaw-modeling&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
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

## Activation information

Enterprise Architecture \(formerly Application Portfolio Management\) is available with activation of the Enterprise Architecture \(com.snc.apm\), which requires a separate subscription. For details, see [Enterprise Architecture](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Enterprise Architecture release notes](enterprise-architecture-rn-landing.md)

