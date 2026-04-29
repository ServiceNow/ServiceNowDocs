---
title: Enterprise Architecture release notes
description: The ServiceNow Enterprise Architecture application unites strategic and operational teams, enabling organizations to achieve their business objectives. Enterprise Architecture was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
---

# Enterprise Architecture release notes

The ServiceNow® Enterprise Architecture application unites strategic and operational teams, enabling organizations to achieve their business objectives. Enterprise Architecture was enhanced and updated in the Australia release.

## Enterprise Architecture Workspace highlights for the Australia release

-   Publish a Technology Reference Model \(TRM\) catalog using the ServiceNow Knowledge Management product to easily find, adopt, and share approved technology standards through a centralized, risk‑managed TRM catalog that is searchable using AI search capability. The published TRM catalog is accessible across the organization or beyond, as needed.
-   Create documents for Enterprise Modeling and Visualization diagrams to publish, share, and archive diagrams together with their associated data. With a single action, you can transform diagrams into ready‑to‑use documents, reducing manual copy‑and‑paste effort. The generated documents support collaboration and editing, can be exported to PDF, and can support approval workflows for governed review and lifecycle management.
-   Add and manage labels on the relationship lines more easily in empty diagrams, hierarchy diagrams, and Business Process Modeling Notation \(BPMN\) diagrams.
-   Visually explore and analyze architecture data modeled using the Architecture Analyzer feature in the Enterprise Architecture Workspace.
-   Store and manage architectural documents, including documents generated from diagrams in the modeling tool using the Architectural Documents under Information Portfolio.
-   Explore and analyze Common Service Data Model \(CSDM\) architecture relationships directly on a visual canvas in the Enterprise Architecture Workspace. You can assess current state of an entity, understand dependencies, and share the insights with stakeholders.
-   Apply the granular level admin role changes to provide safer and more controlled approach to manage access in the Enterprise Architecture Workspace.
-   Determine the bubble size using the Overall score indicator on the Application Rationalization Bubble Chart page.

See [Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=ea-workspace&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US) for more information.

## New in the Australia release

