---
title: Enterprise Architecture \(formerly Application Portfolio Management\) Release Notes
description: The ServiceNow Enterprise Architecture unites strategic and operational teams, enabling organizations to achieve their business objectives. Enterprise Architecture was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
---

# Enterprise Architecture \(formerly Application Portfolio Management\) Release Notes

The ServiceNow® Enterprise Architecture unites strategic and operational teams, enabling organizations to achieve their business objectives. Enterprise Architecture was enhanced and updated in the Xanadu release.

## Enterprise Architecture \(formerly Application Portfolio Management\) highlights for the Xanadu release

-   The  ServiceNow® Application Portfolio Management product is expanding to ServiceNow® Enterprise Architecture.
-   Some Application Portfolio Management modules are deprecated and no longer searchable from the **All** menu. However, all the deprecated modules are available within the Enterprise Architecture Workspace. You must use the Enterprise Architecture Workspace to leverage those features and functionalities.

    **Note:** Existing customers can continue to use these navigation links. However, for new activation customers, the navigation will not be available from the **All** menu.

-   Create diagrams for your business applications hierarchy map, business capability map, and associate them with architectural artifacts and plan the future state modeling of your IT, with alignment to the business, using the Enterprise Modeling and Visualization functionality in Enterprise Architecture Workspace.
-   Support for industry standard ArchiMate® shapes to create modeling diagrams. ArchiMate is a registered trademark of The Open Group.
-   Support for Architectural Decision Record \(ADR\) type artifact to help you align artifacts with your business requirements.
-   Create a one-to-many relationship between a digital interface and CMDB APIs. Find out which digital integrations and interfaces use which APIs. Identify the environments where they’re deployed. Group the deployed APIs and relate them to the digital interface, which describes the design aspects of the related APIs.

