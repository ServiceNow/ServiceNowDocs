---
title: Configuring Card Data Security
description: Plan and configure your implementation of Card Data Security by following the tasks listed in this configuration overview.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Configuring Card Data Security

Plan and configure your implementation of Card Data Security by following the tasks listed in this configuration overview.

## Configuration overview

Refer to the following steps to set up and configure Card Data Security for the first time.

1.  [Set up spoke integrations](../../fso-common/concept/spokes.md)

    Install and set up integrations to the Third-Party Systems \(such as Visa Spoke or Mastercard Spoke\). Card Data Security requires these integrations to function correctly.

2.  [Provision our tokenizer service and complete the onboarding procedure](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2238661)

    Ensure that you have provisioned our tokenizer service and that you have completed the onboarding procedure. For more information, contact your ServiceNow account representative.

3.  [Install Card Data Security](../task/install-card-data-security.md)

    Install Card Data Security \(sn\_data\_sec\) from the ServiceNow Store.

4.  [Create the card vault table in the tokenizer service](create-tokenization-vault.md)

    Create the card vault table in our tokenizer service. This contains the tokenized values from Third-Party Systems.

5.  [Set up connections to the tokenizer service](../task/set-up-outbound-connections.md)

    Set up the connections between your ServiceNow instance, our tokenizer service, and the Third-Party System.

6.  [Set up tokenized HTTP connection and credentials](../task/create-a-new-tokenizer-route.md)

    Define the connection and credentials in ServiceNow to communicate to the Third-Party System via our tokenizer service.

7.  [Set up tokenized REST message record](../task/set-up-a-rest-message-function.md)

    Create or update REST message records for your Third-Party Systems.

8.  [Manage Tokenizer Resource Configurations](manage-tokenizer-resource-configurations.md)

    Review the entries for each endpoint that sends and receives tokenized data, confirming that it is set up for our tokenizer service.


