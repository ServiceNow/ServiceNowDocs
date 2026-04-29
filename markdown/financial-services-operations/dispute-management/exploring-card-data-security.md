---
title: Exploring Card Data Security
description: Learn more about Card Data Security and how it can be used to tokenize sensitive card data, display and mask Primary Account Numbers \(PANs\), and manage sensitive attachments for Dispute Cases and Dispute Transactions.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Exploring Card Data Security

Learn more about Card Data Security and how it can be used to tokenize sensitive card data, display and mask Primary Account Numbers \(PANs\), and manage sensitive attachments for Dispute Cases and Dispute Transactions.

## Card Data Security overview

The Card Data Security application helps organizations adhere to Payment Card Industry Data Security Standard \(PCI DSS\) requirements by protecting cardholder data. It provides a tokenizer service that substitutes sensitive data in dispute workflows—such as Primary Account Numbers \(PANs\) and documents—with non-sensitive equivalent values called tokens.

Using tokens prevents sensitive data from being stored on a ServiceNow instance, minimizing the impact of a data breach.

You can configure data to be tokenized as it enters your ServiceNow instance, and have it restored to its original value when it is sent to Third-Party Systems.

\(Disclaimer: This application enables data tokenization capabilities for Dispute Cases and Dispute Transactions.\)

## Value of Card Data Security

The PCI Data Security Standard requires organizations processing payment card transactions to implement proper security measures. Systems that handle sensitive financial information, such as payment card data, must meet PCI standards to safeguard payment information and reduce the risk of data breaches and fraud.

A card disputes solution needs to be PCI compliant for the following reasons:

1.  Card dispute flows may store, process, or transmit physical card details.
2.  Card dispute case logs may contain sensitive data.
3.  Card dispute flows integrate with card networks that transmit card data in their responses.
4.  Merchants may submit evidence that contains sensitive data, such as screenshots, receipts, or statements.

![Diagram highlighting areas in the card dispute workflow that may handle PCI information.](../image/card-data-security-value.png)

Card Data Security provides a secure, PCI-compliant vault for sensitive payment information, while allowing FSO users to maintain operational efficiency in dispute management processes. Whether your organization falls under PCI Level 1 reporting requirements or operates at lower transaction volumes, Card Data Security can help maintain PCI compliance while streamlining financial services operations.

## Use cases

Card Data Security can support dispute management scenarios such as:

-   Creating a dispute case by entering secure card data
-   Enhancing an investigation workflow by displaying card information
-   Document management for PCI-compliant file handling

## Features

The following table shows the features available in Card Data Security:

<table id="table_iwt_f4y_c3c"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Built-in tokenizer service vault and schemas

</td><td>

Card Data Security includes schemas to support storing card details and sensitive documents in the tokenizer service vault, so that PANs and sensitive data are not stored in ServiceNow.

</td></tr><tr><td>

Manage connections and credentials

</td><td>

Supports defining service accounts, user and role management, and context-aware authorization. Card Data Security provides connection aliases for Visa Resolve Online \(VROL\) and Mastercom that can be configured to your workflow's requirements.

</td></tr><tr><td>

Seamless passthrough integration

</td><td>

The Card Data Security tokenizer service passes through API requests from ServiceNow and responses from card networks, while tokenizing and detokenizing data as required.

</td></tr><tr><td>

Tokenize and detokenize PANs in VROL and Mastercom requests and responses

</td><td>

Use included VROL and Mastercom connections, or upload and configure other connections for the tokenizer service.

</td></tr><tr><td>

Store inbound documents from VROL and Mastercom in the Card Data Security tokenizer service vault

</td><td>

Sensitive documents sent from VROL and Mastercom are kept in the tokenizer service vault, preventing PCI data from being stored in a ServiceNow instance.

</td></tr><tr><td>

List and download documents stored in the Card Data Security tokenizer vault

</td><td>

At the transaction level of a card dispute, use the Attachments contextual side panel to view a list of documents stored in the tokenizer service vault, or download documents to your device.

</td></tr><tr><td>

View and mask PANs in card disputes

</td><td>

Show the full PAN or only the last four digits in the dispute workflow.

</td></tr><tr><td>

Card Data Security container for entering PANs

</td><td>

Use the Card Data Security container to integrate PAN entry in your disputes workflow.**Note:** This feature is not pre-configured for the card disputes workflow and requires additional setup by an administrator.

</td></tr><tr><td>

Document De-identification

</td><td>

Redact predefined entities in images and PDFs.**Note:** This feature is not pre-configured for the card disputes workflow and requires additional setup by an administrator.

</td></tr></tbody>
</table>## Passthrough Integration Workflow Example

See how PCI data is tokenized and detokenized with Card Data Security when communicating with card networks.

![Workflow diagram showing tokenization flow with PCI data in response.](../image/card-data-security-response-workflow.png "Tokenization flow with PCI data in response")

1.  In a dispute intake workflow with a financial account number, a card network API request is sent.
2.  The Card Data Security tokenizer service passes through the request to the card network.
3.  The card network sends a response containing PCI data \(such as a PAN\).
4.  The Card Data Security tokenizer service replaces the PAN with a token value and sends the token to the dispute workflow.

![Workflow diagram showing tokenization flow with PCI data in request.](../image/card-data-security-request-workflow.png "Tokenization flow with PCI data in request")

1.  In a dispute intake workflow, a card network API request is sent containing the tokenized data.
2.  The Card Data Security tokenizer service receives the request and substitutes the tokenized data with the PCI data \(such as a PAN\). The request containing the PAN is sent to the card network.
3.  The card network sends a response.
4.  The Card Data Security tokenizer service passes through the response to the dispute workflow.

## Users

<table id="table_qs3_kyk_4fc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administrator

</td><td>

Administrators manage the card vault table. They configure the connections and routes between your ServiceNow instance, our tokenizer service, and the third-party financial systems involved in Dispute Case and Dispute Transaction processing, such as card networks and core banking systems \("Third-Party System\(s\)"\).

 They can also implement the Card Data Security container in a disputes workflow using UI Builder.

</td></tr><tr><td>

Agent

</td><td>

Agents use Card Data Security to view and reveal PANs in a transaction for a card dispute case. At the transaction level of a dispute case, agents can also view and download secure attachments sent from VROL and Mastercom in the Attachments contextual side panel.

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring Card Data Security, see:

-   [Configuring Card Data Security](configuring-card-data-security.md)
-   [Managing Card data security](managing-card-data-security.md)
-   [Card Data Security Reference](card-data-security-reference.md)

