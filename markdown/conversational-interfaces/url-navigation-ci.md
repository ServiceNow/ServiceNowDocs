---
title: URL navigation in Conversational Interfaces
description: Use URL navigation settings to specify where and how chat links open. You can configure certain links to open in a specific portal. You can also specify the link target, such as a popup window.
locale: en-US
release: zurich
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [URL, navigation, settings, Conversational Interfaces]
breadcrumb: [General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# URL navigation in Conversational Interfaces

Use URL navigation settings to specify where and how chat links open. You can configure certain links to open in a specific portal. You can also specify the link target, such as a popup window.

Your base system instance provides default portals in which chat links to records from certain ServiceNow tables are opened automatically. For example, Service Portal is the default portal used to display knowledge records from the Knowledge \[kbknowledge\] table and also catalog items from the Catalog Item \[sc\_cat\_item\] table.

Use **URL navigation** in Chat Settings to change these default mappings, as well as define custom mappings that map a portal URL to a specified ServiceNow table. The portal configurations apply to the chat widget, chat channels, and messaging channels.

## How URL navigation works

To determine the portals to be used for chat links, the system evaluates the following information in the order listed:

1.  `sysparm` portal parameter - If you specified a sysparm\_portal parameter in the instance URL for the chat widget, that portal is used.
2.  Topic script variable - If you specified a portal in a topic script variable, that portal is used.
3.  Default portal for Provider Channel Identity - If you specified a default portal in the Provider Channel Identity \[sys\_cs\_provider\_application\] table for pre-built chat integrations or custom chat integrations, that portal is used. The default portal applies to the chat and messaging channels for the provider. For details on configuring the Provider Channel Identity, see [Create a channel identifier for your custom chat integration](../../virtual-agent/task/create-channel-id-va-cccif.md) in Custom chat integration framework.
4.  Default portal for a table - Uses the portal value in the default portal mapping listed in **URL navigation** Chat Setting.
5.  Global default portal - If you defined a global default portal using the **com.glide.cs.url\_redirect.default.portal** system property, that global portal is used.
6.  Service Portal - If you didn't define a global portal using the **com.glide.cs.url\_redirect.default.portal** property, Service Portal is used.

## Legacy URL mappings defined in previous releases \(fallback method\)

If you previously added the **com.glide.cs.portal\_url\_mapping.default.&lt;portal\_value&gt;.&lt;table\_name&gt;** property to create URL mappings that were used instead of the default URL mappings, those properties are retained after you upgrade to the Zurich release. However, you can now view the mappings using **URL navigation** in Chat Settings or the URL Navigation \[sys\_cs\_portal\_url\_mapping\] table. There are two types of URL mappings.

-   **Default mappings**

    All system properties with the format **com.glide.cs.portal\_url\_mapping.portal.&lt;table\_name&gt;** that define the default portal used for certain ServiceNow tables.

<table id="table_u53_1pk_24b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.cs.portal\_url\_mapping.portal.kb\_knowledge

</td><td>

Default portal context \(URL mapping\) to use for Knowledge Base articles.-   Type: string
-   Default value: sp \(Service Portal\)


</td></tr><tr><td>

com.glide.cs.portal\_url\_mapping.portal.sc\_cat\_item

</td><td>

Default portal context \(URL mapping\) to use for Service Catalog items.-   Type: string
-   Default value: sp \(Service Portal\)


</td></tr><tr><td>

com.glide.cs.portal\_url\_mapping.portal.sys\_user

</td><td>

Default portal context \(URL mapping\) for sys\_ user records.-   Type: string
-   Default value: esc \(Employee Service Center\)


</td></tr></tbody>
</table>-   **Custom mappings**

    All system properties that define a portal and table combination using the format **com.glide.cs.portal\_url\_mapping.&lt;portal\_name&gt;.&lt;table\_name&gt;**. These mappings are retained as custom mappings. When the portal or table is specified with **\_default**, it indicates that any portal or table is used.

    The system determines the URL for custom mappings by evaluating the following values:

    -   Portal and table/parent table
    -   Portal and any table
    -   Any portal and table/parent table
    -   Any portal and any table
<table id="table_wtj_ztf_b4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.cs.portal\_url\_mapping.\_default.kb\_knowledge

</td><td>

Default for Knowledge URL mapping.

 -   Type: string
-   Value:/\{\{portal\}\}?id=kb\_article&amp;sys\_id=\{\{data.sys\_id\}\}


</td></tr><tr><td>

com.glide.cs.portal\_url\_mapping.\_default.sc\_cat\_item

</td><td>

Default for Catalog Item URL mapping.

 -   Type: string
-   Value: /\{\{portal\}\}?sys\_id=\{\{data.sys\_id\}\}&amp;id=\{\{data.table\_name\}\}&amp;table=\{\{data.table\_name\}\}


</td></tr><tr><td>

com.glide.cs.portal\_url\_mapping.\_default.sys\_user

</td><td>

Default for User URL mapping.

 -   Type: string
-   Value: /\{\{portal\}\}?id=user\_profile&amp;sys\_id=\{\{data.sys\_id\}\}


</td></tr><tr><td>

com.glide.cs.portal\_url\_mapping.\_default.\_default

</td><td>

Default URL mapping for records other than knowledge articles, Service Catalog items, People \(sys\_user\) records, publication records, and task records.

 -   Type: string
-   Value: /\{\{portal\}\}?sys\_id=\{\{data.sys\_id\}\}&amp;id=form&amp;table=\{\{data.table\_name\}\}


</td></tr></tbody>
</table>
## Smart links

As an admin, you can specify the target for URL links based on patterns that you specify. For example, if you want all KB articles to open in a new window, you can configure the mapping in general chat settings. For more information, see [Create a smart link preference](../task/create-smart-link-preference.md).

-   **[Configure URL navigation for chat links](../task/ac-configure-url-navigation.md)**  
Configure the portals in which links to ServiceNow records in Live Agent and Virtual Agent conversations are opened, including links in output cards and cards for Virtual Agent notifications and AI Search results.
-   **[Create a smart link preference](../task/create-smart-link-preference.md)**  
Create smart links to specify where a URL should open. For example, the URL could open in a new browser window, in a new browser tab, in the chat window, or in a pop-up window.

**Parent Topic:**[General chat settings](ci-configuring-chat-features.md)

