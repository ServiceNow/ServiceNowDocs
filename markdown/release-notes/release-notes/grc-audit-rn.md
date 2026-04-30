---
title: Audit Management release notes
description: The ServiceNow Audit Management application supports activities related to planning audit engagements, implementing engagements, and reporting findings to an audit committee. Audit Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Audit Management release notes

The ServiceNow® Audit Management application supports activities related to planning audit engagements, implementing engagements, and reporting findings to an audit committee. Audit Management was enhanced and updated in the Zurich release.

## Audit Management highlights for the Zurich release

-   Set audit time frames within engagements using new audit date fields. Filter indicator results by specific periods, independent of the overall engagement time frame.
-   Access pre-configured content packs through the new Content Accelerator icon in the Audit Workspace. This includes the Digital Operational Resilience Act \(DORA\) pack with citations and authority documents.
-   Create evidence responses quickly with a simplified process.
-   Access engagements, add existing entities to an engagement, and create activities in the Lite Audit workspace, which is a simplified version of the Audit Management workspace. If the advance core store app is installed, evidences can also be associated with the engagement.

See [Audit Management](https://www.servicenow.com/docs/access?context=c_GRCAudits&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Audit Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **Audit Period Start and End Dates **

    Set audit period start and end dates directly on Engagement records to focus audits on specific time-frames. The system displays only indicator results that fall within your defined audit period, keeping the audit time-frame separate from the overall engagement time-frame. This helps you audit past or future periods without affecting the broader engagement timeline.

-   ****

    Simplify the installation of pre-configured content packs with the new Unified content management icon in the Audit Workspace. Content Accelerator includes the Digital Operational Resilience Act \(DORA\) content pack, offering citations and authority documents for DORA compliance. Audit shared manager and Audit WS supervisor roles can access Content Accelerator.

-   **[Enhancement to evidence request](https://www.servicenow.com/docs/access?context=evidence-request&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Create evidence response directly in one step. This bypasses the step involved in creation of evidence request and collection details. Evidence response is enhanced with additional data of source and context. To leverage evidence capabilities, feature roles have been introduced:

    -   sn\_grc\_advanced.evidence\_reader
    -   sn\_grc\_advanced.evidence\_requester
    -   sn\_grc\_advanced.evidence\_responder
    -   sn\_grc\_advanced.evidence\_admin
-   **[Integration with ITAM](https://www.servicenow.com/docs/access?context=solutions-gallery&version=zurich&pubname=zurich-better-together&ft:locale=en-US)**

    Leverage Audit Management support as an ITAM customer through dedicated feature roles. A lightweight version of the Audit Management workspace is available, which includes the following features:

    -   On the Audit Management home page, you can track **Timeline**, **Engagements**, **Tracking**, **Create evidence request**, and **.**
    -   The lightweight Audit Management also includes the key capabilities, such as Engagement, Entity Scoping, Activities, and Evidence when Advanced Core is installed.

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Install Audit Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

