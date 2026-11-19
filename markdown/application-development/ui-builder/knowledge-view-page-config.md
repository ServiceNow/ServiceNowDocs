---
title: Knowledge View page template configuration
description: Knowledge View is a page template that displays the contents of a knowledge article with configurable interactive features, such as user comments and a rating scale. An administrator configures these features using properties in a platform table and not in UI Builder.To configure options on the Knowledge View page, you must create the properties and set their values. These properties are not global and affect only the workspace you specify.Configure these Knowledge View properties for your workspace. The property definitions also show the corresponding global system property, if one exists.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/knowledge-view-page-config.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Knowledge View page template configuration

Knowledge View is a page template that displays the contents of a knowledge article with configurable interactive features, such as user comments and a rating scale. An administrator configures these features using properties in a platform table and not in UI Builder.

Pages are built in UI Builder using a template. For instructions on accessing UIB and selecting the page template you want, see [Create a page from a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/reuse-page-definitions.md) or [Create a page from a legacy template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/legacy-templates.md).

## How to use the template

Create a new page from this template in UI Builder, and choose one of the following options:

-   **Use the original template**: References the template in your page. When the template is updated for a new release, your page gets the updates automatically. This selection permits limited customizations but is the safest choice.
-   **Copy template contents**: Allows you to change the property values for the components used in the page. When you copy a template, you don't get any of the changes when the template is automatically updated for a new release.

## Global vs. workspace properties

The ServiceNow platform provides global system properties \(System Properties \[sys\_properties\]\) that control display characteristics of the information presented on an article view page and the options available to users. To set different values for these properties for a specific workspace, you create records for page properties in the UX Page Property \[sys\_ux\_page\_property\] table. For information about these properties, see [Knowledge Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/r_KnowledgeProperties.md).

**Important:** If the global property controlling a Knowledge View feature is set to **false**, you can't set the corresponding local property to **true** for a workspace.

**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Knowledge View component properties

To configure options on the Knowledge View page, you must create the properties and set their values. These properties are not global and affect only the workspace you specify.

### Before you begin

Role required: admin

### Procedure

1.  In the navigation filter, search for **sys\_ux\_page\_property.list**.

    The list of page properties appears.

2.  Select **New**.

    The UX Page Property form appears.

3.  In the **Page** field select the workspace to which this property applies.

    In this case, select **CSM/FSM Configurable Workspace**.

4.  In the **Name** field, enter the name of the property you want to add from the table below.

5.  Select the data type for the property in the **Type** field.

6.  In the **Value** field, enter the value for the property.

7.  In the **Route** field, select **Knowledge View** from the list.

8.  Add a description for the property from the table below.

9.  Select **Submit** to create the property and apply its value to the Knowledge View page.

    \[Omitted image "knowledge-view-property-form.png"\] Alt text: Shows a completed form for creating and configuring the 5 star rating scale for a knowledge article


## Knowledge view property definitions

Configure these Knowledge View properties for your workspace. The property definitions also show the corresponding global system property, if one exists.

<table id="table_bdm_z14_rpb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

showFlag

</td><td>

Show or hide the menu option enabling users to flag an article that contains incorrect or inappropriate content. By default, this global option is set to **true** by the **glide.knowman.show\_flag** system property.

 \[Omitted image "knowledge-view-flag-article.png"\] Alt text: Shows the menu option in a knowledge article that allows users to flag incorrect or inappropriate content

</td></tr><tr><td>

showHelpful

</td><td>

Show or hide the dialog box enabling users to indicate whether or not an article was helpful.By default, this global option is set to **true** by the **glide.knowman.show\_yn\_rating** system property.

 \[Omitted image "knowledge-view-helpful.png"\] Alt text: Shows the dialog box allowing users to indicate if an article has been helpful or not

</td></tr><tr><td>

showRelatedArticles

</td><td>

Show or hide the panel containing knowledge articles related to the current article. The Related Articles panel is displayed by default. There is no corresponding system property.\[Omitted image "knowledge-view-related-articles.png"\] Alt text: Shows the related articles panel that can be configured to display in a knowledge article

</td></tr><tr><td>

showRating

</td><td>

Show or hide the rating scale at the bottom of a knowledge article. Users select 1-5 stars to evaluate the article.By default, this global option is set to **true** by the **glide.knowman.show\_star\_rating** system property.

 \[Omitted image "knowledge-view-star-rating.png"\] Alt text: Shows the 5 star rating scale for evaluating a knowledge article

</td></tr><tr><td>

showComments

</td><td>

Show or hide comments about the current article from other users.By default, this global option is set to **true** by the **glide.knowman.show\_user\_feedback** system property.

 \[Omitted image "knowledge-view-comments.png"\] Alt text: Shows the container with user comments about the current article

</td></tr><tr><td>

MaxRelatedArticles

</td><td>

Sets the maximum number of entries shown in the Related Articles panel.By default, 5 related articles are displayed. There is no corresponding system property.

</td></tr></tbody>
</table>