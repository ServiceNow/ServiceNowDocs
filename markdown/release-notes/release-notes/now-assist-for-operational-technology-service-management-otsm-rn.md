---
title: ServiceNow Otto for Operational Technology \(OT\) Service Management release notes
description: The ServiceNow ServiceNow Otto for Operational Technology \(OT\) Service Management application enables you to summarize Operational Technology \(OT\) incident information and generate incident resolution notes. ServiceNow Otto for OT Service Management is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-07-20"
reading_time_minutes: 3
---

# ServiceNow Otto for Operational Technology \(OT\) Service Management release notes

The ServiceNow® ServiceNow Otto for Operational Technology \(OT\) Service Management application enables you to summarize Operational Technology \(OT\) incident information and generate incident resolution notes. ServiceNow Otto for OT Service Management is a new application in the Zurich release.

## Now Assist &gt; ServiceNow Otto announcement

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

## ServiceNow Otto for OT Service Management highlights for the Zurich release

[Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)

-   Now Assist for Operational Technology Service Management \(OTSM\) has been changed to ServiceNow Otto for OT Service Management.

[Zurich Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11.md)

-   The Now LLM Service is no longer the default model provider for new or inactive AI assets.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Quickly understand the OT incident context and respond to user inquiries by using the OT incident summarization skill.
-   Help save time by automatically updating the resolution notes for an OT incident.
-   Generate a KB article when an OT incident is resolved by using an agentic workflow.

See [ServiceNow Otto for Operational Technology \(OT\) Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-for-operational-technology-service-management.md) for more information.

**Important:** ServiceNow Otto for OT Service Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## ServiceNow Otto for OT Service Management features

-   **[Now LLM service deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[Summarize an OT incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/summarize-ot-incident-now-assist.md)**

    Automatically summarize an OT incident using the **Summarize** UI action to produce a concise summary of the incident.

-   **[Generate resolution notes for an Operational Technology incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/generate-resolution-notes-ot-incident.md)**

    Automatically generate resolution notes for an OT incident using the **Generate resolution notes** UI action to produce a concise summary of the incident.

-   **[Generate OT KB articles agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/agent-ot-knowledge-generator.md)**

    Automatically generate a KB article for an OT incident when the state of the incident is set to **Resolved**. The article contains the following information:

    -   Site
    -   OT Device
    -   Equipment model entity
    -   Summarization
    -   Resolution notes
    -   KB Base
    -   Author

## UI changes

-   **[Summarize UI action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/summarize-ot-incident-now-assist.md)**

    The **Summarize** UI action was added to OT incident records in the Industrial Workspace so you can automatically summarize the incident details.

-   **[Generate resolution notes UI action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/generate-resolution-notes-ot-incident.md)**

    The **Generate resolution notes** UI action was added to OT incident records in the Industrial Workspace so you can generate resolution notes after the incident state is set to **Resolved**.

    **Note:** This UI action appears after the OT incident state is set to **Resolved**.


## Changed in this release

-   **[Now Assist for OTSM to ServiceNow Otto for OT Service Management name change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-for-operational-technology-service-management.md)**

    ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Now Assist for OTSM. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


## Activation information

Install ServiceNow Otto for OT Service Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugins are new in Zurich:

    ServiceNow Otto for OT Service Management \(com.sn\_otsm\_gen\_ai\): Contains the features, AI agents, and agentic workflows for ServiceNow Otto for OT Service Management.


## Related ServiceNow applications and features

-   **[Operational Technology Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/operational-technology-incident-management-landing-page.md)**

    The ServiceNow® Operational Technology Incident Management application enables engineers to resolve Operational Technology \(OT\) device and production process issues quickly.


**Parent Topic:**[Operational Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/operational-technology-rn-landing.md)

