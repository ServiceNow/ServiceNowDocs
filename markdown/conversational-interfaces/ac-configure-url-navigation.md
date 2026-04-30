---
title: Configure URL navigation for chat links
description: Configure the portals in which links to ServiceNow records in Live Agent and Virtual Agent conversations are opened, including links in output cards and cards for Virtual Agent notifications and AI Search results.
locale: en-US
release: zurich
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [URL navigation in Conversational Interfaces, General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Configure URL navigation for chat links

Configure the portals in which links to ServiceNow records in Live Agent and Virtual Agent conversations are opened, including links in output cards and cards for Virtual Agent notifications and AI Search results.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Under **URL navigation,** select **View All**.

3.  On the URL Navigation page, do one of the following:

    -   To create a new custom mapping, select **New**.
    -   To change a default or custom mapping, select the record to be updated.
    -   If you have multiple mapping records to be updated, click the box to the left of the mapping record to be updated and select **Edit**. The preview pane opens and shows the URL Navigation fields that you can change in the selected records.
4.  Complete or update the URL Navigation fields.

<table id="table_xbp_wkm_spb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Name of the portal for a particular table record.

</td></tr><tr><td>

Type

</td><td>

Type of portal mapping:-   Default Mapping: Default portal mapped to the following ServiceNow tables:
    -   Service Portal - Catalog Item \[sc\_cat\_item\] table
    -   Service Portal - Knowledge \[kb\_knowledge\] table
    -   Employee Center Portal - User \[sys\_user\] table
-   Custom Mapping: Portal URL definition that identifies a portal and ServiceNow table combination, which is entered in the **Value** field.


</td></tr><tr><td>

Table

</td><td>

ServiceNow table that maps to the portal. Select a table from the list of tables.

</td></tr><tr><td>

Application

</td><td>

Name of the application to which this URL mapping belongs.

</td></tr><tr><td>

Portal

</td><td>

Portal to be used in the mapping. Select a portal from the list of portals.

</td></tr><tr><td>

Value

</td><td>

For new custom mappings, specify the combination of portal and table values to form the link. For example, the following value maps knowledge articles to the CSP portal:`/csp?id=kbarticle&sys_id={{data.sys_id}}`

 If you're changing a custom mapping that was defined in a previous release using the **com.glide.cs.portal\_url\_mapping.\_default.&lt;table&gt;** system property, you do not need to specify a **Value**.

</td></tr></tbody>
</table>5.  Select **Save** to enter a new mapping or update an existing mapping.


**Parent Topic:**[URL navigation in Conversational Interfaces](../concept/url-navigation-ci.md)

