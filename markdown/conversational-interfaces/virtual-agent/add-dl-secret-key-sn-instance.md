---
title: Add the Direct Line secret key to your Virtual Agent Bot Interconnect instance
description: To use Power Virtual Agents with Virtual Agent Bot Interconnect, you must add the Direct Line security key as a credential in your Bot Interconnect instance.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Add the Direct Line secret key to your Virtual Agent Bot Interconnect instance

To use Power Virtual Agents with Virtual Agent Bot Interconnect, you must add the Direct Line security key as a credential in your Bot Interconnect instance.

## Before you begin

[Locate and copy the Direct Line secret key in Microsoft Power Virtual Agents](get-dl-secret-key-mspva.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Click the **Bot Interconnect DirectLine Credentials** record to open it.

3.  On the Credentials related list, click **New**.

4.  When prompted for the type of credential to create, click **Bot Interconnect Static Token Credential**.

5.  On the form, fill in the fields as follows:

<table id="table_z5c_3y2_lsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Any unique name for the credential, such as `Power VA Direct Line key`.

</td></tr><tr><td>

Header

</td><td>

Leave as **Authorization**.

</td></tr><tr><td>

Static Token

</td><td>

Enter `Bearer`, with a white space, followed by the Direct Line secret key from Power Virtual Agents.For example, enter:

```
Bearer 4km3D8s_6lY.rDVmxVm3k123nWibx3ciJeed2AKled9_ADuwsaN5uCA
```

</td></tr></tbody>
</table>6.  Click **Submit**.

7.  Return to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

8.  Click the **Bot Interconnect DirectLine Fetch Msgs** record to open it.

9.  Under Related Links, click **Create New Connection &amp; Credential**.

10. In the dialog box, fill in the form.

<table id="table_zcp_fpd_nsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Secondary Bot Name

</td><td>

Any unique name that refers to the Power Virtual Agents bot.

</td></tr><tr><td>

Secondary Bot Endpoint

</td><td>

The Azure function URL that you copied in a previous step.For example, enter `https://demoazurefunctionreceivemsgapp.azurewebsites.net`.

</td></tr><tr><td>

Header

</td><td>

Enter: `dlsecret`

</td></tr><tr><td>

Static Token

</td><td>

The Direct Line key that you copied from Power Virtual Agents in the previous step.

</td></tr></tbody>
</table>11. Click **Create**.


**Parent Topic:**[Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-va-api-ms-powerva.md)

**Previous topic:**[Locate and copy the Direct Line secret key in Microsoft Power Virtual Agents](get-dl-secret-key-mspva.md)

**Next topic:**[Create a Virtual Agent Bot Interconnect shell topic to call Microsoft Power Virtual Agents topics](create-primary-va-topic-ms-pva.md)

