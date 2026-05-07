---
title: Dispute Rules Content Pack for Mastercard release notes
description: The ServiceNow Dispute Rules Content Pack for Mastercard application provides a questionnaire for intake of dispute-related information under various dispute categories according to Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Dispute Rules Content Pack for Mastercard release notes

The ServiceNow® Dispute Rules Content Pack for Mastercard application provides a questionnaire for intake of dispute-related information under various dispute categories according to Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Australia release.

## Dispute Rules Content Pack for Mastercard highlights for the Australia release

-   Verify that dispute cases are compliant with Mastercard core rules through refined chargeback eligibility rules.
-   Streamline dispute intake process through an updated questionnaire.

See [Dispute Rules Content Pack for Mastercard](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US) for more information.

**Important:** Dispute Rules Content Pack for Mastercard is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Dispute Rules Content Pack for Mastercard to Australia

The Australia release adds 14 new data fields to the Authorization and Financial Transaction tables to support the new eligibility rules. The `transactionAmountLocal` field already exists in the Financial Transaction table but is being extended to the Financial Transaction Authorization table in this release. No other pre-existing fields are affected. After upgrading, confirm that the new fields are available and populated on your instance. For a full list of new fields, see New in this release.

## New in the Australia release

-   **[New data fields for Mastercard chargeback eligibility rules](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    New data fields sourced from the Mastercard authorization API and Mastercard clearing API have been added to support the expanded eligibility rules. Fields sourced from the Mastercard authorization API are available on the Financial Transaction Authorization table. Fields sourced from the Mastercard clearing API are available on the Financial Transaction table.

-   **[New eligibility questionnaire questions](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    New Mastercard-specific questions have been added to the chargeback eligibility questionnaire.

    For Authorization disputes \(all RC 4808 sub-categories\): A new mandatory certification statement appears in the dispute information section. It displays after the dispute amount modification reason field. Dispute agents must confirm that authorization was required for the transaction but was not properly obtained before an Authorization chargeback can proceed.

    For Consumer Dispute RC 4853 Failed Travel Merchant: Two new questions support the bond or insurance scheme reimbursement requirement:

    -   When a bond or insurance scheme exists, agents are asked what response was received from the bonding authority or insurance scheme when reimbursement was requested.
    -   When no response has been received, agents are asked to provide the date on which the reimbursement request was submitted.

## Changed in this release

-   **[Dispute Rules Content Pack for Mastercard chargeback eligibility rules updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    Determine the eligibility of a selected transaction for chargeback through chargeback eligibility rules transformed into technical formulas.

    New ineligibility conditions have been added across all five existing RC 4808 Authorization sub-categories:

    -   Required Authorization Not Obtained \(RANO\)
    -   Expired Chargeback Protection Period \(ECPP\)
    -   Stand-in or X-Code Approval after Issuer Decline \(SIXCAID\)
    -   CAT 3 Devices \(CAT3D\)
    -   Transit First Ride Risk Framework Claims \(TFRR\)
    Expanded eligibility rules for the following fraud dispute reason codes:

    -   RC 4837 \(No Cardholder Authorization\)
    -   RC 4849 \(Questionable Merchant Activity\)
    -   RC 4870 \(Chip Liability Shift\)
    -   RC 4871 \(Chip Liability Shift – Lost/Stolen/NRI Fraud\)
-   **[Dispute Rules Content Pack for Mastercard intake questionnaire updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    Benefit from the dispute questionnaire provided through Dispute Rules Content Pack for Mastercard with some modified questions and added hard stop alerts. Questionnaire questions include RC 4853 Failed Travel Merchant – Intra-EEA and Domestic European Transactions Only as an additional display condition.


## Activation information

Install Dispute Rules Content Pack for Mastercard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.

## Related ServiceNow applications and features

-   **[Financial Services Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    The ServiceNow® Financial Services Card Operations application digitizes and automates the card operations of your financial institution, enabling quick processing of credit card applications and card transaction disputes.

-   **[Financial Services Credit Operations](https://www.servicenow.com/docs/access?context=fso-credit-operations-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    The ServiceNow® Financial Services Credit Operations application enables the management of credit cases and tasks that are used in ServiceNow® Financial Services Operations workflows.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

    Enable the extension of tables from the Customer Service Management \(CSM\) application into the Financial Services Card Operations application.

-   **[Playbook capabilities](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

    Visualize business process workflows in a simple, task-oriented view with the Playbooks for Customer Service Management \(CSM\) to verify consistent responses to commonly encountered situations.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

