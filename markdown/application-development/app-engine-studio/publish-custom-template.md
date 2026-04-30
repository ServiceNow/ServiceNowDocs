---
title: Publish a custom template
description: You can publish a custom template that is built from scratch or from an existing application using App Engine Studio \(AES\).
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Build a custom template, Use an app template, Create your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Publish a custom template

You can publish a custom template that is built from scratch or from an existing application using App Engine Studio \(AES\).

## Before you begin

You must have permissions to publish a custom template. For details, see [Assign permissions to publish custom templates](../concept/assign-permissions-publish-custom-templates.md#).

Role required: admin, app\_template\_author

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio** &gt; **Templates**.

2.  Point to the custom template, select the More actions icon \( ![More actions icon.](../image/menu-icon-purple.png)\), and select **Properties**.

3.  On the **General** tab, select the **Activate this template** check box.

4.  Select **Publish template**.

5.  For a custom template built from scratch, select **Publish anyway**.

    App Engine Studio displays the publish template fields.

6.  Fill in the fields.

<table id="table_tfw_nzh_psb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Version

</td><td>

Provide a new version number for the custom template.

</td></tr><tr><td>

Release notes

</td><td>

Provide a brief description of the changes made to the custom template.

</td></tr><tr><td>

Publish options

</td><td>

Select where you want the custom template published.-   To publish the template to your application repository, select **My application repository \(Make the app available to my instances\)**.
-   To publish the template to the ServiceNow Store, select **ServiceNow Store \(Submit this app to the ServiceNow Store for review\)**.


</td></tr></tbody>
</table>7.  Select **Continue**.

8.  On the confirmation screen, select **Close**.


## Result

The custom template is published and available to users the app template admin shares it with.

**Parent Topic:**[Build a custom template](../concept/build-custom-template.md)

