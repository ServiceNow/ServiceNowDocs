---
title: Operational Technology Incident Management release notes
description: The ServiceNow Operational Technology Incident Management application enables engineers to resolve Operational Technology \(OT\) device and production process issues. Operational Technology Incident Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Operational Technology Incident Management release notes

The ServiceNow® Operational Technology Incident Management application enables engineers to resolve Operational Technology \(OT\) device and production process issues. Operational Technology Incident Management was enhanced and updated in the Australia release.

## Operational Technology Incident Management highlights for the Australia release

-   Quickly understand the OT incident context and respond to user inquiries by using the OT incident summarization skill.
-   Help save time by automatically updating the resolution notes for an OT incident.
-   Generate a KB article when an OT incident is resolved by using an agentic workflow.
-   Report an OT incident without an OT incident role using the Employee Center for OT.

See Operational Technology Incident Management for more information.

**Important:** Operational Technology Incident Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **ServiceNow product tiers**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **Summarize an Operational Technology incident by using Now Assist for Operational Technology Service Management \(OTSM\)**

    Automatically summarize an OT incident using the **Summarize** UI action to produce a concise summary of the incident.

-   **Generate resolution notes for an Operational Technology incident**

    Automatically generate resolution notes for an OT incident using the **Generate resolution notes** UI action to produce a concise summary of the incident.

-   **Generate OT KB articles agentic workflow**

    Automatically generate a KB article for an OT incident when the state of the incident is set to **Resolved**. The article contains the following information:

    -   Site
    -   OT Device
    -   Equipment model entity
    -   Summarization
    -   Resolution notes
    -   KB Base
    -   Author
-   **Use the Employee Center for OT to report an OT incident**

    Create an OT incident as a user without an OT incident role with the Report OT incident item in the Employee Center for OT.


## UI changes

-   **Summarize UI action**

    The **Summarize** UI action was added to OT incident records in the Industrial Workspace so you can automatically summarize the incident details.

-   **Generate resolution notes UI action**

    The **Generate resolution notes** UI action was added to OT incident records in the Industrial Workspace so you can generate resolution notes after the incident state is set to **Resolved**.

    **Note:** This UI action appears after the OT incident state is set to **Resolved**.

-   **Catalog item for reporting an OT incident**

    The Report OT incident item has been added to the OT Service Catalog for use in the Employee Center for OT.


## Changed in this release

-   **Admin role dependency**

    Several new granular admin roles have been added, which enable developers to complete administrative configuration tasks without requiring the full admin role.


## Activation information

Install Operational Technology Incident Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **IT Service Management**

    When integrated with Operational Technology Incident Management, the ServiceNow IT Service Management application enables engineers to resolve OT device and production process issues.

-   **Industrial Process Manager**

    Use the ServiceNow Industrial Process Manager application to create the ISA-95 Equipment Model data foundation that is required for the ServiceNow Industrial solution, enabling you to create your own version of the equipment models in each of your industrial solution sites.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

