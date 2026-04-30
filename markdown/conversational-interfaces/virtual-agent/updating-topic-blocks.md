---
title: Maintain reusable topic blocks
description: When you update topic blocks, Virtual Agent Designer provides built-in checks to help you identify changes to topic blocks that affect the calling topics that use them. Updates include changing input and output parameters, deleting topic blocks, and publishing inactive and active topic blocks and calling topics.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Maximizing code reuse with topic blocks, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Maintain reusable topic blocks

When you update topic blocks, Virtual Agent Designer provides built-in checks to help you identify changes to topic blocks that affect the calling topics that use them. Updates include changing input and output parameters, deleting topic blocks, and publishing inactive and active topic blocks and calling topics.

To help you maintain your topic blocks and associated calling topics, Virtual Agent Designer provides alerts that serve as guardrails. These alerts have many functions, including the following:

-   They warn you of topic block updates that affect associated calling topics.
-   They help prevent you from making unintentional changes.
-   They let you know that you may need to make changes in associated calling topics.

## Changing the input or output parameters in a topic block that is used by calling topics

Virtual Agent Designer helps prevent you from deleting output parameters that are being used in calling topics. Virtual Agent Designer informs you that the changes will affect calling topics that use the topic block.

For example, suppose you added a new input parameter and made an existing parameter required in the Acme Contextual Search topic block. You can review the affected topics from a link on the topic block's **Properties** tab. The **View published topics that use this topic block link** opens the Topic Library Usages \[sys\_cs\_topic\_library\_usage\] table. This table lists the published calling topics that use the topic block.

When you open an affected topic, Virtual Agent Designer displays warnings and messages on the canvas indicating where you need to make changes. When you select the Topic Block node, warning messages are displayed in the properties sheet so that you can update parameters accordingly.

![Virtual Agent Designer topic Properties tab, Topic Library usages table, and conversation builder canvas with highlighted areas showing how to find topics affected by input parameter changes.](../images/parameter-change.png "Messaging of input parameter changes")

