---
title: Financial Services Operations Integration with Verifi release notes
description: The ServiceNowFinancial Services Operations Integration with Verifi application connects the Financial Services Operations \(FSO\) issuer dispute workflow to Verifi's Cardholder Dispute Resolution Network \(CDRN\) - a Visa owned pre-dispute settlement network. This integration enables issuers to automatically initiate structured negotiations with merchants before disputes escalate to costly chargebacks. Financial Services Operations Integration with Verifi is a new application in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-03"
reading_time_minutes: 2
---

# Financial Services Operations Integration with Verifi release notes

The ServiceNow®Financial Services Operations Integration with Verifi application connects the Financial Services Operations \(FSO\) issuer dispute workflow to Verifi's Cardholder Dispute Resolution Network \(CDRN\) - a Visa owned pre-dispute settlement network. This integration enables issuers to automatically initiate structured negotiations with merchants before disputes escalate to costly chargebacks. Financial Services Operations Integration with Verifi is a new application in the Australia release.

## Financial Services Operations Integration with Verifi highlights for the Australia release

-   A dispute agent proactively initiates dispute resolution without chargeback for the participating merchants.
-   System runs automated merchant eligibility check.
-   Reduced chargeback exposure for merchants.
-   Seamless API integration.

See Financial Services Operations Integration with Verifi for more information.

**Important:** Financial Services Operations Integration with Verifi is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Financial Services Operations Integration with Verifi features

-   Avoids costly chargebacks: When a merchant accepts the dispute and offers a refund that is acceptable for the cardholder, the case is closed as resolved with no chargeback initiated.
-   Automates merchant eligibility checks: The system automatically checks merchant eligibility through the Verifi CDRN API before creating a case. Non-eligible merchants are routed to the standard dispute lifecycle without agent intervention.
-   Seamless closure of disputes: Merchants participating in CDRN can respond to dispute alerts directly through Verifi .
-   Seamless API integration: The four-subflow API sequence — eligibility check, case creation, polling, and acknowledgment handshake — is fully automated and requires no manual API interaction from agents or supervisors.

## UI changes

-   Playbook actions:
    -   Create alert case
    -   Get case details
-   New fields:
    -   Pre-dispute settlement eligibility: Indicates if a merchant is eligible for a CDRN settlement.
    -   Customer decision: Indicates if a cardholder agrees or disagrees with the refund proposed by the merchant.

## Activation information

Install  by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   New plugins added in the Australia release:
    -   com.sn\_verifi\_spoke - Verifi Verifi Spoke helps streamline the card dispute resolution process by using the Verifi APIs. This integration facilitates early connections between issuers and merchants in the dispute lifecycle, which simplifies conflict resolutions at the pre-dispute stage and minimizes chargebacks.
    -   com.sn\_bom\_credit\_card - This is an application specific to card operations focused on the different customer requests in the card service domain and is part of the overall \(FSO\) product.
    -   sn\_fso\_intg\_verifi.cdrn\_bulk\_retrieval\_batch\_size - Defines the maximum number of CDRN case records that can be fetched in a single bulk retrieval call. The number is 100 by default.

## Additional requirements

The system property sn\_bom\_credit\_card.is\_verifi\_integration\_enabled must be set to true, so that it will be shipped as false out of the box.

## Related ServiceNow applications and features

-   **Financial Services Card Operations**

    The ServiceNow® Financial Services Card Operations application digitizes and automates the card operations of your financial institution, enabling quick processing of credit card applications and card transaction disputes.

-   **Integration Hub**

    Automate integration tasks by using ServiceNow components for ServiceNow® Workflow Studio, or develop custom integrations. A separate subscription is required.

-   **Integration Hub spokes**

    Activate spokes to improve your Workflow Studio experience with integration-specific content. Use prebuilt flows and actions to automate your integrations or create your own integration automation.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