-   **[Enterprise Modeling and Visualization enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-ent-model-and-visual&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

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
-   **[Exploring the publishing center in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=publishing-center-in-ea-workspace&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

    Use the Publishing Center to control publishing workflows, monitor status, and view publishing history from a single location.

-   **[Publish TRM catalog to a knowledge base](https://www.servicenow.com/docs/access?context=working-with-publishing-center&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**
    -   Configure TRM catalogs and apply filters for products and lifecycle phases.
    -   Manage publishing workflows with status updates from Draft to Published.
    -   View publishing job history in the Run logs tab.
    -   Access the published TRM catalog using the generated knowledge base URL.
-   **Enhancements to the [Value stream](https://www.servicenow.com/docs/access?context=eaw-manage-value-streams&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US) and [Value stream stage](https://www.servicenow.com/docs/access?context=eaw-manage-value-stream-stages&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US) related lists**
    -   Value stream: View associated value stream stages and application models as related lists. You can add, edit, or remove the associated value stream stages and application models.
    -   Value stream stage: View associated business processes and business capabilities. Add or remove business processes and business capabilities. You can also view the value stream stage as a related list in the business process and business capability records.
-   **[Enhancements to the Business Process related lists](https://www.servicenow.com/docs/access?context=eaw-manage-business-processes&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

    View the value stream stage as a related list of a business process.

-   **[Enhancements to the Business Capability related lists](https://www.servicenow.com/docs/access?context=eaw-manage-business-capabilities&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

    View the value stream stage as a related list of a business capability.

-   **[Create documents for the Enterprise Modeling and Visualization diagrams](https://www.servicenow.com/docs/access?context=create-documents-for-diagrams&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**
    -   Save diagram as a document using the Generate document option from the Enterprise Modeling and Visualization diagrams page.
    -   Define templates for the documents that can be created and used from the Diagrams page.
    -   Tag components that can be included in the templates to generate documents.
    -   View associated documents from the Diagrams page.
-   **[Exploring the architecture analyzer](https://www.servicenow.com/docs/access?context=eaw-explore-arch-analyzer&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)Architecture Analyzer**
    -   The Architectural Analyzer helps you to analyze architecture data without creating or maintaining custom diagrams. You can visually explore relationships across applications, services, and infrastructure to quickly understand dependencies and collaborate on architecture decisions. You can also understand the potential impact of architectural changes across applications and services.
    -   Added support for analyzing all EA extended entities that are part of Enterprise Modeling and Visualization, such as
        -   Control
        -   Digital integration
        -   Digital interface
        -   GRC risk
        -   Product capability
        -   TRM product
    -   The **Clear** button clears all the selections made in the **Add to canvas** boxes.
-   **[Application rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

    Added an Overall score indicator to show the overall average score of a business application. Use this indicator to determine the bubble size of a business application on the Bubble Chart page. You can compare the overall scores of different business applications using their individual bubble sizes.


## UI changes

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

## Changed in this release

-   **[Granular admin role changes in Enterprise Architecture](https://www.servicenow.com/docs/access?context=eaw-gran-admin-role-changes&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

    Added the granular level admin role \(sn\_apm.apm\_admin\) to the following system properties in the Enterprise Architecture:

    -   **sn\_apm\_trm.is\_product\_life\_cycle\_tech\_debt\_enabled**: Make this property false to disable calculating level 2 technical debt.
    -   **glide.ui.sn\_apm\_trm\_product\_request\_activity.fields**: TRM Product Request activity formatter fields.
    -   **sn\_apm\_trm.noOfPublishersPerTRMPage**: The number of publishers to show per page.
    -   **glide.ui.sn\_apm\_trm\_product\_lifecycle\_request\_activity.fields**: TRM Product Lifecycle Request activity formatter fields.
    -   **sn\_apm.noOfSoftwareModelsPerTPMPage**: The number of software models to show per page. This property is used for client-side pagination.
    -   **sn\_apm.discoveryModelProductTypesForTPMSuggestions**: Product types of discovery models to consider for TPM software suggestions.
    -   **sn\_apm.noOfSDLCComponentPerTPMPage**: The number of SDLC components to show per page.
    -   **glide.ui.cmdb\_ci\_business\_app\_activity.fields**: Business application activity formatter fields.
    -   **sn\_apm.startRangeOfTPMLifecycle**: The number of years prior to the current date is included when displaying software model lifecycle phases in the TPM timeline.
    -   **sn\_apm.endRangeOfTPMLifecycle**: The number of years beyond the current date is included when displaying software model lifecycle phases in the TPM timeline.
    -   **noOfBusinessAppsPerTPMPage**: The number of business applications to show per page.

-   **[Enhancements to the My certifications section](https://www.servicenow.com/docs/access?context=manage-requests-certs-assessments&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

    View only the certifications that are relevant to you in the **My certifications** tab on the Enterprise Architecture Workspace home page.


-   **[Enhancements to the Application Portfolio](https://www.servicenow.com/docs/access?context=eaw-work-with-application-portfolio&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

    Business applications with the Retired state or Lifecycle stage as End of life are no longer displayed in the Business Portfolio section.


## Activation information

Enterprise Architecture \(formerly Application Portfolio Management\) is available with activation of the Enterprise Architecture \(com.snc.apm\), which requires a separate subscription. For details, see [Enterprise Architecture](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US).

## Accessibility information

-   Navigate the interface using the keyboard on the Enterprise Modeling and Visualization pages.
-   Access the shape context menu using the keyboard on the Enterprise Modeling and Visualization canvas. On navigating to a particular shape context menu button, the selected button gets highlighted.
-   See pop-over menus when hovering over connector lines on the Enterprise Modeling and Visualization canvas.
-   Reflow- The Enterprise Architecture Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.


## Related ServiceNow applications and Features

-   **[Now Assist for Enterprise Architecture \(EA\) release notes](now-assist-for-ea-rn.md)**

    The ServiceNow® Now Assist for Enterprise Architecture \(EA\) application introduces generative AI skills into the Enterprise Architecture Workspace.


**Parent Topic:**[Enterprise Architecture release notes](enterprise-architecture-rn-landing.md)

