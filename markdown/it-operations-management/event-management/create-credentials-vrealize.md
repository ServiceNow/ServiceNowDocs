---
title: Create vRealize credentials
description: Create credentials to access vRealize.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure event collection from vRealize, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create vRealize credentials

Create credentials to access vRealize.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Create Basic Auth type of credential to connect to vRealize.

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

Enter a unique and descriptive name for this credential. For example, `NewvRealize`.

</td></tr><tr><td>

User name

</td><td>

Name to identify the user. -   If the username is internal in vRealize, use it as is.
-   If vRealize is integrated with Active Directory \(AD\), use the format

`DOMAIN\username@sourceauth`. For example, `local\administrator@All vCenter Servers`.

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

The credential for use with the vRealize connector is created.

**Parent Topic:**[Configure event collection from vRealize](t_EMConfigurevRealizeConnectorJS.md)

**Related topics**  


[Credentials and connection information](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

