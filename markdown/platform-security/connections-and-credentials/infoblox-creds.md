---
title: Infoblox credentials
description: Infoblox credentials are required to set up IP pools \(IPAM\) in the Cloud Management application.
locale: en-US
release: yokohama
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create and test your credentials, Getting started with credentials, Connections and Credentials, Access Management]
---

# Infoblox credentials

Infoblox credentials are required to set up IP pools \(IPAM\) in the Cloud Management application.

These fields are available on the Credentials form for Infoblox type credentials.

<table id="table_ngl_y4j_kz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

Applies to

</td><td>

Choose whether this credential is available to a specific MID Server or a all MID Servers.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

 Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr><tr><td>

wAPI Version

</td><td>

Enter the [version of wAPI](https://ipam.illinois.edu/wapidoc/) you are using.

</td></tr><tr><td>

User Name and Password

</td><td>

Enter the InfoBlox user name and password.

</td></tr></tbody>
</table>