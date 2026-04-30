---
title: Set up data inputs using Health Log Analytics guided setup
description: The Health Log Analytics guided setup provides a sequence of tasks to help you create data inputs on your ServiceNow instance. Data input configuration is an essential step in setting up the Health Log Analytics application. Using guided setup ensures that you have the minimum required setup for the data input process.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, data input, connector, data input configuration, guided setup]
breadcrumb: [Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Set up data inputs using Health Log Analytics guided setup

The Health Log Analytics guided setup provides a sequence of tasks to help you create data inputs on your ServiceNow instance. Data input configuration is an essential step in setting up the Health Log Analytics application. Using guided setup ensures that you have the minimum required setup for the data input process.

## Before you begin

**Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Ensure that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   If the MID Server IP address is exposed by network address translation \(NAT\), a load balancer, or a similar device, it must have a public IP address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US).
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

-   For MID Server proxy requirements, see [MID Server proxy preconditions for streaming logs to HLA](../reference/hla-mid-proxy-configure.md).

Role required: evt\_mgmt\_admin

## About this task

For information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Guided Setup** &gt; **ITOM Guided Setup** &gt; **Health Log Analytics**.

2.  Follow the instructions to select and set up a data input connector.


## What to do next

Once you've created the data input connector, proceed to [map your raw log data](hla-data-input-mapping.md).

**Parent Topic:**[Health Log Analytics data input setup](../concept/hla-implement.md)

**Related topics**  


[Supported data inputs for Health Log Analytics](../reference/hla-data-input-supported.md)

