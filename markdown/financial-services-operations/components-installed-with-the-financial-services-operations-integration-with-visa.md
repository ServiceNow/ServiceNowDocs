---
title: Financial Services Operations Integration with Visa subflows
description: You can use the following Financial Services Operations Integration with Visa application subflows to handle the card dispute management process.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Financial Services Operations Integration with Visa reference, Integrating with Visa, Integrating with third-party applications, Integrating applications, Financial Services Operations \(FSO\)]
---

# Financial Services Operations Integration with Visa subflows

You can use the following Financial Services Operations Integration with Visa application subflows to handle the card dispute management process.

## Financial Services Operations Integration with Visa subflows

**Note:** Use the decision table and Visa Token Service template to integrate your chosen Token Provider with Visa Integration subflows. This integration enables you to access Visa APIs, which might contain sensitive information. Make sure to use the subflow template for your Token Provider. This confirms that you detokenize data before sending requests to Visa and tokenize data after receiving responses, for a smooth integration with ServiceNow.

<table id="rpa-subflow"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Case from Transaction

</td><td>

Enables you to create a case in Visa Resolve Online \(VROL\) from a transaction.

</td></tr><tr><td>

Change Dispute Status

</td><td>

Enables you to recall a submitted dispute item or delete a saved dispute item.

</td></tr><tr><td>

Initiate Dispute from Transaction or Case

</td><td>

Enables you to initiate a dispute in VROL from a transaction or from an existing Visa case.

</td></tr><tr><td>

Submit Dispute Questionnaire

</td><td>

Enables you to submit or save the dispute questionnaire in VROL.

</td></tr><tr><td>

Look up Associated Transactions

</td><td>

Enables you to retrieve a list of associated transactions for the disputed transaction in the Dispute stage.

</td></tr><tr><td>

Select Associated Transactions

</td><td>

Enables you to associate related transactions to the disputed transaction.

</td></tr><tr><td>

Submit Transaction Inquiry

</td><td>

Enables you to search for transactions using specific criteria. To confirm seamless integration, must have a tokenization solution. To create a subflow that aligns with the tokenization mechanism and use the recommended Visa Token Service template, configuring it in a decision table.

</td></tr><tr><td>

Look Up Transaction Inquiry Results

</td><td>

Enables you to search for transaction information using TIEventID. If Submit Transaction Inquiry gets an asynchronous response, it generates a TIEventID. This ID is then used to call the subflow and retrieve the original transaction details.

</td></tr><tr><td>

Accept dispute

</td><td>

Accepts the dispute liability or accepts the other side's decision, and removes the dispute transaction from the queue.

</td></tr><tr><td>

Cardholder Purchase Inquiry

</td><td>

Enables you to request purchase information and additional merchant information regarding a transaction by supplying TransactionID.

</td></tr><tr><td>

Look Up Transaction Details

</td><td>

Enables you to retrieve detailed transaction data using RolTransactionId.

</td></tr><tr><td>

Look up Dispute Response Details

</td><td>

Enables you to retrieve the details of a submitted or received dispute response.

</td></tr><tr><td>

Create Dispute Pre Arbitration

</td><td>

Enables you to create a pre-arbitration in VROL.

</td></tr><tr><td>

Create Dispute Pre Arbitration Response

</td><td>

Enables you to create a pre-arbitration response in allocation for the pre-arbitration initiated by the acquirer.

</td></tr><tr><td>

Look up Dispute Pre Arbitration Details

</td><td>

Enables you to retrieve the pre-arbitration details.

</td></tr><tr><td>

Look up Dispute Pre Arbitration Response Details

</td><td>

Enables you to retrieve details of a submitted or received pre-arbitration response.

</td></tr><tr><td>

Submit Dispute Filing

</td><td>

Enables you to submit a dispute for arbitration, or to appeal, or withdrawal of arbitration in VROL.

</td></tr><tr><td>

Look up Dispute Filing Details

</td><td>

Enables you to retrieve the details of a dispute case filing request, appeal, or withdrawal request.

</td></tr><tr><td>

Batch Queues Flows Adapter

</td><td>

Includes all batch queue processes.

</td></tr><tr><td>

Mark Batch Queue Item as Read

</td><td>

Marks transactions as read, removing them from the Real-time Systems Interface \(RTSI\) Batch Queue.

</td></tr></tbody>
</table>## Batch queue processing and scheduling

Batch queues are scheduled jobs. They don't run based on user actions; instead, they execute at predefined time intervals. The **Visa Queue Scheduler Flow** manages it when this job is scheduled to run. By default, the Visa Queue Scheduler Flow is inactive. You must activate this flow to enable batch queue subflows to run at their scheduled intervals.

|Batch Queue|Description|
|-----------|-----------|
|Process Awaiting Action Disputes Batch Queue|The acquirer provides a dispute response, which places the Visa case in this queue. Processing this batch queue alerts the FSO case with the received response.|
|Process Incoming Pre-Arbitration Batch Queue|The acquirer submits a pre-arbitration request or response, which places the Visa case in this queue. Processing this batch queue alerts the FSO case with the received response.|
|Process Incoming Arbitration Batch Queue|The acquirer initiates an arbitration request, or the issuer submits an arbitration and receives an acknowledgment or decision from VISA, which places the case in this queue.|
|Processes Incoming Recall Batch Queue|The acquirer processes recalls at various stages, including dispute response, pre-arbitration, and pre-arbitration response, which places the VISA case in this queue. Processing this batch queue alerts the FSO case with the received response.|

**Parent Topic:**[Financial Services Operations Integration with Visa reference](financial-services-operations-integration-with-visa-reference.md)

