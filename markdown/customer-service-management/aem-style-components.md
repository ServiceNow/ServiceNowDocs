---
title: Customizing the colors of ServiceNow components in AEM
description: You can define the look and feel of the ServiceNow components in Adobe Experience Manager \(AEM\) by specifying colors for them.Set the color theme for the ServiceNow components in Adobe Experience Manager \(AEM\) all at once by configuring the color variables.Override the color theme for a ServiceNow component in Adobe Experience Manager \(AEM\) by using the initialize function.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrating with Adobe Experience Manager, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Customizing the colors of ServiceNow components in AEM

You can define the look and feel of the ServiceNow components in Adobe Experience Manager \(AEM\) by specifying colors for them.

As an AEM administrator, you can either modify the color variables preconfigured for all components or use the initializeCSS function for customizing the colors of a particular component using a custom CSS class. You specify the custom CSS class for a component in the **Custom CSS Class** property. For more information, see [Display ServiceNow knowledge articles on an Adobe Experience Manager page](../task/aem-display-knowledge-components.md) and [Display ServiceNow cases on an Adobe Experience Manager page](../task/aem-display-case-components.md).

**Note:** By default, the ServiceNow components are configured using the Bootstrap v4.4.1 CSS styles. If your AEM page uses a different Bootstrap version, the ServiceNow components style is overridden by the page style.

## Modify the color theme for all ServiceNow components in AEM

Set the color theme for the ServiceNow components in Adobe Experience Manager \(AEM\) all at once by configuring the color variables.

### Before you begin

Role required: AEM administrator

### About this task

**Note:** By default, the ServiceNow components are configured using the Bootstrap v4.4.1 CSS styles. If your AEM page uses a different Bootstrap version, the ServiceNow components style is overridden by the page style.

### Procedure

1.  [Open CRXDE Lite in your browser](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/enabling-crxde-lite.html).

    For example, in your browser, enter the URL in the format `http://<AEM_hostname>:<AEM_port>/crx/de`. The default URL for CRXDE Lite is `http://localhost:4502/crx/de`.

2.  Navigate to **apps** &gt; **servicenow-components** &gt; **clientlibs** &gt; **clientlib-common**.

3.  Open the `variables.less` file.

4.  Configure the color variables available for the HTML elements in the ServiceNow components.

    |Color setting|Variable|
    |-------------|--------|
    |Text content|@text-color|
    |Hyperlinks|@link-color|
    |Badges|@badge-text-color|
    |Badges background|@badge-background-color|
    |Primary color for visual emphasis|@primary-color|
    |Color complementary to the primary color, for visual emphasis|@secondary-color|
    |Component titles|@title-color|
    |Primary button text|@primary-btn-text-color|
    |Primary button background|@primary-btn-bkg-color|
    |Secondary button text|@secondary-btn-text-color|
    |Secondary button background|@secondary-btn-bkg-color|

    **Note:** You specify a color for a variable in one of the following ways:

    -   Color name

        For example, `red`

    -   HEX value

        For example, `#FF0000`

    -   RGB value

        For example, `rgb(255,0,0)`

    -   var function

        Use the var function to specify a custom property for a color. For example, `var(--gray-dark)`.

5.  From the CRXDE Lite menu, click **Save All** to save the changes on the AEM server.


## Modify the color theme for a ServiceNow component in AEM

Override the color theme for a ServiceNow component in Adobe Experience Manager \(AEM\) by using the initialize function.

### Before you begin

Role required: AEM administrator

### About this task

The color variables specified in the `variables.less` file are applied to all ServiceNow components in AEM. You can override the default colors for a particular component by setting the color variables for the component in the initializeCSS function.

**Note:** By default, the ServiceNow components are configured using the Bootstrap v4.4.1 CSS styles. If your AEM page uses a different Bootstrap version, the ServiceNow components style is overridden by the page style.

### Procedure

1.  [Open CRXDE Lite in your browser](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/enabling-crxde-lite.html).

    For example, in your browser, enter the URL in the format `http://<AEM_hostname>:<AEM_port>/crx/de`. The default URL for CRXDE Lite is `http://localhost:4502/crx/de`.

2.  Navigate to **apps** &gt; **servicenow-components** &gt; **clientlibs** &gt; **clientlib-common**.

3.  Open the `variables.less` file.

4.  Specify the initializeCSS function for a component in the format `<component_type>;<class_name>;<color_variable_1>;<color_variable_2>;<color_variable_n>`.

    -   component\_type: The type of the component on which you want to apply the custom color theme, for example, articlelist, articleview, casecards, and so on.
    -   class\_name: The Custom CSS class you enter in the **Custom CSS class** property of your component.
    -   color\_variable\_1, color\_variable\_2, color\_variable\_n: The color variables that you specify for the HTML elements in a component. For more information, see the [Color variable settings](aem-style-components.md#table_vhh_gjm_2mb) table.
    Use the following sample code as a reference for color styling at the component level.

    ```
    .initialize(@componentType:articlelist;@className:now-article-list;@text-color:red; @link-color:orange;@badge-text-color:blue;@badge-background-color:yellow;@title-color:magenta;@secondary-color:indigo;);
    .initialize(@componentType:articleview; @className:now-article-view;@text-color:red; @link-color:orange;@badge-text-color:blue;@badge-background-color:yellow;@secondary-color:indigo;);
    .initialize(@componentType:casecards; @className:now-case-cards; @text-color:red;@link-color:orange;@badge-text-color:blue;@badge-background-color:yellow;@title-color:magenta;@secondary-color:indigo;);
    .initialize(@componentType:caselist; @className:now-case-list; @text-color:red; @link-color:orange;@title-color:magenta;@primary-color:green;@secondary-btn-text-color:white;@secondary-btn-bkg-color:black;);
    .initialize(@componentType:searchbox; @className:now-search-box; @text-color:red; @link-color:orange;@title-color:magenta;@primary-color:green;@secondary-btn-text-color:white;@secondary-btn-bkg-color:black;);
    .initialize(@componentType:searchresults;@className:now-search-results;@text-color:gray; @link-color:orange;@badge-text-color:blue;@badge-background-color:yellow;@title-color:magenta;@secondary-color:indigo;);
    .initialize(@componentType:caseview;@className:now-case-view;@text-color:red;@link-color:orange;@primary-color:green;@secondary-color:indigo;@primary-btn-text-color:blue;@primary-btn-bkg-color:white;@secondary-btn-text-color:white;@secondary-btn-bkg-color:blue;);
    .initialize(@componentType:createcase;@className:now-create-case;@text-color:red;@link-color:orange;@primary-color:green;@secondary-color:indigo;@primary-btn-text-color:blue;@primary-btn-bkg-color:white;@secondary-btn-text-color:white;@secondary-btn-bkg-color:blue;)
    ```

5.  From the CRXDE Lite menu, select **Save All** to save the changes on the AEM server.


