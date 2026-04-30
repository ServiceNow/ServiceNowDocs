---
title: Configure search resource context properties
description: Configure the properties to limit the search to a specific catalog or knowledge base. For example, if you want to limit the knowledge search to an IT knowledge base or a service catalog search to software service catalog, you can configure the properties.
locale: en-US
release: zurich
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Contextual search, Search administration, Configure core features, Administer]
---

# Configure search resource context properties

Configure the properties to limit the search to a specific catalog or knowledge base. For example, if you want to limit the knowledge search to an IT knowledge base or a service catalog search to software service catalog, you can configure the properties.

## Before you begin

Role required: admin

## About this task

The following procedure uses Incident Deflection as an example.

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Search Contexts**.

2.  Open the Incident Deflection record.

3.  View the Resource Configurations related list.

    ![Resource Configurations related list on Search Context form.](../image/resource-configuraion-related-list.png)

    In the Resource Configurations related list, edit a resource configuration record to view the properties of the search resource.

    The **knowledge** record displays the following knowledge resource configuration properties:

    |Property|Description|
    |--------|-----------|
    |Condition|Conditions to specify one or more knowledge bases to search.|
    |Exclude pinned articles|Pinned article is a knowledge article. This property helps to decide whether to exclude pinned articles from knowledge base search or not.|

    The **catalog** record displays the following catalog resource configuration properties:

<table id="table_khp_ypb_lhb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog name

</td><td>

A catalog name to search the catalog items.

</td></tr><tr><td>

Search operator

</td><td>

Value of the operator is used in the Zing search engine to instruct how to combine the AND and OR conditions when parsing the search string. The integration of the search strings helps to [score](../../search-administration/concept/c_DocumentScoring.md) the displayed results. The value can only be one of the following values: -   **IR\_AND\_OR\_QUERY** \(the default\): Display results with exact matches of all terms if the number of results is greater than the value of the **glide.ts.query.and\_or\_limit** property \(default 0\) or the \(overriding\) value of the table custom attribute **text\_search\_and\_or\_limit** \(when added\). Otherwise display results with any matches of any terms.
-   **IR\_AND\_QUERY**: Display results with exact matches of all terms only.
-   **IR\_OR\_QUERY**: Display results with any matches of any terms.


</td></tr></tbody>
</table>4.  To edit the value of any property, click the property name and in the Search Resource Context Property form, update the **Value** field to `true` or `false`.

    ![Search resource context property](../image/search-resource-context-property.png)

5.  Click **Update**.


**Parent Topic:**[Configuring contextual search](../concept/configuring-contextual-search.md)

