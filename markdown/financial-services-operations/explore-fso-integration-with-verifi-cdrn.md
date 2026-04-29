---
title: Exploring Financial Services Operations Integration with Verifi application
description: Learn how you can use ServiceNow Financial Services Operations Integration with Verifi application to seamlessly connect FSO's issuer dispute workflow to Verifi CDRN.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 3
keywords: [explore]
breadcrumb: [Verifi, Integrate, Financial Services Operations \(FSO\)]
---

# Exploring Financial Services Operations Integration with Verifi application

Learn how you can use ServiceNow® Financial Services Operations Integration with Verifi application to seamlessly connect FSO's issuer dispute workflow to Verifi CDRN.

## Overview of the application

Financial Services Operations Integration with Verifi lets issuers automatically negotiate with merchants before disputes move toward chargeback process. When a cardholder disputes a transaction, the issuer submits a case to CDRN, which routes it to the merchant. ServiceNow® manages the issuer-side workflow — submitting cases, polling for updates, and closing cases when the merchant responds.

## Financial Services Operations Integration with Verifi application users

<table id="table_yjh_r3f_53c"><thead><tr><th>

User

</th><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dispute agent

</td><td>

Front-line operations staff who manages cardholder dispute cases through the Financial Services Operations Integration with Verifi UI.

</td><td>

-   Review merchant alerts and determine eligibility for Verifi CDRN resolution.
-   Act on merchant responses by accepting or rejecting the proposed resolution.
-   Close dispute cases efficiently without escalating to chargeback when a valid merchant offer is available that is acceptable for the cardholder.

</td></tr><tr><td>

System administrator

</td><td>

ServiceNow platform administrator responsible for configuring and maintaining the Verifi CDRN integration.

</td><td>

-   Configure the polling interval and SLA thresholds for Verifi CDRN case monitoring.
-   Maintain the decision table that maps Verifi status codes to outcomes and descriptions.
-   Confirm the Verifi CDRN API credentials and connection settings are active and correctly configured.

</td></tr><tr><td>

Integration developer

</td><td>

Implementation partner or internal developer who configures, extends, or troubleshoot the Verifi CDRN integration.

</td><td>

-   Understand the API call sequence — eligibility check, case creation, polling, and acknowledgment handshake — to configure or extend subflows.
-   Debug failures at each API touchpoint, including HTTP 403, 409, and EXPORTING status handling.
-   Validate that the issuer acknowledgment PATCH is correctly closing cases in Verifi.

</td></tr><tr><td>

Cardholder

</td><td>

The issuer's customer who initiated the dispute.

</td><td>

-   Receive a timely resolution to their dispute.
-   Understand the outcome of the merchant's response when communicated by the agent.

</td></tr><tr><td>

Merchant

</td><td>

The retailer or service provider whose transaction is being disputed by the cardholder.

</td><td>

-   Respond to dispute alerts within the 72-hour window to avoid a chargeback.
-   Provide a resolution offer — such as a full or partial refund — that the cardholder will accept.
-   Avoid chargeback fees and protect their dispute ratio by resolving cases directly with the issuer through CDRN.

</td></tr></tbody>
</table>## Financial Services Operations Integration with Verifi application benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Dispute resolution without chargeback.|When a merchant accepts the dispute and offers a refund that is acceptable for the cardholder, the case is closed as resolved with no chargeback initiated.|Dispute agent, cardholder|
|Automated merchant eligibility check.|The system automatically checks merchant eligibility through the Verifi CDRN API before creating a case. Non-eligible merchants are routed to the standard dispute lifecycle without agent intervention.|Dispute agent|
|Reduced chargeback exposure for merchants|Merchants participating in CDRN can respond to dispute alerts directly through Verifi and offer a resolution before a chargeback is filed, protecting their dispute ratio and avoiding chargeback fees.|Merchant|
|Seamless API integration|The four-subflow API sequence — eligibility check, case creation, polling, and acknowledgment handshake — is fully automated and requires no manual API interaction from agents or supervisors.|Integration developer, system administrator|

## What to explore next

To learn more about configuring and using CDRN, see:

-   [Configuring Financial Services Operations Integration with Verifi](../task/configure-financial-services-integration-with-verifi-cdrn.md)
-   [Verifi Spoke](https://www.servicenow.com/docs/access?context=verifi-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   [Financial Services Operations Integration with Visa reference](../../fso-visa-spoke/concept/FSO-integration-with-visa-reference.md)

**Parent Topic:**[Financial Services Operations Integration with Verifi](financial-services-operations-verifi-cdrn-integration-app-landing-page.md)

