---
title: Financial Services Operations Integration with Mastercard subflows
description: You can use the following Financial Services Operations Integration with Mastercard application subflows to handle the Mastercard dispute management process.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Components installed, Reference, Mastercard, Integrate, Financial Services Operations \(FSO\)]
---

# Financial Services Operations Integration with Mastercard subflows

You can use the following Financial Services Operations Integration with Mastercard application subflows to handle the Mastercard dispute management process.

## Financial Services Operations Integration with Mastercard subflows

When an agent works on a dispute case, some actions automatically trigger related Mastercom subflows. These subflows connect to their APIs at specific touch points where the agent performs these actions in the dispute process.

<table id="table_dhl_l1k_wfc"><thead><tr><th>

Subflow

</th><th>

Description

</th><th>

API Endpoint

</th><th>

Touch point

</th></tr></thead><tbody><tr><td>

Mastercom - Look up Transaction Details

</td><td>

Searches for details of an original transaction using the AcquirerReferenceNumber, TransStartDate, and TransEndDate.

</td><td>

POST/v6/transactions/search

</td><td>

-   **Initiate** stage:
    -   The agent creates a dispute case for the initial transaction.
    -   The agent creates a dispute case for more transactions in the **Add more transactions** activity and selects **Continue**.
-   **Review** stage:

The agent adds more transactions to a dispute case that the cardholder or the contributor created and selects **Continue**.


</td></tr><tr><td>

Mastercom - Look up Authorization Transaction Details

</td><td>

Retrieves authorization details for a transaction linked to a claim.

</td><td>

GET/v6/claims/\{claim-id\}/transactions/authorization/\{transaction-id\}

</td><td>

-   **Initiate** stage:
    -   The agent creates a dispute case for the initial transaction.
    -   The agent creates a dispute case for more transactions in the **Add more transactions** activity and selects **Continue**.
-   **Review** stage:

The agent adds more transactions to a dispute case that the cardholder or the contributor created and selects **Continue**.


</td></tr><tr><td>

Mastercom - Look up Clearing Transaction Details

</td><td>

Retrieves clearing details for the original transaction involved in a claim, whether you're an issuer or an acquirer.

</td><td>

GET /v6/claims/\{claim-id\}/transactions/clearing/\{transaction-id\}

</td><td>

-   **Initiate** stage:
    -   The agent creates a dispute case for the initial transaction.
    -   The agent creates a dispute case for more transactions in the **Add more transactions** activity and selects **Continue**.
-   **Review** stage:

The agent adds more transactions to a dispute case that the cardholder or the contributor created and selects **Continue**.

-   **Investigate** stage:

The agent works on a **Report fraud for card network** task that displays only the claim ID without other claim details.


</td></tr><tr><td>

Mastercom - Look up Fraud Related Information

</td><td>

Enables you to obtain fraud-related information that is associated with a claim before creating a fraud item for the claim.

</td><td>

GET /v6/claims/\{claim-id\}/fraud/loaddataforfraud

</td><td>

**Initiate** stage:-   The agent creates a dispute case for a single transaction and completes the **Fill dispute questionnaire** activity.
-   The agent creates a dispute case for multiple transactions and completes the **Fill additional dispute questionnaire** activity.

</td></tr><tr><td>

Mastercom - Create Fraud Report

</td><td>

Creates a fraud report when identifying a transaction as fraudulent.

</td><td>

POST /v6/claims/\{claim-id\}/fraud/mastercard

</td><td>

**Investigate** stage:The agent works on a **Report fraud for card network** task.

</td></tr><tr><td>

Mastercom - Create Claim

</td><td>

Creates a new claim before submitting a retrieval request or a first chargeback.

</td><td>

POST /v6/claims

</td><td>

-   **Initiate** stage:
    -   The agent creates a dispute case for the initial transaction.
    -   The agent creates a dispute case for more transactions in the **Add more transactions** activity and selects **Continue**.
-   **Review** stage:

The agent adds more transactions to a dispute case that the cardholder or the contributor created and selects **Continue**.

-   **Investigate** stage:

