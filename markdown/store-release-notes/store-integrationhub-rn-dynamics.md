---
title: Microsoft Dynamics CRM spoke release notes
description: Version history for the Integration Hub Microsoft Dynamics CRM spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-dynamics.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Dynamics CRM spoke release notes

Version history for the Integration Hub Microsoft Dynamics CRM spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.10.0 - June 2026**

    Security patch for non-glide ACLs

-   **Version 1.9.0 - November 2025**

    Security update: Improved system scoping privilege for better sample subflow security.

-   **Version 2.7.0 - October 2025**

    Fixed: Security defect.

-   **Version 1.7.0 - September 2025**

    Added required ACLs or Roles as per the AI Security Directive guidelines.

-   **Version 1.6.0 - March 2025**

    Added 5 conversational spoke actions and subflow samples.

-   **Version 1.5.3 - February 2025**
    -   Fixed:
        -   "Regarding" attribute in the Create Record action
        -   Scope name issue for subflow names in scripted rest api when calling sample webhook decision table
-   **Version 1.5.2 - June 2023**
    -   Fixed: Parsing the internal name of the ""Regarding"" field of Entity :'annotations' with the right value to rectify the ""undeclared property 'objectid' error.
-   **Version 1.5.1 - September 2022**

    Patch version of Microsoft Dynamics CRM Spoke for Integration Hub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 1.5.0 - February 2022**
    -   New:
        -   Added two actions:
            -   Look up Accounts Stream: Retrieve accounts details from Microsoft Dynamics CRM
            -   Look up Contacts Stream:Retrieve contacts details from Microsoft Dynamics CRM
-   **Version 1.4.0 - September 2021**

    New: This version adds a sample remote table for looking up opportunities.

-   **Version 1.3.0 - July 2021**
    -   Added a sample create opportunity flow from ServiceNow to MS Dynamics CRM
    -   Updated inbound sample subflow output with drag-n-droppable objects to make end users easier to create workflow
-   **Version 1.2.0 - June 2021**
    -   Output fields are now data pills so that customers can build the workflow much easier.
    -   Upgrade some of the actions with datastream.
    -   Consolidate and update generic create, retrieve, update, and delete records with dynamics templates and introspection
-   **Version 1.1.1 - May 2021**

    This is a patch release for the MS CRM Dynamics spoke.

-   **Version 1.0.1 - February 2020**

    Fixed an issue with payload parsing in subflows.

-   **Version 1.0.0 - November 2019**

    Initial release of Microsoft Dynamics CRM spoke for IntegrationHub.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

