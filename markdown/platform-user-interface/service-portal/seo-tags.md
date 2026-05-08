---
title: Add meta tags to a public page
description: Improve the searchability of Service Portal pages by adding meta tags. You can add the meta name and description attributes to a page, define the robots attribute, or create dynamic meta tags for pages that load record data based on a URL parameter.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Improving search engine optimization for portals, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Add meta tags to a public page

Improve the searchability of Service Portal pages by adding meta tags. You can add the meta name and description attributes to a page, define the robots attribute, or create dynamic meta tags for pages that load record data based on a URL parameter.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Pages**.

2.  Open a page.

3.  Check that **Public** is selected.

    Pages that are not public are not indexed by external search engines.

4.  Click the **Meta tags** related list tab.

5.  Click **New** to create a new meta tag.

6.  Complete the form.

<table id="table_rt5_cqq_v1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Page

</td><td>

Page to apply the meta tag to.

</td></tr><tr><td>

Application

</td><td>

Application scope of the page. This value is read-only.

</td></tr><tr><td>

Name

</td><td>

The HTML meta name attribute.To define the meta robots attribute, add **ROBOTS**.

</td></tr><tr><td>

Content

</td><td>

The HTML meta description attribute. If **ROBOTS** is defined in the **Name** field, you can add one of the following content values:

 -   **INDEX, FOLLOW**: The search engine shows the page in search results and trusts any links in the page. This is the default value.
-   **NOINDEX, FOLLOW**: The search engine does not show the page in search results, but trusts any links in the page.
-   **INDEX, NOFOLLOW**: The search engine shows the page in the search results, but does not trust links in the page.
-   **NOINDEX, NOFOLLOW**: The search engine does not show the page in search results and does not trust links in the page.
 Alternatively, you can pass a variable into this field based on record data. For example, you can define a `%description` variable in this field, and create a content variable to populate the content tag with record data.

</td></tr></tbody>
</table>    ![A competed meta tag form for the sc_home page.](../image/add-tag.png)

7.  Click **Submit**.

    The meta information is added to the page header. For example:

    ```
    <meta name="description" content="Order something from the Service Catalog">
    ```

8.  Create a content variable to populate the content tag with record data.

    If the page loads record data based on one or more URL parameters, you can add meta tags generated from the record data.

    1.  Open a meta tag record and check that the **Content** field contains a variable, or add a variable.

        Depending on the available URL parameters and the meta tag you would like to define, you can add the following types of values:

        |Value types|Description|Example value|
        |-----------|-----------|-------------|
        |One URL parameter variable|Populates the content tag with the value defined in the associated content variables record.|`%description`|
        |More than one URL parameter variable|Populates the content tag with the values defined in the associated content variables records.|`%description %price`|
        |Static value and a URL parameter variable|Populates the content tag with a static value and the associated content variables record.|`Catalog item: %description`|

        ![A Meta Tag form that uses a variable in the Content field.](../image/content-var.png)

    2.  In the **Content variables** related list, click **New**.

        The **Content variables** related list is only available after saving the meta tag record.

    3.  Complete the form.

        Associate a field with a URL query parameter. When the value of the query parameter is used to display content, a field from the same record is used to generate the content tag. You can define the field to generate the content tag through the **Table field** field.

<table id="table_acv_cff_51b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The variable to store the value. Must begin with **%** and cannot contain spaces. This value must match one of the variables defined in the **Content** field in the Meta tag record.

</td></tr><tr><td>

Application

</td><td>

Application scope of the page. This value is read-only.

</td></tr><tr><td>

Metatag

</td><td>

The meta tag to apply the dynamic variable to.

</td></tr><tr><td>

URL query parameter

</td><td>

URL parameter to indicate the record that is being displayed. You can enter any string.**Tip:** To create a URL parameter that is meaningful and easily identifiable, use a field name from the record. For example, to refer to a knowledge article, you can enter `number` to reference the article by its number.

</td></tr><tr><td>

Relevant table column

</td><td>

Table field to match the URL query parameter. For example, if you entered `number` to reference a knowledge article by its number, select **Number**. If left blank, the system uses the record sys\_id.

</td></tr><tr><td>

Table

</td><td>

The source table of the URL query parameter record.

</td></tr><tr><td>

Table field

</td><td>

Select a field from the table defined in the **Table** field. This field is used to generate the value of the content tag.**Important:** To support SEO, ensure that the referenced table field is public. For more information on granting access to a table field, see [Create an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr></tbody>
</table>        If more than one content variables match a variable defined in the **Content** field of the meta tag record, the record with the earliest Created date is used.

    4.  Click **Submit**.

        ![A competed content variable form that populates the description tag with the value of a sys_id parameter.](../image/new-content-var.png)

    The content tag loads record data. For example:

    ```
    <meta name="description" content="Apple iPad 3">
    ```


**Parent Topic:**[Improving search engine optimization for portals](../concept/seo-sp.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](t_ConfigureAPage.md#)

