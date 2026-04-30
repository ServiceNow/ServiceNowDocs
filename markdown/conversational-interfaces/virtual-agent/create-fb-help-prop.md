---
title: Configure the help link for the Virtual Agent Facebook Messenger integration \(Legacy\)
description: Use the va.messenger.help.url system property to create the link that opens a web help page when requesters use the Help command in the Virtual Agent Facebook Messenger integration.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Conversational Integration with Facebook Messenger, Integrating Virtual Agent with consumer messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure the help link for the Virtual Agent Facebook Messenger integration \(Legacy\)

Use the **va.messenger.help.url** system property to create the link that opens a web help page when requesters use the **Help** command in the Virtual Agent Facebook Messenger integration.

## Before you begin

-   Determine the web page that provides the help content that your Facebook Messenger users need.
-   Role required: virtual\_agent\_admin or admin


## Procedure

1.  Set the application scope to **Global**.

2.  In the Navigation filter, enter `sys_properties.list`.

3.  Click **New**.

4.  Complete the following:

    1.  In the **Name** field, enter the system property name: **va.messenger.help.url**.

    2.  In the **Description** field, enter a brief explanation of this property.

    3.  In the **Value** field, enter the URL of the website page that the link opens.

    4.  Click **Submit**.


## Result

When your Facebook Messenger users type `help`, they are directed to the URL of the website specified in the **va.messenger.help.url** property.

