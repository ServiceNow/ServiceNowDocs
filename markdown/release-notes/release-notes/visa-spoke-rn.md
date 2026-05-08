---
title: Visa Spoke release notes
description: The ServiceNow Visa Spoke application enables the ServiceNow AI Platform to connect with the Visa Resolve Online \(VROL\) API suite and Visa Stop Payment Service \(VSPS\) APIs, providing seamless access to Visa card, payment, and dispute resolution services. Visa Spoke was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Visa Spoke release notes

The ServiceNow® Visa Spoke application enables the ServiceNow AI Platform to connect with the Visa Resolve Online \(VROL\) API suite and Visa Stop Payment Service \(VSPS\) APIs, providing seamless access to Visa card, payment, and dispute resolution services. Visa Spoke was enhanced and updated in the Australia release.

## Visa Spoke highlights for the Australia release

-   Use updated Visa Spoke APIs to help prevent storage or transmission of Payment Card Industry \(PCI\) data within ServiceNow.
-   Apply Visa Resolve Online \(VROL\) release 26.1 revision changes to some Visa Spoke actions.

See Visa Spoke for more information.

**Important:** Visa Spoke is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Changed in this release

-   **Card data security updates**

    The following spoke actions have been updated to support integration with the Card data security application:

    -   Look up Associated Transaction List
    -   Look up Image
    -   Look up Report Output
    -   Download and Attach Image
-   **VROL release 26.1 updates**

    Updated the following Visa Spoke actions to align with VROL release 26.1 revision changes. These changes support dispute agents and admins in processing disputes accurately:

    -   Submit Exception Request Builder
    -   Submit Fraud Bundle Dispute Questionnaire
    -   Look up Dispute Financial Details Request Builder
    -   Look up Dispute Financial Details Response Parser
    -   Submit Fraud Report Request Builder
    -   Look up Fraud Report Details Response Parser
    -   Look up Fraud Report Details Request Builder
    -   Look up Transaction Details Request Builder
    -   Look up Dispute Details Request Builder
    -   Look up Dispute Details Response Parser
    -   Look up Dispute Filing Details Response Parser
    -   Look up Transaction Details Response Parser
    -   Look up Transaction Details from Case Response Parser
    -   Look up All Transaction Details Response Parser
    -   Create Dispute Pre Arbitration Response
    -   Look up Dispute Pre Arbitration Details Request Builder
    -   Look up Dispute Pre Arbitration Response Details Request Builder
    -   Look up Dispute Pre Arbitration Details Response Parser
    -   Look up Dispute Response Details Request Builder
    -   Submit Dispute Questionnaire
    -   Look up Dispute Pre Arbitration Response Details Response Parser
    -   Look up Dispute Response Details Response Parser
    -       -   Initiate Dispute from Transaction or Case
    -   Create Dispute Pre Arbitration

## Activation information

Install Visa Spoke by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **Integration Hub**

    Automate integration tasks by using ServiceNow components for ServiceNow® Workflow Studio, or develop custom integrations.

-   **Integration Hub spokes**

    Activate spokes to enhance your Workflow Studio experience with integration-specific content. Use prebuilt flows and actions to automate your integrations or create your own integration automation.

-   **Integrating with spokes**

    Integrate spokes with ServiceNow® Financial Services Operations \(FSO\) applications to enable flow designers to provide specific actions within Workflow Studio for those applications.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

