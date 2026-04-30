---
title: Message delivery order
description: Control message delivery order by enabling the Maintain message ordering option in the Provider Channel \[sys\_cs\_provider\] table. You can view the message order and status in the Custom Adapter Message \[sys\_cs\_ca\_message\] table.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Supported features for custom chat integrations, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Message delivery order

Control message delivery order by enabling the **Maintain message ordering** option in the Provider Channel \[sys\_cs\_provider\] table. You can view the message order and status in the Custom Adapter Message \[sys\_cs\_ca\_message\] table.

When you enable the **Maintain messaging order** option in the Provider Channel table, a Sender Subflow occurs only after the previous Sender Subflow completes to ensure that messages are delivered in the order that they were sent.

Messages are stored in the Custom Adapter Message \[sys\_cs\_ca\_message\] table, which is cleaned nightly. If the Custom Chat Integration Framework client is not receiving any messages, you can use this table to check the message delivery status:

-   Processing
-   Pending - not yet processed
-   Completed
-   Error - problem with processing an outbound message, possibly due to Integration Hub issues that could occur when the Sender Subflow is invoked

**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

