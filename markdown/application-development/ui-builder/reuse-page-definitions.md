---
title: Create a page from a template
description: Use a template to create a page based on a pre-defined page template. A page template can help you create pages faster and keep pages consistent within an experience. Page templates may include components, data resources, and a layout.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/ui-builder/reuse-page-definitions.html
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a page in UI Builder, Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create a page from a template

Use a template to create a page based on a pre-defined page template. A page template can help you create pages faster and keep pages consistent within an experience. Page templates may include components, data resources, and a layout.

This video shows you how to perform the following procedure.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Select a page template when creating a page in your experience. After creating a page from a template, you can customize the page to your needs. Page templates include controllers that can be used with component presets. See [Bind data to UI Builder pages using controllers \(advanced feature\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/ui-builder/controllers.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Select the **+** icon in the **Pages and variants** section.

    \[Omitted image "create-page-icon.png"\] Alt text: Create page button on the experience view page.

4.  Select **Create a new page**.

    \[Omitted image "page-create-popup.png"\] Alt text: Page type selection modal.

5.  Select **Use template** when pointing to the template that you want to use.

    \[Omitted image "template-select.png"\] Alt text: Standard record template selected in the page creation wizard.

6.  Enter a unique name for the page in the **Name** field.

7.  Specify a path for your page in the **Path** field. UI Builder generates a default path based on the name that you provided in the previous step.

    A default path is added based on your page name. You can also create your own path. The path is required and must be unique. The path can include digits \(0-9\), letters \(A-Z, a-z\), and a few special characters \(`"-"`, `"."`, `"_"`, `"~"`\), with the words separated by a forward slash or hyphen. The **URL preview** shows the path of your page.

    \[Omitted image "template-page-settings.png"\] Alt text: Name and URL path fields.

    **Note:** The application scope defaults to the scope that the user is in within the ServiceNow AI Platform®. For more information about the application scope, see [Learn about security and roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/ui-builder/security-roles.md).

8.  Select **Continue**.

9.  Review the page parameters included in the template.

    For more information about required and optional page parameters, see [Adding Page Parameters](https://developer.servicenow.com/dev.do#!/learn/courses/washingtondc/app_store_learnv2_uibuilder_washingtondc_ui_builder/app_store_learnv2_uibuilder_washingtondc_create_pages_in_ui_builder/UCP_AddingPageParameters_washingtondc) in the ServiceNow Developer website.

10. Select **Looks good**.

11. Enter a name for the page variant.

    The first variant you create is named **Default** by default.

12. Add one or more audiences for this page.

    If an audience you need is not listed, you can choose the Open audiences in platform link to create one.

13. Declare conditions for when to display the page \(this variant\) by either using the provided dropdown menus or writing an encoded query string.

    For more information on writing encoded queries, see [Encoded query strings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/c_EncodedQueryStrings.md).

14. Select **Create** to create your page from template.

    The page you created displays in the **Page and variants** section of your experience. Select **Editor** to start adding components to your page. For more information, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/ui-builder/work-components.md).


**Parent Topic:**[Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/ui-builder/create-page.md)

