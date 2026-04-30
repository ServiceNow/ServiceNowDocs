---
title: Create a connection for the MicrosoftTranslation alias
description: Connect to the Microsoft translation service by creating a connection. Provide information that is used by HTTP\(s\) actions or activities to connect to that service.
locale: en-US
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Translator Service spoke, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Create a connection for the MicrosoftTranslation alias

Connect to the Microsoft translation service by creating a connection. Provide information that is used by HTTP\(s\) actions or activities to connect to that service.

## Before you begin

Ensure that you are in the application scope that you want for your connection. The default application scope is **Microsoft Azure Translator Service Spoke**.

Role required: connection\_admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select the MicrosoftTranslation alias \(sn\_ms\_trans\_spoke.MicrosoftTranslation\).

3.  In the **Connections** tab, click **New**.

4.  In the HTTP\(S\) Connection form, fill the fields.

<table id="table_lyh_2bv_shb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the HTTP\(s\) connection.

</td></tr><tr><td>

Credential

</td><td>

Credential record used to authorize the connection.

</td></tr><tr><td>

Connection alias

</td><td>

Alias record to associate with the connection. Using an alias enables you to update the connection record without having to reconfigure any actions or activities that use the alias.

</td></tr><tr><td>

Active

</td><td>

Option to activate the connection.

</td></tr><tr><td>

Domain

</td><td>

Domain where the connection is applicable.

</td></tr><tr><td>

URL builder

</td><td>

Option to enable the system to build the connection URL. Clear this check box.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to the Microsoft's translation service. For example, `https://api.cognitive.microsofttranslator.com`. **Note:** This URL is a sample only. Microsoft translation customers may need to use custom API URLs or virtual network type API URLs, even when they do not subscribe to a virtual network. Check your Azure portal to obtain your API URL.

 For further information, refer to [Microsoft](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/reference/v3-0-reference#virtual-network-support) documentation.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server for this connection.

</td></tr><tr><td>

Connection timeout

</td><td>

Timeout value in milliseconds. Overrides the global property for this usage.

</td></tr><tr><td class="sub-head" colspan="2">

Attributes

</td></tr><tr><td>

Version

</td><td>

API version that the related spokes are built for. The default value is v3. Do not edit this value.

</td></tr><tr><td>

Ocp-Apim-Subscription-Region

</td><td>

Value of the regional translator resource. This value is optional when using a global translator resource. **Note:** This value is mandatory for customers using Microsoft's multi-service or regional translator resources.

For information on supported regions, see the [Microsoft](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/reference/v3-0-reference#authenticating-with-a-multi-service-resource) documentation.

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Microsoft Azure Translator Service spoke](../concept/microsoft-translation-spoke.md)

**Previous topic:**[Create a credential for the MicrosoftTranslation alias](create-credential-ms-translation.md)

**Next topic:**[Activate the Microsoft translator configuration](activate-ms-translator-config.md)

