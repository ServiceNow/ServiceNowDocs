---
title: Set up NLU for Sourcing and Procurement Operations Virtual Agent
description: Set up Natural Language Understanding \(NLU\) for Sourcing and Procurement Operations Virtual Agent before chatting with the Virtual Agent to optimize the search experience.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Virtual Agent for Sourcing and Procurement Operations, Sourcing and Procurement Operations integration with Employee Center, Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Set up NLU for Sourcing and Procurement Operations Virtual Agent

Set up Natural Language Understanding \(NLU\) for Sourcing and Procurement Operations Virtual Agent before chatting with the Virtual Agent to optimize the search experience.

## Before you begin

Role required: admin, virtual\_agent\_admin

You must have the following plugin installed on your instance: Natural Language Understanding Models for Sourcing and Procurement Operations. For information on how to install the plugin, follow this [procedure](install-virtual-agent-for-shoppinghub.md).

## Procedure

1.  Train and publish the NLU model.

    1.  Navigate to **NLU Workbench &gt; Models**.

    2.  Select **Sourcing and Procurement Operations Model**.

    3.  Select **Train** to train your prediction server for the first time before you get started.

    4.  Select **Publish** to publish the NLU model.

2.  Enable NLU for Sourcing and Procurement Operations Virtual Agent.

    **Note:** This is a one-time activity that you must perform to ensure that NLU is enabled for Virtual Agent in your instance.

    1.  Navigate to **Conversational Interfaces &gt; Virtual Agent &gt; General Settings**.

    2.  Select the **Enable NLU in Virtual Agent** radio button to enable NLU.

    3.  In the **NLU service provider** field, select **ServiceNow NLU**.

    4.  Select **Save**.

3.  Integrate NLU with Sourcing and Procurement Operations Virtual Agent.

    1.  Navigate to **Conversational Interfaces &gt; Virtual Agent &gt; Designer**.

    2.  In the **Category** field, select **PSM Virtual Agent Topics**.

    3.  In the **Type** field, select **Topics**.

    4.  Select any topic to open it.

    5.  Select the **Properties** tab.

    6.  In the **Set up Natural Language Understanding \(NLU\)** section, **NLU Model** field, select **Sourcing and Procurement Operations Model**.

    7.  In the **Associated Intent** field, select the relevant intent.

    8.  Select the **Flow** tab.

    9.  Select the first input entity.

    10. In the **User Input Properties** section, **Name** field, enter **Product service term**.

    11. In the **Associated Entity** field, select **SupplierProduct**.

    12. Select the **Enable NLU at Input Node** radio button.

    13. Select the **Skip confirmation for recognized entity** radio button.

    14. Save and publish the topic.


**Parent Topic:**[Virtual Agent for Sourcing and Procurement Operations](../concept/virtual-agent-for-psm.md)

