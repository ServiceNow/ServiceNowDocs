---
title: Configure a websocket endpoint
description: Configure a websocket endpoint to provide web access from the MID Server to the Agent Client Collector \(ACC\).
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector with a MID Server, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Configure a websocket endpoint

Configure a websocket endpoint to provide web access from the MID Server to the Agent Client Collector \(ACC\).

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

For added security, ensure that MID Servers deployed for the Agent Client Collector aren’t deployed for other components.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **MID Servers**.

2.  Select a MID Server.

3.  Select the **ACC Websocket Endpoints** tab on the bottom of the page.

4.  Select **New**.

5.  Configure the fields on the page.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a descriptive name for the websocket endpoint.|
    |MID Server|The name of the selected MID Server.|
    |Short description|Optionally, enter a short description for the websocket endpoint.|
    |Accessible IP address|Apply an external/public IP when the MID Server has an internal IP that is not accessible from an agent. Used for cloud solutions with an agent that has access only to the MID Server's public IP. If the MID Server and all agents are in the same Virtual private cloud \(VPC\), this field can be left empty.|

6.  In the **Related Links** section, select **Start** to activate the websocket endpoint.


**Parent Topic:**[Configuring Agent Client Collector with a MID Server](../concept/acc-configuring-with-mid.md)