See [Enterprise Architecture](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Exploring Enterprise Modeling and Visualization in the EA Workspace](https://www.servicenow.com/docs/access?context=eaw-modeling&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    Use the Enterprise Modeling and Visualization functionality in Enterprise Architecture Workspace to create diagrams for your applications hierarchy. You can associate the diagrams with architectural artifacts and plan the future state modeling of your IT with alignment to the business. Creating modeling diagrams can you help your stakeholders to understand the complexities of the organization. Perform the following tasks using the Enterprise Modeling and Visualization:

    -   Create and update modeling diagrams using the General, Enterprise Architecture, and ArchiMate shapes.
    -   Create diagrams from the Business Application view using the Create diagram menu option.
    -   Create diagrams for Business hierarchy map and Business capability maps from the Enterprise Modeling and Visualization page.
    -   Apply colors to business capability shapes in the capability hierarchy map.
    -   Add related records to a shape. Add CI relationship or Reference type relationship.
    -   Synchronize shapes, relationships, and entire diagrams to the repository.
    -   Select an architectural category while creating a diagram.
    -   Share your diagrams with the other users or groups and define their access levels for the diagram.
    -   Leverage a workflow to get approval for the diagrams, and to enable committing the diagram to the database.
    -   Configure access for Enterprise Modeling and Visualization menu items for roles, users, and groups.
    -   Initiate modeling in the Enterprise Modeling and Visualization directly from any Unified map.
-   **[Technology Portfolio](https://www.servicenow.com/docs/access?context=eaw-technology-portfolio-view&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    The Technology Portfolio section has been restructured and new features have been added. The section now contains the following pages:

    -   TRM catalog
    -   Technical debt
    -   TPM lifecycles
    -   TPM risk
    -   Technology portfolio audit
-   **[Digital integration and interface enhancements](https://www.servicenow.com/docs/access?context=eaw-create-digital-interface&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**
    -   View Information Objects and SDLC Components associated with a digital integration or digital interface.
    -   View Credentials assigned to a digital interface, digital integration, and business application.
    -   Set the Provider company instead of Provider business application, for a Provider digital interface in a digital integration.
-   **[Portfolio section enhancements](https://www.servicenow.com/docs/access?context=portfolio-list-view&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    The Portfolio section has been restructured and new modules and features have been added. The following is the new structure:

    -   Business Architecture
        -   Business Units
        -   Departments
        -   Goals
        -   Value Streams
        -   Value Stream Stages
        -   Business Capabilities
        -   Business Processes
        -   Demands
    -   Application Portfolio
        -   Business Applications
        -   Application Services
        -   Digital Integrations
        -   Digital Interfaces
    -   Information Portfolio
        -   Data Domains
        -   Information Objects
        -   Architectural Artifacts
        -   Architectural Artifact Versions
        -   Diagrams
    -   My Entities
        -   My Business Capabilities
        -   My Business Processes
        -   My Business Applications
        -   My Application Services
        -   My Information objects
        -   My Architectural Artifacts
        -   My Technology Reference Model Products
        -   My Digital Integrations
        -   My Digital Interfaces
-   **[Setup section enhancements](https://www.servicenow.com/docs/access?context=eaw-setup&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    The configuration for Enterprise Modeling and Visualization is the following:

    -   Shape Libraries
    -   Modeling menu options
    -   Entities
    -   Relationships
    The **TPM logs** details are now available in the Setup section.

-   **[Connect a digital interface with the CMDB API in the EA Workspace](https://www.servicenow.com/docs/access?context=eaw-relate-dig-interface-api&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    Create a relationship between a digital interface and a CMDB API from the digital interface related list. Find out which digital integration uses which API. Find the environments where they’re deployed and group the deployed APIs.

-   **[Working with the Enterprise Architecture Workspace dashboard](https://www.servicenow.com/docs/access?context=eaw-workspace-dashboard&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    The following widgets are available on the TCO tab of the Enterprise Architecture Workspace dashboard.

    -   **Business applications by TCO score**
    -   **Business application TCO by cost type and planned disposition for FY:Q \(Current quarter\)**
    -   **Top 10 business applications with the highest cost for FY:Q \(Current quarter\)**
-   **[Manage information objects of a business application in EA Workspace](https://www.servicenow.com/docs/access?context=eaw-associate-info-obj-ba&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    Relate a business application to an information object using the CI relationship \[cmdb\_rel\_ci\] table of type Uses::Used by. Use this suggested relationship to get the logical data of the information object, which can be used to leverage the business application.

-   **[Technology portfolio management \(TPM\) enhancements](https://www.servicenow.com/docs/access?context=eaw-tpm&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    Added support for all CMDB configuration items in Technology Portfolio Management \(TPM\). By default, TPM support docker containers and serverless hardware tables. An admin user can configure any of the supported CMDB CIs for TPM.

-   **[TRM product enhancements](https://www.servicenow.com/docs/access?context=eaw-create-trm-prod-lifecycle&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**
    -   For a software TRM product, the **Operating system** field is added. Using this field, the operating system on which the software TRM product can be deployed, is tracked.
    -   Added support for creating wildcard for TRM lifecycle versions, to make it easier to specify a TRM standard without the need to specify the minor version.
-   **[Support for Architectural Decision Record \(ADR\) type artifact](https://www.servicenow.com/docs/access?context=eaw-create-edit-adr&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    Create or update an artifact with type architectural decision record \(ADR\) to align it with your business requirements.


## UI changes

-   **[Technology Portfolio view](https://www.servicenow.com/docs/access?context=eaw-technology-portfolio-view&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    The Technology Portfolio icon \(![Technology Portfolio icon](../image/technology-portfolio-icon.png)\) is added in the left navigation of the Enterprise Architecture Workspace.

-   **[Digital Integration and Interface](https://www.servicenow.com/docs/access?context=eaw-create-digital-interface&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    New tabs are added for Information Objects and SDLC Component in the Digital Integration and Digital Interface records.

-   **[Portfolio list view](https://www.servicenow.com/docs/access?context=portfolio-list-view&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    New modules and features have been added in the Portfolio section.

    The Technology Portfolio section has been removed, containing the following sections:

    -   Discovered Technology
    -   Technology Risk
    -   TPM Logs
    -   Technology Reference Model Products
    -   Technical Debt
    These sections are now available in the Technology Portfolio page.

    The TCO section is moved to the Application Portfolio section.

-   **[Enterprise Architecture Workspace Dashboard page](https://www.servicenow.com/docs/access?context=eaw-workspace-dashboard&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    In the Enterprise Architecture Workspace Dashboard page, the **Business Portfolio** tab has been added. For more details, see [Working with the Enterprise Architecture Workspace dashboard](https://www.servicenow.com/docs/access?context=eaw-workspace-dashboard&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US).

-   **[Enterprise Architecture Workspace home page](https://www.servicenow.com/docs/access?context=ea-workspace&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    In the Enterprise Architecture Workspace home page, the **Technology Portfolio Audit** and the **Technical Debt** tabs have been removed from the Needs Attention section.

    The Needs Attention section shows count for **My Requests**, **My Approvals,** **My Certifications**, and **My Assessment** in the respective tabs. The count helps you to know the number of items in each tab that you need to look at.

-   **[Add a TRM product in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-create-trm-prod-lifecycle&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    The **Operating system** field is added to the Technical debt page and business application Lifecycle Timelines page.

-   **[View the unified map for a business application in Enterprise Modeling and Visualization](https://www.servicenow.com/docs/access?context=eaw-view-unified-map-in-modeling-tool&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    A new button **Model** with Enterprise Modeling and Visualization is added in the business application CMDB node map.

-   **[Add related records in the modeling diagram](https://www.servicenow.com/docs/access?context=eaw-modeling-add-related-records&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    The Entities section in the Add related records window shows the number of entities and the relationship type \(CI relationship or Reference\).

-   **[Add additional category details for TRM products](https://www.servicenow.com/docs/access?context=eaw-request-a-trm-products&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    The **Other Category** field is added in the Request TRM Product form and the Create TRM product form. Using this data, you can filter for TRM products using additional categories details.

-   **[Business application form](https://www.servicenow.com/docs/access?context=eaw-apprat-business-application-form&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)**

    The **Target date** field is added in thePlanned disposition section of the business application form.


## Deprecations

Starting with the Xanadu release, some modules are deprecated from Enterprise Architecture \(formerly known as Application Portfolio Management\). The navigation links to the deprecated modules are removed from the **All** menu. If you’re an existing customer, you can continue to use these navigation links. However, if you’re a new activation customer, navigation to these modules using the navigation links from the **All** menu won’t be available. All the deprecated modules are available within the Enterprise Architecture Workspace. You’re encouraged to use the Enterprise Architecture Workspace to leverage those features and functionalities. The deprecated modules are:

-   Application Portfolio Management Home
-   Application Portfolio
-   Application Portfolio Analysis
-   Architectural Artifacts
-   Business Application Lifecycles - Service Requests
-   Application Ratings
-   Capability Ratings
-   Information Portfolio
-   Technology Portfolio Management
-   Technology Reference Model
-   Administration
    -   Business Processes
    -   Business Capabilities
    -   Application Families
    -   Application Category Groups
    -   Application Categories
    -   Application Indicators
    -   Scoring Profiles
    -   Bubble Chart
    -   Demand Actions
    -   Portfolio

## Activation information

Enterprise Architecture \(formerly Application Portfolio Management\) is available with activation of the Enterprise Architecture \(com.snc.apm\), which requires a separate subscription. For details, see [Enterprise Architecture](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US).

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

