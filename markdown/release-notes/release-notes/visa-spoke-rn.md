---
title: Visa Spoke release notes
description: The ServiceNow Visa Spoke enables the ServiceNow AI Platform to connect with the Visa Resolve Online \(VROL\) API suite and Visa Stop Payment Service \(VSPS\) APIs, providing seamless access to Visa's card, payment, and dispute resolution services. Visa Spoke was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Visa Spoke release notes

The ServiceNow® Visa Spoke enables the ServiceNow AI Platform to connect with the Visa Resolve Online \(VROL\) API suite and Visa Stop Payment Service \(VSPS\) APIs, providing seamless access to Visa's card, payment, and dispute resolution services. Visa Spoke was enhanced and updated in the Yokohama release.

## Visa Spoke highlights for the Yokohama release

-   Manage card disputes with Visa Resolve Online \(VROL\) and card-on-file payments with the Visa Stop Payment Service \(VSPS\) API suite using Visa Spoke.
-   Accept and close dispute items in a queue with Visa Spoke actions.
-   Download images from an endpoint using Visa Spoke actions.
-   Handle card operations and dispute resolution services with Visa Spoke actions.

See [Visa Spoke](https://www.servicenow.com/docs/access?context=visa-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Visa Stop Payment Service \(VSPS\) integration](https://www.servicenow.com/docs/access?context=visa-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    The Visa Stop Payment Service \(VSPS\) enables Visa card issuers to stop card-on-file payments \(including recurring and installment payments\) from being authorized, cleared, and settled through VisaNet. This service helps Visa issuers handle cardholder stop payment requests.

    The following Visa Spoke actions allow clients to integrate with VSPS APIs and work through the platform:

    -   Create Stop Payment Instruction by Merchant Identifier Request Builder​
    -   Create Stop Payment Instruction by Merchant Identifier Response Parser​
    -   Create Stop Payment Instruction by PAN Request Builder​
    -   Create Stop Payment Instruction by PAN Response Parser​
    -   Create Stop Payment Instructions by Merchant Category Code Request Builder​
    -   Create Stop Payment Instructions by Merchant Category Code Response Parser​
    -   Look up Eligible Transactions for Stop Payment by PAN and Date Range Request Builder​
    -   Look up Eligible Transactions for Stop Payment by PAN and Date Range Response Parser
    -   Look up Stop Instruction Details by Stop Instruction ID Request Builder​
    -   Look up Stop Instruction Details by Stop Instruction ID Response Parser​
    -   Look up Stop Payment Instructions by PAN Request Builder​
    -   Look up Stop Payment Instructions by PAN Response Parser​
    -   Update Stop Instructions Duration by Stop Instruction ID Request Builder​
    -   Update Stop Instructions Duration by Stop Instruction ID Response Parser​
    -   Update Stop Payment Instruction by Merchant Identifier Request Builder​
    -   Update Stop Payment Instruction by Merchant Identifier Response Parser​
    -   Update Stop Payment Instruction by Merchant Category Code Request Builder​
    -   Update Stop Payment Instruction by Merchant Category Code Response Parser​
    -   Look up all linked stop payment instructions by stop instruction id Request Builder​
    -   Look up all linked stop payment instructions by stop instruction id Response Parser
    -   Look up stopped transactions by PAN Request Builder​
    -   Look up stopped transactions by PAN Response Parser​
    -   Look up stopped transactions by stop Instruction id Request Builder​
    -   Look up stopped transactions by stop Instruction id Response Parser
    -   Cancel Multiple Stop Instructions Request Builder​
    -   Cancel Multiple Stop Instructions Response Parser​

**Important:** Visa Spoke is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Changed in this release

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=visa-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#section_gsl_nw5_vyb)**

    Updated the following Visa Spoke actions to align with Visa Resolve Online \(VROL\) release 25.1 revision changes:

    -   Submit Fraud Report Request Builder
    -   Look up Fraud Report Details Response Parser
    -   Look up Dispute Response Details Response Parser
    -   Look up Dispute Details Response Parser
    -   Submit Dispute Questionnaire
-   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://www.servicenow.com/docs/access?context=visa-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#section_gsl_nw5_vyb)**

    Updated the following Visa Spoke actions to align with Visa Resolve Online \(VROL\) release 25.2 revision changes:

    -   Submit Dispute Questionnaire
    -   Hypersearch Request Builder
    -   Hypersearch Response Parser
    -   Create Dispute Pre-Arbitration Request Builder
    -   Create Dispute Pre-Arbitration Response Parser
    -   Look up Dispute Response Details Request Builder
    -   Look up Dispute Response Details Response Parser
    -   Look up Dispute Pre-Arbitration Response Details Request Builder
    -   Look up Dispute Pre-Arbitration Response Details Response Parser
    -   Look up Dispute Pre-Arbitration Details Request Builder
    -   Look up Dispute Pre-Arbitration Details Response Parser
    -   Look up Dispute Details Request Builder
    -   Look up Dispute Details Response Parser

## Activation information

Install Visa Spoke by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Automate integration tasks by using ServiceNow components for ServiceNow® Workflow Studio, or develop custom integrations. A separate subscription is required.

-   **[Integration Hub available spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Activate spokes to enhance your Workflow Studio experience with integration-specific content. Use prebuilt flows and actions to automate your integrations or create your own integration automation.

-   **[Integrating with spokes](https://www.servicenow.com/docs/access?context=spokes&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

    Integrate spokes with ServiceNow® Financial Services Operations \(FSO\) applications to enable flow designers to provide specific actions within Workflow Studio for those applications.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

