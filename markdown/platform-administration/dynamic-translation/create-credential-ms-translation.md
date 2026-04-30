---
title: Create a credential for the MicrosoftTranslation alias
description: Authorize actions of Microsoft Azure Translator Service spoke by creating a credential for the MicrosoftTranslation connection and credential alias.
locale: en-US
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft Azure Translator Service spoke, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Create a credential for the MicrosoftTranslation alias

Authorize actions of Microsoft Azure Translator Service spoke by creating a credential for the MicrosoftTranslation connection and credential alias.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

3.  Select **API Key Credentials**.

4.  In the API key Credentials form, fill the fields.

<table id="table_vt4_m45_shb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Identifier of the credential.

</td></tr><tr><td>

Active

</td><td>

Option to activate the credential for use.

</td></tr><tr><td>

Applies to

</td><td>

MID servers for which the credentials are applicable. Possible options are:-   All MID servers in your network.
-   Specific MID servers. In this case specify the servers in the **MID servers** field.


</td></tr><tr><td>

MID servers

</td><td>

Specific MID servers for which the credentials are applicable. This field is displayed only when you select **Specific MID servers** for the **Applies to** field.

</td></tr><tr><td>

Order

</td><td>

Sequence in which the credential is applied.

</td></tr><tr><td>

API Key

</td><td>

Unique code that is passed to an API to identify the connection.

</td></tr><tr><td>

Credential alias

</td><td>

Alias to use the credential.

</td></tr></tbody>
</table>5.  Select **Submit**.


**Parent Topic:**[Microsoft Azure Translator Service spoke](../concept/microsoft-translation-spoke.md)

**Previous topic:**[Microsoft Azure Translator Service spoke](../concept/microsoft-translation-spoke.md)

**Next topic:**[Create a connection for the MicrosoftTranslation alias](create-connection-ms-translation.md)

