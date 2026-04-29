---
title: API key credentials
description: An API key is a unique code that is passed in to an API to identify the calling application or user.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create and test your credentials, Get started with credentials, Connections and Credentials, Access Management]
---

# API key credentials

An API key is a unique code that is passed in to an API to identify the calling application or user.

## API key credentials

<table id="table_APIKeyCredentialsForm"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

API Key

</td><td>

Enter the API key.

</td></tr><tr><td>

Credential alias

</td><td>

Allow flow and workflow creators to assign individual credentials to any activity in a flow or workflow or assign different credentials to each occurrence of the same activity type in a flow or workflow.

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr></tbody>
</table>