The agent works on a **Report fraud for card network** task that displays the claim ID.


</td></tr><tr><td>

Mastercom - Look up Chargeback Details

</td><td>

Enables you to retrieve chargeback details using the Get Claims API.

</td><td>

GET /v6/claims/\{claim-id\}

</td><td>

**Chargeback** stage: This subflow runs when the queue API confirms that a response is available after:

-   The agent submits a chargeback request.
-   The agent escalates the transaction chargeback through a pre-arbitration or arbitration request.

</td></tr><tr><td>

Mastercom - Look up Second Presentment Details

</td><td>

Enables you to fetch second presentment details from the Get Claims API.

</td><td>

GET /v6/claims/\{claim-id\}

</td><td>

**Chargeback** stage: This subflow runs when the queue API confirms that a response is available after:

-   The agent submits a chargeback request.
-   The agent escalates the transaction chargeback through a pre-arbitration or arbitration request.

</td></tr><tr><td>

Mastercom - Look up Case Filing Details

</td><td>

Enables you to fetch pre-arbitration or arbitration case filing details from the Get Claims API.

</td><td>

GET /v6/claims/\{claim-id\}

</td><td>

**Chargeback** stage: This subflow runs when the queue API confirms that a response is available after:

-   The agent submits a chargeback request.
-   The agent escalates the transaction chargeback through a pre-arbitration or arbitration request.

</td></tr><tr><td>

Mastercom - Validate Claim Response Details

</td><td>

Enables you to validate that claim response details are up to date following a queue update.

</td><td>

GET /v6/claims/\{claim-id\}

</td><td>

**Chargeback** stage: This subflow runs when the queue API confirms that a response is available after:

-   The agent submits a chargeback request.
-   The agent escalates the transaction chargeback through a pre-arbitration or arbitration request.

</td></tr><tr><td>

Mastercom – Take Action on Existing Claim

</td><td>

Enables you to act on an existing claim, such as reopen or close it.

</td><td>

PUT /v6/claims/\{claim-id\}

</td><td>

The agent reopens a claim that was previously closed in the following stages: -   **Investigate** stage:

The agent submits a fraud report by selecting the **Submit fraud** button in the **Report fraud for card network** task.

-   **Chargeback** stage:

The agent submits a chargeback request by selecting the **Initiate chargeback** button in the **Initiate chargeback and recover funds from merchant** task.


</td></tr><tr><td>

Mastercom - Look up Claim Details

</td><td>

Enables you to retrieve details of an existing claim.

</td><td>

GET /v6/claims/\{claim-id\}

</td><td>

The agent reopens a claim that was previously closed in the following stages: -   **Investigate** stage:

The agent submits a fraud report by selecting the **Submit fraud** button in the **Report fraud for card network** task.

-   **Chargeback** stage:

The agent submits a chargeback request by selecting the **Initiate chargeback** button in the **Initiate chargeback and recover funds from merchant** task.


</td></tr><tr><td>

Mastercom - Create Chargeback

</td><td>

Enables you to create a chargeback and optionally upload supporting documents.

</td><td>

POST /v6/claims/\{claim-id\}/chargebacks

</td><td>

**Chargeback** stage:The agent starts a chargeback request by selecting the **Initiate chargeback** button in the **Initiate chargeback and recover funds from merchant** task.

</td></tr><tr><td>

Mastercom - Reverse Chargeback

</td><td>

Enables you to reverse an existing chargeback in cases where the chargeback was created in error.

</td><td>

POST /v6/claims/\{claim-id\}/chargebacks/\{chargeback-id\}/reversal

</td><td>

**Chargeback** stage:The agent reverses a chargeback request after submitting it by selecting the **Reverse** button in the **Initiate chargeback and recover funds from merchant** task.

</td></tr><tr><td>

Mastercom - Acknowledge Chargeback

</td><td>

Enables you to acknowledge a chargeback or second presentment, moving the claim from the Unworked to the Worked queue.

</td><td>

PUT /v6/chargebacks/acknowledge

</td><td>

This subflow does not have a direct user interface or trigger point.

 The system processes this through queues to clear the second presentment queue. It identifies whether the process has already progressed beyond the second presentment stage by checking if the second presentment details have been retrieved.

