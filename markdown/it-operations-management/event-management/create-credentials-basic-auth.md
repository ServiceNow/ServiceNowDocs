---
title: Create basic auth server credentials
description: Create credentials to access a ServiceNow instance.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Event forwarding, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create basic auth server credentials

Create credentials to access a ServiceNow instance.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

3.  Select **Basic Auth Credential**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique and descriptive name for this credential.|
    |User name|Name to identify the user.|
    |Password|Password to use this credential.|
    |Active|Option to enable the use of this credential.|
    |Order|The order \(sequence\) in which the platform tries this credential while it attempts to log in to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order. Default value: `100`|

5.  Select **Submit**.


## Result

The Basic Auth credential for use with the server instance is created.

