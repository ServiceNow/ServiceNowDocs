---
title: Enterprise Architecture \(formerly Application Portfolio Management\) Release Notes
description: The ServiceNow Enterprise Architecture application unites strategic and operational teams, enabling organizations to achieve their business objectives.Enterprise Architecture was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
---

# Enterprise Architecture \(formerly Application Portfolio Management\) Release Notes

The ServiceNow® Enterprise Architecture application unites strategic and operational teams, enabling organizations to achieve their business objectives.Enterprise Architecture was enhanced and updated in the Yokohama release.

## Enterprise Architecture highlights for the Yokohama release

Yokohama Patch 6

-   Select a fiscal period on the Application Rationalization pages using the new fiscal period filter option. The fiscal period filter enables you to view application rationalization data for the selected fiscal period.
-   Evaluate the technical debt score for business applications using the Technology Reference Model \(TRM\) technical debt indicator. This helps you to identify high-risk business applications and enables you to prioritize modernization and rationalization.
-   Generate business process modeling diagrams and model the future state of the business processes using Enterprise Modeling and Visualization.
-   Associate business capabilities to a business application from the business application related list.
-   View the past due certification tasks for your business applications from the Application Portfolio tab of the Insights section.
-   Generate scores for indicators and scoring profiles in the Enterprise Architecture Workspace.
-   Read-only access to the  Enterprise Architecture Workspace is added to the business stakeholder role \(sn\_apm.apm\_read\).

Yokohama General Availability

-   Generate business process modeling diagrams and model the future state of the business processes using Enterprise Modeling and Visualization.
-   Associate business capabilities to a business application from the business application related list.
-   View the past due certification tasks for your business applications from the Application Portfolio tab of the Insights section.
-   Generate scores for indicators and scoring profiles in the Enterprise Architecture Workspace.
-   Read-only access to the  Enterprise Architecture Workspace is added to the business stakeholder role \(sn\_apm.apm\_read\).

