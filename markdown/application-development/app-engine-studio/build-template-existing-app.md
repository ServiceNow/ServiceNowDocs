---
title: Build a custom template from an existing application
description: Use an existing application as a starting point to build a custom template in App Engine Studio \(AES\). Existing data, experience, logic and automation, and security roles from the application are automatically added to the custom template.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Build a custom template, Use an app template, Create your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Build a custom template from an existing application

Use an existing application as a starting point to build a custom template in App Engine Studio \(AES\). Existing data, experience, logic and automation, and security roles from the application are automatically added to the custom template.

## Before you begin

Role required: admin, app\_template\_author

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the Template page, select **Create new template**.

3.  Select **Existing app**, and then select **Continue**.

4.  On the app selection screen, select an existing application for the custom template creation, and then select **Continue**.

    The following outcomes are possible.

    -   All items are supported: The custom template is created. All the objects are available in the custom template and in apps created from the custom template.
    -   Some items aren't supported: You can continue to create the template but a few items are not available in the custom template. There’s no impact on the custom template or the apps created from the template.
    -   Some items are denied: You encounter an error message and cannot continue further until the errors are fixed. The author must change the app, if it was created from an existing app or the template, if it was created from scratch.
    **Note:** For more information, see [Supported features and metadata in custom templates](../reference/supported-features-metadata-custom-templates.md).

5.  Enter a name and description for the custom template.

6.  Accept or change the application's logo.

    -   If the existing application has a logo in SVG format, the same logo is applied to the custom template.
    -   If there’s no logo or the logo is in a format other than SVG, upload an SVG logo for the custom template by either dragging the image to the **Browse or drag an SVG image** field or selecting the field, selecting the image from your file directory, and selecting **Open**.
7.  Select **Continue**.

8.  Specify which users or groups should have access to this template.

<table id="choicetable_m5y_2nz_5tb"><tbody><tr><td id="d265613e181">

**Share with specific users and groups**

</td><td>

1.  From the **Shared with** list, select **Specific users and groups**.
2.  Add users individually or in groups.
3.  Select **Give access**.
4.  Select **Continue**.


</td></tr><tr><td id="d265613e217">

**Share with all users and groups**

</td><td>

1.  From the **Shared with** list, select **All users and groups**.
2.  Select **Continue**.


</td></tr></tbody>
</table>    For more information about template sharing and permissions, see [App template sharing](../concept/app-template-sharing.md#).

9.  Access the custom template in one of the following ways.

    |Option|Action|
    |------|------|
    |**Go to all templates**|Access custom templates from the template library.|
    |**View template**|Access the custom template you just created.|


## Result

Your custom template is created and ready for your use. The custom template is activated and is available to App Engine Studio users who have access to it.

**Parent Topic:**[Build a custom template](../concept/build-custom-template.md)

