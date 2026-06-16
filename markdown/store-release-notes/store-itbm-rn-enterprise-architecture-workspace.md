---
title: Enterprise Architecture Workspace release notes
description: Version history for the Enterprise Architecture Workspace on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-enterprise-architecture-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Enterprise Architecture release notes, ServiceNow Store release notes]
---

# Enterprise Architecture Workspace release notes

Version history for the Enterprise Architecture Workspace on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.1.1 - June 2026 \(Australia\)**
    -   New: Added AI portfolio analytics widgets on EA Workspace Dashboard page and the AI Control Tower Home page. The new AI Portfolio widgets display associations between business applications and AI systems, with pie charts and legends displaying total counts. You can filter results by department, business unit, and application family.
    -   Removed: The Business applications by install type widget is removed from the EA Workspace homepage.
-   **Version 9.1.0 - June 2026**
    -   New: Added AI portfolio analytics widgets on EA Workspace Dashboard page and the AI Control Tower Home page. The new AI Portfolio widgets display associations between business applications and AI systems, with pie charts and legends displaying total counts. You can filter results by department, business unit, and application family.
    -   Removed: The Business applications by install type widget is removed from the EA Workspace homepage.
-   **Version 9.0.1 - May 2026 \(Zurich\)**
    -   New:
        -   Added a business application field to the AI use case form on the Service Portal. Use this field to associate business applications with AI systems.
        -   Added a Business applications section to the Related assets section on the Details tab of an AI system in AI Control Tower. Use this section to view the business applications associated with an AI system.
    -   Changed:
        -   Renamed the AI Product Models tab in the business application related list to AI Systems. The AI Systems tab displays list of AI systems classified into managed or unmanaged categories.
        -   Updated the default columns displayed on the AI Systems page.
-   **Version 9.0.0 - May 2026 \(Australia\)**
    -   New:
        -   Added a business application field to the AI use case form on the Service Portal. Use this field to associate business applications with AI systems.
        -   Added a Business applications section to the Related assets section on the Details tab of an AI system in AI Control Tower. Use this section to view the business applications associated with an AI system.
    -   Changed:
        -   Renamed the AI Product Models tab in the business application related list to AI Systems. The AI Systems tab displays list of AI systems classified into managed or unmanaged categories.
        -   Updated the default columns displayed on the AI Systems page.
-   **Version 8.0.2 - March 2026**
    -   New:
        -   Added Publishing Center feature to support a structured way to publish curated Enterprise Architecture content. It helps with a centralized workflow, consistency, governance, increased visibility, and activity tracking via status and run logs.
        -   Added Architecture Analyzer feature to visualize relationships between CSDM entities such as business applications, business capabilities, application services, and information objects.
    -   Changed:
        -   Renamed the Certifications tab on Enterprise Architecture Workspace home page to My Certifications. The My Certifications tab displays only tasks assigned to the logged-in user or their group.
        -   Replaced the Value stream to process tab with Value Stream Stages tab in the Value stream related list.
        -   Added business capability and business process as related list to the value stream stages.
        -   Added value stream stages as related list to the business process.
        -   Added value stream stages as related list to the business capability.
        -   Renamed ADR format to Document in the Architectural Artifact Version type choice list.
-   **Version 7.0.3 - January 2026**

    Fixed: Updated zoom controls on the bubble chart page in Application Rationalization, from mouse wheel scroll and pinch on trackpad to double-click on the chart or seleccting an area on the bubble chart. The Help side panel documents the new zoom interaction methods.

-   **Version 7.0.2 - December 2025**
    -   New:
        -   Added an icon to navigate to the Data Certification page from the left navigation menu of Enterprise Architecture Workspace.
        -   Monitor certification policies and track progress using the Data Certification page.
        -   Enabled an option to export data to Microsoft Excel or CSV format from the Business Portfolio, Application Rationalization, TRM Catalog, and Data Certification pages.
        -   Added a toggle on the side panel in the Application Rationalization page to view actual scores of business applications compared with their normalized scores.
        -   Added the following options under AI Governance section of the Portfolio page:
            -   AI System Product Models
            -   AI Model Product Models
            -   AI Dataset Product Models
            -   AI Prompt Product Models
        -   Added AI Product Models tab as a related list to a business application record. Using the tab, you can add or remove AI System associated to the business application.
    -   Fixed: Fixed spacing and UI text font issues in TRM and Application Rationalization related pages.
-   **Version 6.5.0 - October 2025**

    New:

    -   Replaced pill-based filters with advanced filters on the Application Rationalization page for both bubble chart view and list view pages
    -   Added option to export to Excel and CSV file format on pages: Business Portfolio, Application Rationalization, and TRM product category section on the Technology Portfolio page
    -   Introduced a custom-configurable application indicator that calculates a technical debt score for each business application
    -   Added fiscal period drop-down on Application Rationalization pages. The fiscal period selection is also saved in the user preference
    Changed:

    -   UX improvements of the Application Rationalization page:
        -   Changed spacing of icons, buttons, and UI text
        -   Changed font size of UI text
        -   Changed position of the bubble chart legend
    Business applications having 'End of Life' or 'Retired' lifecycle stage are excluded from Application Rationalization page.

-   **Version 6.3.0 - September 2025**
    -   New:
        -   Support for generating insights for business applications using the Now Assist skill, Business Application Insights
        -   Support for refining Architectural Decision Record \(ADR\) summaries by providing prompts to generate more targeted, relevant, and actionable summaries
