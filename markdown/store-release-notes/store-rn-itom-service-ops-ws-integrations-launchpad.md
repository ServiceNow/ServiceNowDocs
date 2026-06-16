---
title: Service Operations Workspace Integrations launchpad release notes
description: Version history for the ITOM Service Operations Workspace Integrations launchpad application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-ops-ws-integrations-launchpad.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Service Operations Workspace Integrations launchpad release notes

Version history for the ITOM Service Operations Workspace Integrations launchpad application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 27.1.5 - June 2026**

    See AIOps Experience.

-   **Version 27.0.4 - April 2026**
    -   Fixed:
        -   AI Insights in Express List breaks when AIOps Experience version doesn't match Now Assist \(affects Yokohama and Zurich &lt; ZP5\).
        -   Integration Launchpad shows "No content available" after upgrading app-sow-integrations-launchpad to v27.0.3 on Yokohama.
        -   Activate with AI modal colour not rendering correctly.
        -   Grouping Automation rules cannot be saved or updated when active is set to false.
-   **Version 27.0.3 - March 2026**
    -   New:
        -   Enabled SOW UI screens for AWS CloudWatch Data Input integration
        -   Enabled SOW UI screens for AWS S3 Data Input integration
        -   Enabled SOW UI screens for Vector Data Input integration
        -   Added feature to activate with AI for data inputs integration.
    -   Changed: Enhanced overview page for push data inputs to update data input configuration.
    -   Fixed: Fixed few minor UI issues.
-   **Version 26.0.5 - December 2025**
    -   New:
        -   EdgeDelta Data Input
        -   GCP Pubsub Data Input
        -   Azure EventHub Data Input
        -   Added Mapping Context Link from Overview Page
    -   Changed:
        -   Enhanced Test and Save functionality for Pull Data Inputs
        -   Enhanced Cribl Data Input to support Credential Alias
    -   Fixed:
        -   PRB1911614 - Discrepancy in ServiceNow Docs vs Launchpad when setting up Dynatrace integration
        -   PRB1936129 - Unable to save the custom MID integration after updating the field mapping values.
        -   PRB1926046 - Improved REST API integration Set-up instruction page
        -   PRB1916918 - Cribl Data Input is incorrectly available in Xanadu
-   **Version 22.9.6 - October 2025**

    Fixed: Resolved a naming issue where some applications displayed the plugin name instead of the actual application name.

-   **Version 22.9.5 - August 2025**
    -   New:
        -   Added support for Metric Connectors from Integration Launchpad.
        -   Added support for Cribl Health Log Analytics Data Input \(Log Connector\)
        -   Added ITOM Gateway status for Ingest connectors in Overview Page of Log Connector
        -   Added minimum version requirement modal
        -   Added option to create Mid Web Server from Provide Details page of REST API Log connector.
    -   Changed:
        -   Improved Overview Page for Log Connectors
        -   Improved auto refresh of Overview page for Log Connectors
    -   Fixed:
        -   Fixed accessibility issues
        -   Fixed minor issues in overview page
        -   Cancel button on the Edit popup is unresponsive and does not close the popup when clicked
        -   Save/next button sometimes redirect user to the browse integration page
-   **Version 22.8.6 - June 2025**
    -   Fixed:
        -   PRB1884316 - Integration Launchpad not working with HLA versions prior to February.
        -   PRB1890903 - Push Connector Instance Deletion Issue Not Created via Integration Launchpad.
        -   PRB1892575 - Integration created for a Dynamic CI service in SRM has a blank "Default CI" field.
-   **Version 22.8.5 - May 2025**
    -   New:
        -   Added integrations to the following Health Log Analytics Data Inputs:
            -   REST Data Input
            -   MID Server Data Input
            -   Kafka Data Input
            -   Azure Log Analytics Data Input
        -   Added support for following components in Overview page of data input
            -   Added link for Log Viewer in Context menu
            -   Added dynamic to show the status of the data input
            -   Added calculated detection score in the overview page
    -   Fixed:
        -   Fixed performance issue with overview page
        -   Fixed translation issues
        -   Fixed accessibility issues
        -   The error message is unclear when the custom connector fails to update while in activated mode.
-   **Version 22.7.7 - February 2025**
    -   New:
        -   Added integrations to the following Health Log Analytics Data Inputs:
            -   TCP Data Input
            -   UDP Data Input
            -   Elasticsearch Data Input
            -   Glide Syslog Data Input
        -   Added an Overview page for Health Log Analytics Data Inputs to display granular integration status.
-   **Version 22.4.5 - June 2024**
    -   New:
        -   Existing integrations -&gt; related events tab health state widget
        -   The Integration health widget allows users to understand integration performance and how to improve it.
        -   Optimize integrations by monitoring their health through an overview of performance using recent events in Integration Launchpad.
        -   Realize the value or identify improvements needed for reducing the noise of alerts.
        -   Get suggestions on how to improve core aspects of alert health, including alert suppression, compression, CI binding, metric name mapping, and new alert tags.
-   **Version 22.3.2 - March 2024**
    -   New:
        -   Assigned group field for new connectors
        -   Custom connector attribute mapping from received JSONs
    -   Changed: Align logos with the Express List repository.
-   **Version 22.2.3 - February 2024**

    Small fixes.

-   **Version 22.2.1 - November 2023**

    No changes.

-   **Version 22.1.1 - August 2023**
    -   Introducing Integrations Launchpad: Streamline Your ITOM-Health Integrations
    -   Discover a revolutionary solution, Integration Launchpad, that provides a new and updated experience for viewing, configuring, and managing all your available ITOM-Health integrations. With Integrations Launchpad, you can effortlessly optimize the power of your IT Operations Management by seamlessly managing the following key components:
        -   Event Connectors: Simplify event management by leveraging a wide range of connectors tailored to your specific needs. Integrations Launchpad offers a comprehensive collection of event connectors, ensuring seamless integration and real-time visibility into your critical events.
        -   Metric Policies: Unleash the full potential of metric intelligence with our advanced metric policies. Integrations Launchpad empowers you to configure and manage metric policies, enabling proactive monitoring and accurate performance insights for your IT infrastructure.
        -   Log Data Inputs: integrate and centralize log data from various sources using Integration Launchpad. Allowing you to configure and manage log data inputs, enabling efficient log monitoring and analysis for updated troubleshooting and security.
    -   Integrations Launchpad revolutionizes the way you approach ITOM-Health integrations. With its intuitive interface and powerful features, it empowers you to streamline your operations, increase efficiency, and gain valuable insights from your IT infrastructure.

