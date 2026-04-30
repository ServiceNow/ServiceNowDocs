---
title: Dispute Rules Content Pack for Visa release notes
description: The ServiceNow Dispute Rules Content Pack for Visa application enables issuers to access Visa card network rules for initiating and investigating card dispute cases. Dispute Rules Content Pack for Visa was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Dispute Rules Content Pack for Visa release notes

The ServiceNow® Dispute Rules Content Pack for Visa application enables issuers to access Visa card network rules for initiating and investigating card dispute cases. Dispute Rules Content Pack for Visa was enhanced and updated in the Xanadu release.

## Dispute Rules Content Pack for Visa highlights for the Xanadu release

-   Optimize the chargeback process by identifying eligibility immediately, prior to submitting the dispute to the card payment network.
-   Avoid penalties by identifying ineligible transactions that are based on the reason code and transaction data.

See [Dispute Rules Content Pack for Visa](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US) for more information.

**Important:** Dispute Rules Content Pack for Visa is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Changed in this release

-   **[Questionnaire and chargeback eligibility ruless](https://www.servicenow.com/docs/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**
    -   Added new chargeback eligibility rules to reflect the latest dispute conditions from Visa.
    -   Updated the dispute questionnaire to support the following reason codes:
        -   10.3 \(Other fraud—card-present environment\)
        -   13.1 \(Merchandise/services not received\)
        -   13.5 \(Misrepresentation\)
-   **[Visa Resolve Online \(VROL\) 24.2 revision Alignment](https://www.servicenow.com/docs/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**
    -   Updated chargeback reason codes and dispute questionnaire with VROL's latest release revision 24.2.
    -   Updated 12.1 chargeback rules to 11.3.
-   **[Visa Resolve Online \(VROL\) 25.2 revision Alignment](https://www.servicenow.com/docs/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    The chargeback eligibility rule under the 12.6 reason code that validates **Is the other transaction paid by other means? == N** has been removed,

-   **[Updated references in Card Operations tables](https://www.servicenow.com/docs/access?context=components-installed-with-dispute-rules-content-pack-for-visa&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    Updated references from the old questionnaire tables to the new intake tables in Card Operations.

-   **[Updated data model](https://www.servicenow.com/docs/access?context=dispute-data-model&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**
    -   Enhanced Dispute Rules Content Pack for Visa to support the updated chargeback eligibility conditions and the fields used for validating disputed transactions.
    -   Moved the following tables as generic intake tables, from Dispute Rules Content Pack for Visa \[sn\_bom\_visa\_cp\] to Financial Services Card Operations \[sn\_bom\_credit\_card\]:
        -   Visa Dispute Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\] → Dispute Intake \[sn\_bom\_credit\_card\_dispute\_intake\]
        -   Visa Dispute Cardholder Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_cardholder\_intake\] → Cardholder Dispute Intake \[sn\_bom\_credit\_card\_cardholder\_dispute\_intake\]

            **Note:** These tables have been moved only for new customers, but they are still available in the Dispute Rules Content Pack for Visa for existing customers.


## Activation information

Install Dispute Rules Content Pack for Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Financial Services Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    The ServiceNow® Financial Services Card Operations application digitizes and automates the card operations of your financial institution, enabling quick processing of credit card applications and card transaction disputes.

-   **[Financial Services Credit Operations](https://www.servicenow.com/docs/access?context=fso-credit-operations-landing-page&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

    The ServiceNow® Financial Services Credit Operations application enables the management of credit cases and tasks that are used in ServiceNow® Financial Services Operations workflows.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Enables the extension of tables from the Customer Service Management \(CSM\) application into the Financial Services Card Operations application.

-   **[Playbook capabilities](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Visualize business process workflows in a simple, task-oriented view with the Playbooks for Customer Service Management \(CSM\) to confirm consistent responses to commonly encountered situations.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

