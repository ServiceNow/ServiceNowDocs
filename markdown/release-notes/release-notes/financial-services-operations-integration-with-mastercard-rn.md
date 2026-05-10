---
title: Financial Services Operations Integration with Mastercard release notes
description: The ServiceNow Financial Services Operations Integration with Mastercard application enables financial institutions to manage the entire Mastercard dispute process. Financial Services Operations Integration with Mastercard was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Financial Services Operations Integration with Mastercard release notes

The ServiceNow® Financial Services Operations Integration with Mastercard application enables financial institutions to manage the entire Mastercard dispute process. Financial Services Operations Integration with Mastercard was enhanced and updated in the Australia release.

## Financial Services Operations Integration with Mastercard highlights for the Australia release

-   Help prevent storage or transmission of Payment Card Industry \(PCI\) data for card disputes within your ServiceNow instance by using updated subflows.
-   Streamline dispute document submission to Mastercard with the document attachment and validation enhancement.

See [Financial Services Operations Integration with Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-operations-integration-with-mastercard-landing-page.md) for more information.

**Important:** Financial Services Operations Integration with Mastercard is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **​ [Integration components for the Mastercard document attachment and validation enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-operations-integration-with-mastercard-subflows.md)**

    Simplify dispute document submission to Mastercard with improved document attachment and validation feature. The application compresses multiple attachments into a single zipped file, validates files for type and size, and alerts you to non-compliant files. This capability adds the following integration subflow and action:

    -   Mastercom - Validate and Process Attachments of Card Disputes Task
    -   Create a Zip Attachment from Uploaded Documents

## Changed in this release

-   **[Updated subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-operations-integration-with-mastercard-subflows.md)**

    The following subflows were updated to support integration with the Card data security application:

    -   Mastercom - Look up Case Documents
    -   Mastercom - Look up Chargeback Documents

-   **[Updated subflows for the Mastercard document attachment and validation enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-operations-integration-with-mastercard-subflows.md)**

    The following subflows were updated to support the document attachment and validation enhancement:

    -   Mastercom - Create Case Filing
    -   Mastercom - Create Chargeback
    -   Mastercom - Take Action on Case
    -   Mastercom - Update Chargeback

## Activation information

Install Financial Services Operations Integration with Mastercard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Financial Services Card Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-card-operations/card-ops-landing-page.md)**

    The ServiceNow® Financial Services Card Operations application digitizes and automates the card operations of your financial institution, enabling quick processing of credit card applications and card transaction disputes.

-   **[Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/integrationhub.md)**

    Automate integration tasks by using ServiceNow components for ServiceNow® Workflow Studio, or develop custom integrations. A separate subscription is required.

-   **[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/spokes-list.md)**

    Activate spokes to improve your Workflow Studio experience with integration-specific content. Use prebuilt flows and actions to automate your integrations or create your own integration automation.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

