---
title: Financial Services Operations Integration with Mastercard subflows
description: You can use the following Financial Services Operations Integration with Mastercard application subflows to handle the Mastercard dispute management process.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Components installed, Mastercard, Integrate, Financial Services Operations \(FSO\)]
---

# Financial Services Operations Integration with Mastercard subflows

You can use the following Financial Services Operations Integration with Mastercard application subflows to handle the Mastercard dispute management process.

## Financial Services Operations Integration with Mastercard subflows

When an agent works on a dispute case, some actions automatically trigger related Mastercom subflows. These subflows connect to their APIs at specific touch points where the agent performs these actions in the dispute process.

|Category|Subflow|Description|API Endpoint|
|--------|-------|-----------|------------|
|Transactions|Mastercom - Look up Transaction Details|Searches for details of an original transaction using the AcquirerReferenceNumber, TransStartDate, and TransEndDate.|POST /v6/transactions/search|
|Transactions|Mastercom - Look up Authorization Transaction Details|Retrieves authorization details for a transaction linked to a claim.|GET /v6/claims/\{claim-id\}/transactions/authorization/\{transaction-id\}|
|Transactions|Mastercom - Look up Clearing Transaction Details|Retrieves clearing details for the original transaction involved in a claim, whether you're an issuer or an acquirer.|GET /v6/claims/\{claim-id\}/transactions/clearing/\{transaction-id\}|
|Fraud|Mastercom - Look up Fraud Related Information|Enables you to obtain fraud-related information that is associated with a claim before creating a fraud item for the claim.|GET /v6/claims/\{claim-id\}/fraud/loaddataforfraud|
|Fraud|Mastercom - Create Fraud Report|Creates a fraud report when identifying a transaction as fraudulent.|POST /v6/claims/\{claim-id\}/fraud/mastercard|
|Claims|Mastercom - Create Claim|Creates a new claim before submitting a retrieval request or a first chargeback.|POST /v6/claims|
|Claims|Mastercom - Look up Claim Details|Enables you to retrieve details of an existing claim.|GET /v6/claims/\{claim-id\}|
|Claims|Mastercom - Take Action on Existing Claim|Enables you to act on an existing claim, such as reopen or close it.|PUT /v6/claims/\{claim-id\}|
|Claims|Mastercom - Validate Claim Response Details|Enables you to validate that claim response details are up to date following a queue update.|GET /v6/claims/\{claim-id\}|
|Claims|Mastercom - Look up List of Claims|Enables you to retrieve claim IDs using existing case IDs related to a dispute task.|PUT /v6/cases/retrieve/claims|
|Chargebacks|Mastercom - Create Chargeback|Enables you to create a chargeback and optionally upload supporting documents.|POST /v6/claims/\{claim-id\}/chargebacks|
|Chargebacks|Mastercom - Reverse Chargeback|Enables you to reverse an existing chargeback in cases where the chargeback was created in error.|POST /v6/claims/\{claim-id\}/chargebacks/\{chargeback-id\}/reversal|
|Chargebacks|Mastercom - Acknowledge Chargeback|Enables you to acknowledge a chargeback or second presentment, moving the claim from the Unworked to the Worked queue.|PUT /v6/chargebacks/acknowledge|
|Chargebacks|Mastercom - Update Chargeback|Enables you to update an existing chargeback by adding memos or documents if omitted during initial creation.|PUT /v6/claims/\{claim-id\}/chargebacks/\{chargeback-id\}|
|Chargebacks|Mastercom - Look up Chargeback Documents Status|Enables you to check the status of documents for specific claim and chargeback IDs.|PUT v6/chargebacks/status|
|Chargebacks|Mastercom - Look up Chargeback Documents|Enables you to retrieve documents related to any chargeback in your desired format.|GET /v6/claims/\{claim-id\}/chargebacks/\{chargeback-id\}/documents|
|Chargebacks|Mastercom - Look up Chargebacks Related Information|Enables you to obtain information about a potential first chargeback before creating the chargeback.|POST /v6/claims/\{claim-id\}/chargebacks/loaddataforchargebacks|
|Chargebacks|Mastercom - Look up Chargeback Details|Enables you to retrieve chargeback details using the Get Claims API.|GET /v6/claims/\{claim-id\}|
|Chargebacks|Mastercom - Look up Second Presentment Details|Enables you to fetch second presentment details from the Get Claims API.|GET /v6/claims/\{claim-id\}|
|Case Filing|Mastercom - Create Case Filing|Enables you to file a pre-arbitration or arbitration case and optionally upload supporting documents.|POST /v6/cases|
|Case Filing|Mastercom - Take Action on Case|Enables you to take action on pre-compliance, pre-arbitration, or arbitration cases.|PUT /v6/cases/\{case-id\}|
|Case Filing|Mastercom - Look up Case Documents|Enables you to retrieve all case-related documents in the format you need.|GET /v6/cases/\{case-id\}/documents|
|Case Filing|Mastercom - Look up Case Documents Status|Enables you to check the document status for a specific list of cases.|PUT /v6/cases/status|
|Case Filing|Mastercom - Look up Case Filing Details|Enables you to fetch pre-arbitration or arbitration case filing details from the Get Claims API.|GET /v6/claims/\{claim-id\}|

## Mastercom queues

Mastercom queues help gather related dispute events all in one place, based on their lifecycle. Claims are grouped into standard queues by their common details, making them easier to find and manage.

|Queues|Description|
|------|-----------|
|Acquirer Collaboration Unworked|Contains claims with collaboration requests for the acquirer.|
|Acquirer First CB Unworked|Contains first chargeback initiated by an issuer, and any follow-up chargebacks due to rejection by First-Party Trust evidence.|
|Acquirer Worked|Contains all claims worked by an acquirer.|
|Issuer Collaboration Unworked|Contains claims for which the acquirer has provided a collaboration response.|
|Issuer Re-presentment Unworked|Contains claims for which the acquirer has provided representments as a response.|
|Issuer Worked|Contains all claims worked by an issuer.|
|Pending|Contains all claims created by an issuer with no action taken.|
|Pending Documentation|Contains all claims that need supporting documents.|
|Claims with No Activity|Contains all claims that have no associated dispute events.|
|Rejects|Contains all rejected claims or claims with rejected dispute events, either due to collaboration-related or first-party trust-related rejections.|
|Closed|Contains all closed claims.|
|Claims List|Contains all open claims.|

