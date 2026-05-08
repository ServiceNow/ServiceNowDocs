---
title: Create Nagios XI server credentials
description: Create credentials to access Nagios XI server.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure event collection from NagiosXI, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create Nagios XI server credentials

Create credentials to access Nagios XI server.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

3.  Select **Basic Auth Credential**.

4.  On the form, fill in the fields.

<table id="table_j35_mmp_ydb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential. For example, you might call it `Nagios authentication`.

</td></tr><tr><td>

User name

</td><td>

Name to identify the user.Ensure that the user password contains the NagiosXI user API key, for example, `04lquEPqf4JimWCm8RWbJokOpW8LYBUfEvJp9OSHSRYe4QDrHPFndYbWcCHapBpk`.

</td></tr><tr><td>

Password

</td><td>

Password to use this credential.

</td></tr><tr><td>

Active

</td><td>

Option to enable the use of this credential.

</td></tr><tr><td>

Order

</td><td>

The order \(sequence\) in which the platform tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order. Default value: `100`

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

The credential for use with the Nagios XI server connector is created.

**Parent Topic:**[Configure event collection from NagiosXI](configure-nagios-connector.md)

**Related topics**  


[bundle-psec.r-credentials]