</td></tr><tr><td>

Mastercom - Update Chargeback

</td><td>

Enables you to update an existing chargeback by adding memos or documents if omitted during initial creation.

</td><td>

PUT /v6/claims/\{claim-id\}/chargebacks/\{chargeback-id\}

</td><td>

**Chargeback** stage:The agent receives an error message when uploading supporting documents in any of these tasks: **Initiate chargeback and recover funds from merchant**, **Review and respond to collaboration**, or **Review chargeback response and decide on pre-arbitration or arbitration**.

</td></tr><tr><td>

Mastercom - Look up Chargeback Documents Status

</td><td>

Enables you to check the status of documents for specific claim and chargeback IDs.

</td><td>

PUT v6/chargebacks/status

</td><td>

**Chargeback** stage:This subflow works with the Mastercom - Look up Chargeback Documents subflow when a merchant submits a second presentment request.

During the **Review chargeback response and decide on pre-arbitration or arbitration** task, the system fetches the second presentment details and this subflow runs to verify the status of attached supporting documents.

If the document status shows as Complete, the Mastercom - Look up Chargeback Documents subflow runs to retrieve the document.

When an issuer uploads supporting documents, this subflow also runs to retrieve the document status.

</td></tr><tr><td>

Mastercom - Look up Chargeback Documents

</td><td>

Enables you to retrieve documents related to any chargeback in your desired format.

</td><td>

GET /v6/claims/\{claim-id\}/chargebacks/\{chargeback-id\}/documents

</td><td>

**Chargeback** stage:This subflow works with the Mastercom - Look up Chargeback Documents Status subflow when a merchant submits a second presentment request.

During the **Review chargeback response and decide on pre-arbitration or arbitration** task, the system fetches the second presentment details. The Mastercom - Look up Chargeback Documents Status subflow then runs to verify the status of attached supporting documents.

If the document status shows as Complete, this subflow runs to retrieve the document.

</td></tr><tr><td>

Mastercom - Look up Chargebacks Related Information

</td><td>

Enables you to obtain information about a potential first chargeback before creating the chargeback.

</td><td>

POST /v6/claims/\{claim-id\}/chargebacks/loaddataforchargebacks

</td><td>

**Dispute Intake** stage:This subflow runs when the dispute intake form loads.

</td></tr><tr><td>

Mastercom - Process Pending Documentation Queue

</td><td>

Enables you to track the document status for chargebacks in the pending documentation queue.

</td><td>

POST /v6/queues

</td><td>

This subflow does not have a direct user interface or trigger point.

 It runs in the back-end as a scheduled job to monitor activities from the Mastercard server.

</td></tr><tr><td>

Mastercom - Process Issuer Worked Queue

</td><td>

Enables you to confirm that chargeback documents were successfully processed and the claim advanced from the PendingDocumentation queue.

</td><td>

POST /v6/queues

</td><td>

This subflow does not have a direct user interface or trigger point.

 It runs in the back-end as a scheduled job to monitor activities from the Mastercard server.

</td></tr><tr><td>

Mastercom - Process Reject Queue

</td><td>

Enables you to monitor rejections that occurred during the initial chargeback creation process.

</td><td>

POST /v6/queues

</td><td>

This subflow does not have a direct user interface or trigger point.

 It runs in the back-end as a scheduled job to monitor activities from the Mastercard server.

</td></tr><tr><td>

Mastercom - Process Issuer Re-presentment Unworked Queue

</td><td>

Enables you to retrieve claims where an acquirer submitted a representment in response to a chargeback.

</td><td>

POST /v6/queues

</td><td>

This subflow does not have a direct user interface or trigger point.

 It runs in the back-end as a scheduled job to monitor activities from the Mastercard server.

</td></tr><tr><td>

Mastercom - Process Sender Case Filing Queue

</td><td>

Enables you to track dispute updates from pre-arbitration through the full case lifecycle.

</td><td>

POST /v6/queues

</td><td>

