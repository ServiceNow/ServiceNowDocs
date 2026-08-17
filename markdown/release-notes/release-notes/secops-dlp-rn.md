---
title: Data Loss Prevention Incident Response release notes
description: The ServiceNow Data Loss Prevention Incident Response application helps you to manage sensitive information for your customers such as financial and proprietary data, health records, or Social Security numbers. Data Loss Prevention Incident Response was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-02-20"
reading_time_minutes: 3
---

# Data Loss Prevention Incident Response release notes

The ServiceNow® Data Loss Prevention Incident Response application helps you to manage sensitive information for your customers such as financial and proprietary data, health records, or Social Security numbers. Data Loss Prevention Incident Response was enhanced and updated in the Yokohama release.

## Data Loss Prevention Incident Response highlights for the Yokohama release

-   Enhanced the ability to securely store, manage, and track evidence files within the platform for all Data Loss Prevention Incident Response integrations.
-   Preview the evidence file of an incident from either the DLP IR analyst workspace or end user workspace.
-   Enhanced the DLP incident closure process by adding support for closure codes.
-   Introduced the Playbook feature in the DLP IR workspace to enhance operational efficiency.
-   Improved response to Data Loss Prevention \(DLP\) incidents through the initiation of SLA triggers.

See [Data Loss Prevention Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/dlp-landing.md) for more information.

**Important:** Data Loss Prevention Incident Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Create a Data Loss Prevention Incident Response SLA trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sla-records.md)**

    Enable prompt and efficient responses to incidents by creating SLA triggers.

-   **[Create a Data Loss Prevention Incident Response SLA definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/dlp-sla-definitions.md)**

    Outline the conditions and duration for responding to data breaches by creating Data Loss Prevention Incident Response SLA definitions.

-   **[Create an Application in Proofpoint and Obtain Client Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/create-application-proofpoint-dlp.md)**

    Create an application in Proofpoint and configure the required settings to obtain client credentials. These credentials enable secure access to the Proofpoint API for seamless integration and automation.

-   **[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/icap-dlp-integration.md)**

    Integration supports the ingestion of Data Loss Prevention Incident Response alerts, allows the fetching of match content, and evidence files from Amazon S3 created on the ICAP supported Data Loss Prevention Incident Response deployment.

-   **[Configure evidence file storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/configure-evidence-file-storage.md)**

    Store evidence files directly in your ServiceNow instance with Proofpoint integration, by enhancing the ability to manage and track evidence files within the platform.

-   **[Configure evidence file storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/config-evidence-file.md)**

    Symantec DLP supports evidence file storage to securely store the evidence files for the DLP Incidents.

-   **[Preview Evidence files for DLP incidents of type Exchange Online, OneDrive, and SharePoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/preview-file-dlp-microsoft.md).**

    With the DLP Microsoft integration, preview evidence files in the DLP Workspace in the Microsoft OneDrive, Microsoft Exchange Online, and Microsoft SharePoint formats. You can preview and download evidence files directly from the preview interface, simplifying evidence review and retrieval.

-   **Netskope integration: [Preview evidence files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/preview-files-netskope.md) and [Download evidence files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/download-files-netskope.md)**

    With Netskope integration you can preview and download evidence files directly from the preview interface, simplifying evidence review and retrieval.

-   **[Preview evidence files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/using-dlp-ops-portal.md)**

    Preview evidence files and download them directly from the preview interface, simplifying evidence review and retrieval.

-   **[Playbook for Data Loss Prevention Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/using-dlp-ops-portal.md)**

    Introduced playbooks in the DLP Workspace to enhance operational efficiency.

-   **[Create incident consolidation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/configure-incident-consolidation-rules-to-consolidate-your-dlp-incidents.md)**

    Parent incident is always assigned the highest priority among consolidated incidents, enhancing incident management accuracy.


## UI changes

-   **[Data Loss Prevention Incident Response Analyst Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/using-dlp-ops-portal.md)**

    Introduced a new action in the DLP incident form view that requires users to specify a closure code prior to incident closure.


## Changed in this release

-   **[Create additional incident data fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/create-custom-fields-dlp.md)**

    In the DLP incident table, the **Custom Fields** column has been renamed **Additional Incident Data Fields**.


## Activation information

Install Data Loss Prevention Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **[Security Operations common functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sec-ops-common-functionality.md)**

    The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


## Related ServiceNow applications and features

-   **[Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sir-landing-page.md)**

    The ServiceNow® Security Incident Response application tracks the progress of security incidents from discovery and initial analysis, through containment, eradication, and recovery, and into the final post incident review, knowledge base article creation, and closure.


**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/security-operations-rn-landing.md)