-   **Version 6.0.0 - August 2025**
    -   New:
        -   Advanced filters in Portfolio Overview and Health section of the Home page
        -   AI Portfolio section is added to the Portfolio page
        -   Associate product capabilities with business applications and TRM products
        -   Associate TRM products with business applications
        -   Add label, description, and target date details to an architectural artifact version
    -   Changed: Color palette of the bubbles in the bubble chart view in Application Rationalization page
    -   Fixed:
        -   The following accessibility issues while zooming to 200%:
            -   The TRM product list was not visible
            -   The Personalize section layout was broken in the Technology Portfolio page
        -   The following accessibility issues while zooming to 400%
            -   The View all link in the Needs Attention section of the Home page was not showing correctly and was cut off
            -   The text inside the cards in the Portfolio Overview and Health section was spilling over the card edges
            -   The icon and text in the Portfolio Overview and Health cards were displayed on different lines instead of being aligned
        -   Performance improvement in the business portfolio and lifecycles timelines gantt chart
            -   Decreased the loading time and reduced the number of SQL calls
        -   Localization and translation issues
            -   Date and time formatting and language issues in the lifecycles timelines gantt chart page
-   **Version 4.0.1 - June 2025**
    -   Fixed:
        -   The architectural artifact access issues when the artifact is shared with a read user
        -   Enterprise Architecture Workspace compatibility issue with older versions of the Enterprise Modeling and Visualization application
-   **Version 3.4.0 - February 2025**
    -   New:
        -   Support for business stakeholder role \(read-only\) is added
        -   Support for ADR doc summarization and actions \(Gen AI feature\) is added
    -   Changed: Architectural decision record \(ADR\) document view is changed to full-page view
    -   Fixed: Workspace view for all tables configured for record forms
-   **Version 3.3.1 - November 2024**
    -   New:
        -   Relate a business application to an information object from the Business Application form.
        -   Initiate modeling in the Enterprise Modeling and Visualization directly from the Unified map.
        -   Create an Architectural Decision Record \(ADR\) from the Portfolio page and request for an approval.
    -   Changed:
        -   Removed the Technology Portfolio section from the Portfolio page. It is now available on the Technology Portfolio page.
        -   Moved the Total Cost of Ownership \(TCO\) under the Application Portfolio on the Portfolio page.
        -   Moved the TPM Logs from the Portfolio page to the Setup page.
        -   Removed the Technology Portfolio Audit and the Technical Debt tabs from the Needs Attention section. These tabs are now available on the Technology Portfolio page.
    -   Fixed: On creating architectural artifact from a business application record, an associated artifact gets created for the business application.
-   **Version 3.2.0 - August 2024**
    -   New: Added a new navigation icon for Technology Portfolio Management
    -   Changed: The Portfolio section has been restructured and new modules and features have been added.
    -   Fixed: Performance improvement for Application Rationalization List view
-   **Version 3.1.0 - May 2024**
    -   New:
        -   Added a fiscal period filter for the Business Capability grid.
        -   Added new dashboards in EA Workspace
-   **Version 3.0.2 - March 2024**
    -   Fixed:
        -   Fixed issues caused due to removal of SAM plugin dependency
        -   Fixed bussiness application filtering issue in capability hierarchy map
-   **Version 3.0.1 - February 2024**
    -   New:
        -   View TPM and TRM lifecycle information of a business application in a Gantt chart format
        -   Evaluate the total cost of ownership \(TCO\) of a business application
        -   View the roadmap for your business capabilities and business applications
    -   Changed: Redesigned Dashboard page to show widgets in portfolio specific tabs such as Application Portfolio, Technology Portfolio, Information Portfolio, and Portfolio TCO.
    -   Fixed: Support for custom indicators in Application Rationalization.
-   **Version 2.2.1 - December 2023**

    Fixed: The error 'Duplicate group by element label\(s\)' is fixed in the Application Rationalization bubble chart view.

-   **Version 2.2.0 - November 2023**
    -   New: Rationalize your business applications by analyzing the applications by their capability, creating a demand for an application, setting the planned disposition, and adding lifecycle, demand, and project details
    -   Changed:
        -   View the unified map for a business application within the EA Workspace
        -   Access the Dashboards page from the left navigation pane instead of the EA Workspace home page
    -   Removed: The Dashboard tab is removed from the EA Workspace home page
-   **Version 2.1.0 - August 2023**
    -   Added unified map functionality for Business Applications to view the Business Applications hierarchy.
    -   Added Create Diagram feature to create Lucidchart diagrams for Business Applications and Business Capabilities.
    -   A new Setup section is added to configure your APM functionality within the EA Workspace.
    -   Request TRM Products and TRM Product Lifecycles from EA Workspace.
    -   View TRM Technical Debts in EA Workspace.
    -   Create demand in EA Workspace for a Business Application and Business Capability.
    -   New TRM widgets are added to the Dashboards page of the EA Workspace.
-   **Version 2.0.0 - May 2023**

    Added support for Technology Portfolio Management.

-   **Version 1.0.2 - February 2023**

    An intuitive user experience for Enterprise Architects to manage their application portfolio and stay up-to-date with their tasks, get insights, and monitor the health of their portfolio in one interface. Manage business portfolio with updated capability hierarchy. Configure the workspace home page for insights, scorecard, and portfolio health sections. Customize portfolio entities by grouping, filtering, and sorting.


**Parent Topic:**[ServiceNow Store - Enterprise Architecture release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-enterprise-architecture-highlights.md)

