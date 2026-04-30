---
title: Exploring Card Data Security
description: Learn more about Card Data Security and how it can be used to tokenize sensitive card data for Dispute Cases and Dispute Transactions.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Exploring Card Data Security

Learn more about Card Data Security and how it can be used to tokenize sensitive card data for Dispute Cases and Dispute Transactions.

## Card Data Security overview

The Card Data Security application provides a tokenizer service that enables you to replace sensitive data in dispute workflows with non-sensitive equivalent values called tokens.

You can configure data to be tokenized as it enters your ServiceNow instance, and have it restored to its original value when it is sent to Third-Party Systems.

\(Disclaimer: This application enables data tokenization capabilities for Dispute Cases and Dispute Transactions.\)

Other features of the tokenizer service are shown below:

-   **File Vaulting**

    Securely store files with sensitive information in the tokenizer service vault.

-   **Document De-identification**

    Redact predefined entities in images and PDFs.

-   **Embeddable SDKs**

    Embed front-end SDKs into ServiceNow UIs.

-   **Vault type: Multi-Tenant**

    Accounts are hosted on shared infrastructure, isolated by account and vault boundaries.


For more information on these other features of the tokenizer service, refer to the [tokenizer service documentation](https://docs.skyflow.com/).

**Note:**

Check your entitlements to determine whether you have access to a feature.

## Card Data Security users

<table id="table_qs3_kyk_4fc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administrator

</td><td>

Administrators manage the card vault table. They configure the connections and routes between your ServiceNow instance, our tokenizer service, and the third-party financial systems involved in Dispute Case and Dispute Transaction processing, such as card networks and core banking systems \("Third-Party System\(s\)"\).

</td></tr></tbody>
</table>## Card Data Security workflow

The following graphic shows how our tokenizer service is designed to tokenize and detokenize data in Card Data Security.

![Infographic showing the flow of data being tokenized from Third-Party Systems, and the detokenization of sensitive data when sent to Third-Party Systems. For details, refer to the following description.](../image/card-data-security-workflow.png "Tokenization data flow")

1.  Data retrieved from a Third-Party System that you configure is tokenized using our tokenizer service before it enters your ServiceNow instance.
2.  Tokenized data sent from your ServiceNow instance's dispute workflow can also be configured to be detokenized to its original value by our tokenizer service before it is sent to a Third-Party System.

## Card Data Security benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Use a card vault table to store tokenized values of configured data.|[Create the card vault table in the tokenizer service](create-tokenization-vault.md)|Administrator|
|Manage each tokenizer configuration that sends and receives tokenized data with Third-Party Systems.|[Manage Tokenizer Resource Configurations](manage-tokenizer-resource-configurations.md)|Administrator|

## What to explore next

To learn more about configuring Card Data Security, see:

-   [Configuring Card Data Security](configuring-card-data-security.md)
-   [Managing Card data security](managing-card-data-security.md)
-   [Card Data Security Reference](card-data-security-reference.md)

**Related topics**  


[Configuring Card Data Security](configuring-card-data-security.md)

[Managing Card data security](managing-card-data-security.md)

[Card Data Security Reference](card-data-security-reference.md)

