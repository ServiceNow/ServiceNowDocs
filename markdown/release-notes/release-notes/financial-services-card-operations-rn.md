---
title: Financial Services Card Operations release notes
description: The ServiceNow Financial Services Card Operations application introduces a dispute playbook on the portal, enabling cardholders to initiate disputes, retrieve enriched transaction details, and receive real-time case updates through a dispute tracker. Financial Services Card Operations was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Financial Services Card Operations release notes

The ServiceNow® Financial Services Card Operations application introduces a dispute playbook on the portal, enabling cardholders to initiate disputes, retrieve enriched transaction details, and receive real-time case updates through a dispute tracker. Financial Services Card Operations was enhanced and updated in the Xanadu release.

## Financial Services Card Operations highlights for the Xanadu release

-   Enable cardholders to create and track disputes with a dispute playbook experience on the portal.
-   Enhance navigation with intuitive transitions between different role-based landing pages.
-   Permit scoped admins to modify landing pages with extensive capabilities, confirming that content aligns with the specific needs and preferences of their user base.

See [Financial Services Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US) for more information.

**Important:** [Financial Services Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Playbook enhancements for dispute](https://www.servicenow.com/docs/access?context=dispute-playbook-for-portal&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    These enhancements enable the cardholders to do the following:

    -   Initiate disputes directly through the portal by selecting your financial account and the transactions that you want to dispute.
    -   Simplify the process of initiating and tracking disputes with the user-friendly dispute portal interface.
    -   Collect detailed information about the dispute through a questionnaire on the portal.
    -   Enable cardholders to attach relevant documents to their dispute cases.
    -   Receive real-time updates on your case through the dispute tracker on the portal.
    -   Submit the dispute through the portal to land on a review page, where the agent can review and modify the details for the case as required before submitting it for investigation.
-   **[Card disputes enhancements](https://www.servicenow.com/docs/access?context=dispute-management&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**
    -   Added a common dispute questionnaire table with questions relevant to various card networks for both agents and cardholders.
    -   Moved the reason code field to the card dispute transaction table.
    -   Updated the logic to determine the reason code from the case to the card dispute transaction table.

## Changed in this release

-   **[Updated data model](https://www.servicenow.com/docs/access?context=installed-with-card-operations&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    Introduced the following two new tables for questionnaire intake:

    -   Dispute Intake \[sn\_bom\_credit\_card\_dispute\_intake\]
    -   Cardholder Dispute Intake \[sn\_bom\_credit\_card\_cardholder\_dispute\_intake\]

-   **[Updated Card disputes transaction table](https://www.servicenow.com/docs/access?context=installed-with-card-operations&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    Removed the following fields from the Card disputes case table:

    -   Account status as of transaction date
    -   Dispute amount modification reason
    -   Reason code
    -   Reason code message
    -   Suggested reason code

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=card-operations-reference&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    The domain value description for the **DisputeResponseReason** column has been updated from **Copy of ATM Cash Disbursement or Load Transaction** to **Copy of ATM Cash Disbursement**.


## UI changes

-   **[Dispute workspaces](https://www.servicenow.com/docs/access?context=dispute-workspaces&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    The updated landing pages for dispute personas feature a new visual design and improved navigation.


## Removed in this release

-   Moved the reason code for Late Presentment from the processing error decision question to the authorization category.
-   Updated the 12.1 chargeback rules to 11.3, aligning with VROL’s latest release revision 24.2.
-   Removed the **is\_parcelado** column from the dispute intake table, in alignment with VROL’s latest release revision 24.2.

## Activation information

Install Financial Services Card Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Financial Services Operations Core](https://www.servicenow.com/docs/access?context=financial-services-operations-core-data-model&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    The ServiceNow® Financial Services Operations Core stores the customer data that is required for handling card requests.

-   **[Financial Services Credit Operations](https://www.servicenow.com/docs/access?context=fso-credit-operations-landing-page&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    The ServiceNow® Financial Services Credit Operations application enables the management of credit cases and tasks that are used in ServiceNow® Financial Services Operations workflows.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Enables the extension of tables from the ServiceNow® Customer Service Management \(CSM\) application into the Financial Services Card Operations application.

-   **[Playbook capabilities](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Visualize business process workflows in a simple, task-oriented view with the Playbooks for Customer Service Management \(CSM\) to confirm consistent responses to commonly encountered situations.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

