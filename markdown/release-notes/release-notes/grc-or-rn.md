---
title: Operational Resilience release notes
description: The ServiceNow Operational Resilience application supports organizations to help keep business services running during adverse events like pandemics, severe weather, or cyber attacks. Operational Resilience was enhanced and updated in the Zurich release.The ServiceNow Operational Resilience application supports organizations to help keep business services running during adverse events like pandemics, severe weather, or cyber attacks. Operational Resilience was enhanced and updated in the Zurich release.The ServiceNow Operational Resilience application supports organizations to help keep business services running during adverse events like pandemics, severe weather, or cyber attacks. Operational Resilience was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 8
---

# Operational Resilience release notes

The ServiceNow® Operational Resilience application supports organizations to help keep business services running during adverse events like pandemics, severe weather, or cyber attacks. Operational Resilience was enhanced and updated in the Zurich release.

## About Operational Resilience

-   Set up the nexus map configurations and use the interactive node map view to define dependencies and relationships between records.
-   Generate a Microsoft Word document for the action tasks in Digital resilience incident reporting.
-   Create DIR cases for multiple regulations from either an incident or a security incident report. You can map entities to regulations and configure the Smart Assessment Engine \(SAE\) template for each regulation within the regulatory agency profile.
-   Generate and validate regulator-ready Register of Information \(RoI\) packages for EU DORA compliance.
-   Use the enhanced fix scripts in the Common Service Data Model for improved Operational Resilience metrics.
-   Evaluate the importance and impact tolerance of services and self-attest their status by using Smart Assessment.

See [Operational Resilience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/grc-opres-landing-page.md) for more information.

## Activation and other requirements

**Important:** Operational Resilience is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    After upgrading to Operational Resilience version 21.0.x, rerun the **Update CSDM and other dependencies** scheduled job to populate the additional metadata that was introduced in this release.

-   **Browser requirements**

    Operational Resilience requires the following browsers:

    -   Google Chrome
    -   Firefox and Firefox Extended Support Release \(ESR\)
    -   Microsoft Edge Chromium
    -   Safari 12.0 and later versions

## Accessibility and localization

-   **Accessibility information**
    -   **Dark theme**

        The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/grc-rn-landing.md)

## December 2025

The ServiceNow® Operational Resilience application supports organizations to help keep business services running during adverse events like pandemics, severe weather, or cyber attacks. Operational Resilience was enhanced and updated in the Zurich release.

### What's new

-   **[Use the interactive Node Map visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/configure-nexus-map-configurations.md)**

    Navigate operational dependencies using the interactive Node map visualization. Configure node and edge settings in the Nexus map, then display Main node configurations directly within the Operational Resilience Workspace. The **Resilience map** action provides access to relationships for Business Services \(BS\), Application Services \(AS\), Supporting Offerings \(SO\), Business Processes \(BP\), and Dependencies modules in the map view.

    You can configure node dependency directions and enhance visual elements with improved colors and icons for clarity. Additionally, you can gain comprehensive insights from the summary panel and address missing 'red flags' for a complete picture.

-   **[Generate Word reports of action tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/gen-word-reports.md)**

    Use the Document designer to set up Microsoft Word templates and download action task reports in Digital resilience incident reporting. This functionality enables you to customize predefined templates or create templates, incorporating specific data like tables and columns from records, to generate intuitive, audit-ready reports. You can then save these reports within the ServiceNow® instance or as cloud documents in Microsoft SharePoint.

-   **[Report incidents associated with multiple regulations for various legal entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/reporting-for-multiple-regulations.md)**

    Report incidents or security incidents associated with multiple regulations for various legal entities in Digital resilience incident reporting. Its automated workflow generates regulatory reporting assessment of IT incidents, DRI Initial report, DRI Intermediate report, and DRI Final report within regulatory timelines, each with dedicated action tasks. You can complete these tasks and generate reports in Microsoft Word format required by regulatory authorities for analysis.

-   **[Generate Register of Information \(RoI\) regulatory packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/opres-dora-roi-reg-pkg.md)**

    Generate regulator-ready Register of Information \(RoI\) regulatory packages using the Plain-CSV Report Package option on the download page in Digital resilience third-party registers. The resulting ZIP file, structured to regulator specifications, includes metadata and report folders with file names containing LEI, entity ID, and release version.

    This format helps you to verify EU DORA compliance and supports automated validation workflows. For suggested steps and permissions, refer to the user guide on the Download and Upload request page.

-   **[Validate downloaded Register of Information regulatory packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/opres-dora-validate-roi.md)**

    Validate downloaded Register of Information \(RoI\) regulatory packages against requirements using the Plain-CSV Report Package option on the Digital resilience third-party registers download page. This process verifies file format, structure, encoding, naming conventions, and field-level data across multiple tables.

    If validation warnings are detected, an automated report is attached, mapping issues to regulator fields like Template Code, Row Code, and Column Code. These reports include real-world field labels, rule expressions, and record identifiers. You can easily cross-reference validation errors using a downloadable Excel template that mirrors the CSV structure, simplifying issue location and resolution. Further enhancements include support for 'Not applicable' values, enforced file size limits, and clearer error messages for malformed data.


