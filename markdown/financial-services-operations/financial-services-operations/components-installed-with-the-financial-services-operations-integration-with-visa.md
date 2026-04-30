---
title: Financial Services Operations Integration with Visa subflows
description: You can use the following Financial Services Operations Integration with Visa application subflows to handle the card dispute management process.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Financial Services Operations Integration with Visa subflows

You can use the following Financial Services Operations Integration with Visa application subflows to handle the card dispute management process.

**Note:** Use the decision table and Visa Token Service template to integrate your chosen Token Provider with our Visa Integration subflows. This integration will enable you to securely access Visa APIs, which may contain sensitive information. Ensure to implement the subflow template for your Token Provider, ensuring detokenization before sending requests to Visa and tokenization after receiving responses from Visa for seamless integration with the ServiceNow system.

|Subflow|Description|
|-------|-----------|
|Create Case from Transaction|Allows users to create a case in the VROL system from a transaction.|
|Initiate Dispute from Transaction or Case|Allows users to initiate a dispute in the VROL system from a transaction or from an existing Visa case.|
|Submit Dispute Questionnaire|Allows users to submit or save the dispute questionnaire in the VROL system.|
|Look up Associated Transactions|Allows users to retrieve a list of associated transactions for the disputed transaction in the Dispute stage.|
|Select Associated Transactions|Allows users to associate related transactions to the disputed transaction.|
|Change Dispute Status|Allows users to recall a submitted dispute item or delete a saved dispute item.|
|Look up Case Details|Allows users to request details of a specific VROL case, including case status, stage and resolution status details.|
|Submit Fraud Report|Allows users to submit a fraud report to Visa Resolve Online \(VROL\), including all the required fraud data.|
|Update Case Resolution Status|Allows users to update the case resolution status of a case. This may close the case, depending on the status change made.|
|Submit Transaction Inquiry|Allows users to search for transactions using specific criteria. To ensure seamless integration, users must have a tokenization solution. To create a subflow that aligns with the tokenization mechanism and use the recommended Visa Token Service template, configuring it in a decision table.|

**Parent Topic:**[Financial Services Operations Integration with Visa reference](financial-services-operations-integration-with-visa-reference.md)

