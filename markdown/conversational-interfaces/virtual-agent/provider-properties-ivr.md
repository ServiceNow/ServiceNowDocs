---
title: Provider properties for Amazon Connect
description: View and update the provider properties available for Amazon Connect
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Conversational IVR with Amazon Connect, Configuring Conversational IVR with Amazon Connect, Conversational IVR with Amazon Connect, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Provider properties for Amazon Connect

View and update the provider properties available for Amazon Connect

## Before you begin

Role required: admin

## Procedure

1.  Select **All** and enter `sys_cs_provider.list` to open the Connections table.

2.  Select the provider **VA Amazon Connect Adapter Provider**.

3.  In the Provider Channels form, select the **Provider Properties** tab.


## What to do next

The following table lists the properties.

**Important:** Unless absolutely necessary, the property values must not be edited.

<table id="table_ysb_njh_m2c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

amazon\_connect\_pause\_break\_time

</td><td>

Property to specify the pause time, in seconds, between line breaks, choice options, sentences, bullet points, and so on, in the amazon connect response. The value must be a number.

</td></tr><tr><td>

amazon\_connect\_reference\_number\_pause\_time

</td><td>

Pause time before reading of the submitted request or incident number. Value is in seconds. Maximum value allowed is 10.

</td></tr><tr><td>

amazon\_lex\_voice\_timeout\_ms

</td><td>

Property to specify the time, in milli seconds, the bot waits before assuming that the user isn't going to speak.

</td></tr><tr><td>

pagination\_enabled

</td><td>

Property used to enable pagination at adapter level. Value must be set to true to enable pagination.**Note:** Pagination shouldn't be disabled.

</td></tr><tr><td>

pagination\_max\_choice\_limit

</td><td>

Property used to specify the maximum number of items per page when pagination is enabled. Value must be an integer.

</td></tr><tr><td>

picker\_pagination\_experience\_supported

</td><td>

Property used to enable pagination at server level. Value must be set to true to enable pagination.**Note:** Pagination shouldn't be disabled.

</td></tr><tr><td>

disable\_manual\_linking

</td><td>

If the property value is true, manual linking options aren't shown when account linking is enabled.**Note:** Do not change the property value.

</td></tr><tr><td>

support\_genai\_qa\_card

</td><td>

Internal, do not change.

</td></tr><tr><td>

support\_skill\_card

</td><td>

Internal, do not change.

</td></tr></tbody>
</table>**Parent Topic:**[Configure Conversational IVR with Amazon Connect](configure-va-ivr.md)