### What's changed

-   **[Main node configurations: A component of the Data Relationships Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/main-node-relationship-fw.md)**

    The properties, related lists, and copy functionality in the Main node configurations form are updated.

-   **[Configure the Nexus map configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/configure-nexus-map-configurations.md)**

    The Nexus map configuration settings are added.

-   **[Node configurations and Node status configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/configure-node-configurations.md)**

    The Node configurations and Node status configurations related lists are added.

-   **[Edge configurations and edge status configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/configure-edge-configurations.md)**

    The Edge configurations and Edge status configurations related lists are added.

-   **[Interacting with the Nexus map UI from the Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/interacting-with-nexus-map-ui-from-worksapce.md)**

    The **Resilience map** UI action is added to display the map view for a service record.

-   **[Word reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/reporting-for-multiple-regulations.md)**

    The 'Template Configurations' module displays the document design template configuration details of DIR action tasks. The 'Word Templates' module provides the DIR Word templates used to generate Microsoft Word reports.

-   **[Regulation mappings related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/workflow-confi-auto-trigger-inci-repo-cases.md)**

    The 'Digital Resilience Incident Case Type' module displays the ‘Digital Resilience Incident Case.’ The Regulation Mappings related list in the record shows the relationships between entities and their corresponding regulations.

-   **[Download the Excel template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-excel-upload-download-request.md)**

    The option to download the Third-party Information Register is renamed to Excel Master Template.


## Zurich

The ServiceNow® Operational Resilience application supports organizations to help keep business services running during adverse events like pandemics, severe weather, or cyber attacks. Operational Resilience was enhanced and updated in the Zurich release.

### What's new

-   **[Improve resilience metrics with the enhanced CSDM model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/using-csdm-v5.md)**

    Leverage the enhanced fix scripts in the Common Service Data Model \(CSDM\) to enhance your Operational Resilience metrics. Each node in the hierarchy is now stored separately, with its class and parent nodes, to help you manage your data more efficiently.

    The **Update CSDM and other dependencies** scheduled job script has been optimized to process the main node configurations in parallel, triggering a separate event for each node. Any node can be at the top level. Additionally, you can store impacted objects, including all parents, in a single table, so that you can efficiently retrieve children nodes and improve your data retrieval.

    Configure the **sn\_oper\_res.top\_class\_name** property to designate any class as the top class. You can view the downstream data and various dashboards based on the selected top class, such as the number of application services that are under a business service.

-   **[Analyze importance and impact tolerance of a service using Smart Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-an-assessment-for-services-in-ws.md)**

    Analyze a service's importance and impact tolerance through flexible assessments by using one or multiple Smart Assessment templates. Role-based access controls and auto-assigned tasks help you to streamline the process. You can reopen and complete assessments as needed and send email notifications to relevant users.

-   **[Generate customized and flexible self-attestation reports using Smart Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-new-attestation-in-ws.md)**

    Generate customized and flexible self-attestation reports by using Smart Assessment. Start with the default template, add relevant scopes and users, and generate a PDF report on completion of the self-attestation process. By creating custom templates with various data types, you make the self-attestation process more efficient.

-   **[Leverage enhanced DORA capabilities for contracts, supply chains, and assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-drtp-reg-contract.md)**

    Use the enhanced Digital Operational Resilience Act \(DORA\) data model in Operational Resilience. You can configure contracts based on their supply chains and assessments, upload the contract records, and generate a detailed report in Microsoft Excel that provides information on the entities, third parties, and specific contract details.

-   **[Track third-party risk assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/opres-ws-homepage-overview.md)**

    Track third-party risk assessments as red flags in Operational Resilience reports and overview pages for business services, service offerings, and business processes. Operational Resilience users, managers, and administrators can review these assessments in Operational Resilience Workspace. The sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer role is now included in the sn\_oper\_res.user role, so that you can grant the necessary access to the assessments.


### What's changed

-   **[Action tasks configuration related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/work-on-action-tasks.md)**

    Action tasks configuration related list is used to set up contextual information for different regulations. This includes the assessment template, assignment group, trigger conditions, due dates, and more.

-   **[New modules and layout for Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/using-csdm-v5.md)**

    The Application services module is added to the list view, which enables you to configure application services.A vertical layout is added for the Services, Business services, Offerings, Business processes, and Application services modules.In the CSDM objects table, the Impacted objects column displays the parent objects, while the Impacted objects classes column shows the classes. The Red flags count column indicates the number of the red flags that are directly assigned to a node, and the Total red flags count column displays the total count of the red flags directly assigned to a node and its children.

-   **[Contracts and related tabs for DORA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-drtp-reg-contract.md)**

    The related tabs for the contracts, including associated entities and third parties, are now shown in the Contract record forms.

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


### What's deprecated or removed

The Operational Resilience application previously stored the entire dependency chain in the \[sn\_oper\_res\_profile\] table, which resulted in redundant data and potential performance issues. The **Update CSDM and other dependencies** scheduled job script has been optimized to address this issue. Any node can now be at the top level. Data retrieval is more efficient because you can store the impacted objects in a single table.