This subflow does not have a direct user interface or trigger point.

 It runs in the backend as a scheduled job to monitor activities from the Mastercard server.

</td></tr><tr><td>

Mastercom - Process Pending Queue

</td><td>

Enables you to track second presentment reversals in the pending queue.

</td><td>

POST /v6/queues

</td><td>

This subflow does not have a direct user interface or trigger point.

 It runs in the backend as a scheduled job to monitor activities from the Mastercard server.

</td></tr><tr><td>

Mastercom - Create Case Filing

</td><td>

Enables you to file a pre-arbitration or arbitration case and optionally upload supporting documents.

</td><td>

POST /v6/cases

</td><td>

**Chargeback** stage:The agent files a dispute case by selecting either the **Create pre arbitration** button or the **Create arbitration** button in the **Review chargeback response and decide on pre-arbitration or arbitration** task.

</td></tr><tr><td>

Mastercom - Take Action on Case

</td><td>

Enables you to take action on pre-compliance, pre-arbitration, or arbitration cases.

</td><td>

PUT /v6/cases/\{case-id\}

</td><td>

**Chargeback** stage:-   The agent escalates the pre-arbitration request to arbitration by selecting the **Escalate to arbitration** button in the **Review pre-arbitration response and escalate to arbitration** task.
-   The agent withdraws a pre-arbitration or arbitration case by selecting the **Withdraw case** button in either the **Review chargeback response and decide on pre-arbitration or arbitration** task or the **Review pre-arbitration response and escalate to arbitration** task.
-   The agent reuploads the supporting documents for a dispute case by selecting the **Upload document** button in either the **Review pre-arbitration response and escalate to arbitration** task or the **Review arbitration response** task.

</td></tr><tr><td>

Mastercom - Look up Case Documents

</td><td>

Enables you to retrieve all case-related documents in the format you need.

</td><td>

GET /v6/cases/\{case-id\}/documents

</td><td>

**Chargeback** stage:This subflow works with the Mastercom - Look up Case Documents Status subflow when the agent submits a pre-arbitration or arbitration request.

During the **Review pre-arbitration response and escalate to arbitration** and **Review arbitration response** tasks, the system fetches the pre-arbitration or arbitration details. The Mastercom - Look up Case Documents Status subflow then runs to verify the status of the pre-arbitration or arbitration response document.

If the document status shows as Complete, this subflow runs to retrieve the document.

</td></tr><tr><td>

Mastercom - Look up Case Documents Status

</td><td>

Enables you to check the document status for a specific list of cases.

</td><td>

PUT/v6/cases/status

</td><td>

**Chargeback** stage:This subflow works with the Mastercom - Look up Case Documents subflow when the agent submits a pre-arbitration or arbitration request.

During the **Review pre-arbitration response and escalate to arbitration** and **Review arbitration response** tasks, the system fetches the pre-arbitration or arbitration details and runs this subflow to verify the status of the pre-arbitration or arbitration response document.

If the document status shows as Complete, the Mastercom - Look up Case Documents subflow runs to retrieve the document.

</td></tr><tr><td>

Mastercom - Look up List of Claims

</td><td>

Enables you to retrieve claim IDs using existing case IDs related to a dispute task.

</td><td>

PUT /v6/cases/retrieve/claims

</td><td>

**Chargeback** stage:This subflow runs directly after the Mastercom - Create Case Filing subflow runs when the agent files a dispute case by selecting either the **Create pre arbitration** button or the **Create arbitration** button in the **Review chargeback response and decide on pre-arbitration or arbitration** task.

</td></tr><tr><td>

Validate and Process Attachments of Card Disputes Task

</td><td>

A non Mastercom subflow that enables you to validate if uploaded attachments meet Mastercard attachments criteria. This subflow also look up for zip attachment and extract its base64 encoded content.

</td><td>

 

</td><td>

**Chargeback** stage:The agent uploads supporting documents in any of these tasks: **Initiate chargeback and recover funds from merchant**, **Review chargeback response and decide on pre-arbitration or arbitration**, or **Review pre-arbitration response and escalate to arbitration**.

</td></tr></tbody>
</table>## Mastercom queues

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