**Important:** Enterprise Architecture is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **Yokohama Patch 6 [Application rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   Apply the fiscal period filter to filter and view business applications for a specific fiscal period.
    -   Apply the application rationalization filters to filter and view specific business applications on the bubble chart or list view page. An indicator is displayed on top of the filter icon to show the number of filters currently applied.
    -   View the business application technical debt indicator score on the application rationalization list view page. On the application rationalization bubble chart view page, you can use the TRM technical debt indicator to form the bubble size based on the indicator score.
    -   Export the list view of application rationalization data to Excel or CSV file format. You can use the data to obtain insights, share with stakeholders, and prepare for analysis.
    -   Business applications with Retired or End of Life lifecycle stage aren’t displayed on the Application Rationalization bubble chart page.
-   **[Enterprise Modeling and Visualization in the EA Workspace](https://www.servicenow.com/docs/access?context=eaw-modeling&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
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
-   **[Business application related list enhancements](https://www.servicenow.com/docs/access?context=eaw-app-portfolio&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    In the **Architectural Artifacts** tab of the business application related list, selecting the **New** button displays a modal to create an architectural artifact.

-   **[Architectural Decision Records \(ADR\) enhancements](https://www.servicenow.com/docs/access?context=eaw-managing-arch-decision-records&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
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
-   **[Data Certification changes](https://www.servicenow.com/docs/access?context=eaw-config-cert-schedules&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    In the Enterprise Architecture Workspace, the certifications data is saved to and fetched from the CMDB Data Management Task Control \(cmdb\_data\_management\_task\) table.

    If your certification data is still fetched from the Certification Schedules \(cert\_schedule\) table, you might consider migrating your certification policies to the CMDB Data Management Task Control \(cmdb\_data\_management\_task\) table. For more information, see [Convert legacy certification schedules into Data Manager Certification policies](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/convert-data-cert-definitions.html)and[Publish a draft Data Manager policy in CMDB Workspace](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/data-manager-publish-draft-policy.html%22%20HYPERLINK%20%22https:/www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/data-manager-publish-draft-policy.html)

-   **[Regenerate indicator scores in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-regenerate-indicator-score&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Generate a score for application and capability indicators for a particular period. Also, generate scores for an application scoring profile and capability scoring profile, to calculate scores for all indicators attached to that particular scoring profile.

-   **[Business stakeholder role for Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-business-stakeholder-role&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Read-only access to the  Enterprise Architecture Workspace is added to the business stakeholder role \(sn\_apm.apm\_read\).

-   **[TRM technical debt form](https://www.servicenow.com/docs/access?context=eaw-trm-technical-debt-form&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    The **TPM Discovered Technologies and Lifecycles** scheduled job fetches the server details for the TRM products.

-   **[Technology portfolio management \(TPM\) enhancements](https://www.servicenow.com/docs/access?context=eaw-tpm&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   Added a restart button on the TPM Logs page to restart the Populate TPM Discovered Technologies and Lifecycles scheduled job, in case the job is stuck and doesn’t refresh the log data for more than an hour. For more information, see [View TPM logs](https://www.servicenow.com/docs/access?context=eaw-view-tpm-logs&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US) and [Restart Populate TPM Discovered Technologies and Lifecycles scheduled job](https://www.servicenow.com/docs/access?context=eaw-restart-tpm-scheduled-job&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US).

## UI changes

-   **[Application Rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   Added the **Score for fiscal period** filter drop-down.
    -   Added a filter button.
    -   Removed the previously available filter drop-downs.
    -   Added the export icon.
    -   Added the technical debt column on the list view page.
    -   Added the technical debt indicator in the bubble size list under the settings of the bubble chart page.
-   **[View business capabilities associated with a business application](https://www.servicenow.com/docs/access?context=eaw-view-business-capabilities-assoc-with-ba&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Added the **Business Capabilities** tab in the business application related list. **Add** and **Remove** buttons are added to associate or dissociate a business capability with a business application.

-   **[Business application related list enhancements](https://www.servicenow.com/docs/access?context=eaw-app-portfolio&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    The business application related list is reorganized and the available tabs are:

    -   Business Capabilities
    -   Information Objects
    -   Architectural Artifacts
    -   Digital Interfaces
    -   Digital Integrations
    -   Application Model Lifecycle
    -   CI Scores
    -   Architecture Reviews
-   **[Insights section enhancements](https://www.servicenow.com/docs/access?context=eaw-insights&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    A new card "Past due certification tasks for business applications" is added in the **Application Portfolio** tab of the Insights section. The following cards are removed the **Application Portfolio** tab of the Insights section:

    -   Open quarterly certifications for business applications
    -   Open on demand certifications for business applications
-   **[Enterprise Modeling and Visualization](https://www.servicenow.com/docs/access?context=eaw-modeling&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US) enhancements**
    -   In the Diagrams page, added an option to create a business process map.
    -   Added a field in the shape library element form to show or hide the shape for different diagram types.
    -   The following categories are added for the ArchiMate shapes:
        -   ArchiMate- Application Layer
        -   ArchiMate- Business Layer
        -   ArchiMate- Technology Layer
        -   ArchiMate- Relationships
    -   Enhanced the Enterprise Architecture shape library with new shapes for Value Stream and Value Stream Stage.
-   **[Architectural Artifacts](https://www.servicenow.com/docs/access?context=eaw-managing-architectural-artifacts&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US) enhancements**
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
-   **[Configure certification policies](https://www.servicenow.com/docs/access?context=eaw-config-cert-schedules&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    In the Setup page, the Certification Schedules section is renamed to Certification Policies.

-   **[Regenerate indicator scores in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-regenerate-indicator-score&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    The following buttons are added to generate scores for indicators and scoring profiles:

    -   The **Regenerate indicator score** button is added in the Indicator record.
    -   The **Generate scores** button is added in the Scoring Profile record.
-   **[Create diagram action](https://www.servicenow.com/docs/access?context=eaw-modeling-create-diagram-action&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    An option to open diagram actions list for the Enterprise Modeling and Visualization in the Setup page.

-   **[Create a blank diagram using modeling in the EA Workspace](https://www.servicenow.com/docs/access?context=eaw-modeling-create-diagram&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    In the Enterprise Modeling and Visualization, an option to create blank diagrams is added.

-   **[Restart Populate TPM Discovered Technologies and Lifecycles scheduled job](https://www.servicenow.com/docs/access?context=eaw-restart-tpm-scheduled-job&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    The **Restart** button added on the TPM Logs page to restart the Populate TPM Discovered Technologies and Lifecycles scheduled job.

-   **[TRM technical debt form](https://www.servicenow.com/docs/access?context=eaw-trm-technical-debt-form&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    The technical debts table \[sn\_apm\_trm\_standards\_technical\_debt\] displays the server details for the TRM products along with the associated business applications details, and the reason for the technical debt.

-   **[Portfolio list view](https://www.servicenow.com/docs/access?context=portfolio-list-view&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    New modules and features have been added in the Portfolio section.

-   **[Add additional category details for TRM products](https://www.servicenow.com/docs/access?context=eaw-request-a-trm-products&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    The **Other Category** field is added in the Request TRM Product form and the Create TRM product form. Using this data, you can filter for TRM products using additional categories details.


## Activation information

Enterprise Architecture \(formerly Application Portfolio Management\) is available with activation of the Enterprise Architecture \(com.snc.apm\), which requires a separate subscription. For details, see [Enterprise Architecture](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US).

**Parent Topic:**[Enterprise Architecture release notes](enterprise-architecture-rn-landing.md)

