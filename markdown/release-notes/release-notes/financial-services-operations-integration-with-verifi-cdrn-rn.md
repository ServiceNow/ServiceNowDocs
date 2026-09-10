---
title: Financial Services Operations Integration with Verifi release notes
description: The ServiceNowFinancial Services Operations Integration with Verifi application connects the Financial Services Operations \(FSO\) issuer dispute workflow to Verifi's Cardholder Dispute Resolution Network \(CDRN\) - a Visa owned pre-dispute settlement network. This integration enables issuers to automatically initiate structured negotiations with merchants before disputes escalate to costly chargebacks. Financial Services Operations Integration with Verifi is a new application in the Australia release.The ServiceNowFinancial Services Operations Integration with Verifi application connects the Financial Services Operations \(FSO\) issuer dispute workflow to Verifi's Cardholder Dispute Resolution Network \(CDRN\) - a Visa owned pre-dispute settlement network. This integration enables issuers to automatically initiate structured negotiations with merchants before disputes escalate to costly chargebacks. Financial Services Operations Integration with Verifi is a new application in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-04-03"
reading_time_minutes: 2
---

# Financial Services Operations Integration with Verifi release notes

The ServiceNow®Financial Services Operations Integration with Verifi application connects the Financial Services Operations \(FSO\) issuer dispute workflow to Verifi's Cardholder Dispute Resolution Network \(CDRN\) - a Visa owned pre-dispute settlement network. This integration enables issuers to automatically initiate structured negotiations with merchants before disputes escalate to costly chargebacks. Financial Services Operations Integration with Verifi is a new application in the Australia release.

## About Financial Services Operations Integration with Verifi

-   A dispute agent proactively initiates dispute resolution without chargeback for the participating merchants.
-   System runs automated merchant eligibility check.
-   Reduced chargeback exposure for merchants.
-   Seamless API integration.

See [Financial Services Operations Integration with Verifi](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-operations-verifi-cdrn-integration-app-landing-page.md) for more information.

## Activation and other requirements

**Important:** Financial Services Operations Integration with Verifi is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install  by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Additional requirements**

    The system property sn\_bom\_credit\_card.is\_verifi\_integration\_enabled must be set to true, so that it will be shipped as false out of the box.


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/financial-services-operations-rn-landing.md)

## Australia

The ServiceNow®Financial Services Operations Integration with Verifi application connects the Financial Services Operations \(FSO\) issuer dispute workflow to Verifi's Cardholder Dispute Resolution Network \(CDRN\) - a Visa owned pre-dispute settlement network. This integration enables issuers to automatically initiate structured negotiations with merchants before disputes escalate to costly chargebacks. Financial Services Operations Integration with Verifi is a new application in the Australia release.

### What's new

-   Avoids costly chargebacks: When a merchant accepts the dispute and offers a refund that is acceptable for the cardholder, the case is closed as resolved with no chargeback initiated.
-   Automates merchant eligibility checks: The system automatically checks merchant eligibility through the Verifi CDRN API before creating a case. Non-eligible merchants are routed to the standard dispute lifecycle without agent intervention.
-   Seamless closure of disputes: Merchants participating in CDRN can respond to dispute alerts directly through Verifi .
-   Seamless API integration: The four-subflow API sequence — eligibility check, case creation, polling, and acknowledgment handshake — is fully automated and requires no manual API interaction from agents or supervisors.

### What's changed

-   Playbook actions:
    -   Create alert case
    -   Get case details
-   New fields:
    -   Pre-dispute settlement eligibility: Indicates if a merchant is eligible for a CDRN settlement.
    -   Customer decision: Indicates if a cardholder agrees or disagrees with the refund proposed by the merchant.

-   Create alert case
-   Get case details

-   Pre-dispute settlement eligibility: Indicates if a merchant is eligible for a CDRN settlement.
-   Customer decision: Indicates if a cardholder agrees or disagrees with the refund proposed by the merchant.

