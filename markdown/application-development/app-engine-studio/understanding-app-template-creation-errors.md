---
title: Identifying and fixing app template creation errors
description: Learn how to identify and fix your app when unsupported features or metadata stop the template creation process in App Engine Studio \(AES\).Errors that occurred during the creation of a custom template that are displayed in the Scan Failure \[sys\_app\_scan\_failure\] table and their cause.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Build a custom template, Use an app template, Create your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Identifying and fixing app template creation errors

Learn how to identify and fix your app when unsupported features or metadata stop the template creation process in App Engine Studio \(AES\).

## Unsupported features

Sometimes items in a source application from which you created a custom template aren’t supported in the template. You must remove unsupported items before you can create a template from the application.

When an error happens during the template creation process, an error message is displayed.

![Template creation failure notification](../image/template-errors-purple.png "Template creation failure notification")

You can identify which elements of your application are causing it to fail the template creation process by selecting **View all errors**, which displays the Scan Failure \[sys\_app\_scan\_failure\] table. For more information about the errors in the table and their cause, see [Template creation errors in the Scan Failure table](understanding-app-template-creation-errors.md#).

**Parent Topic:**[Build a custom template](build-custom-template.md)

## Template creation errors in the Scan Failure table

Errors that occurred during the creation of a custom template that are displayed in the Scan Failure \[sys\_app\_scan\_failure\] table and their cause.

### Error messages

For more information about what types of records are allowed and skipped, see [Supported features and metadata in custom templates](../reference/supported-features-metadata-custom-templates.md).

<table id="table_jyq_4qt_z5b"><thead><tr><th>

Error message

</th><th>

Definition

</th><th>

More details

</th></tr></thead><tbody><tr><td>

Unsupported\_table

</td><td>

Record class for which there is no allow rule, and there’s an unknown level of support.

</td><td>

One or more unsupported records are unrecognized by App Engine Studio and must be removed for the template creation process to continue.

</td></tr><tr><td>

Denied\_table

</td><td>

Record class for which there is a deny rule, and template creation isn’t supported.

</td><td>

The record class is explicitly denied and must be removed for the template creation process to continue.

</td></tr><tr><td>

Scripted\_record

</td><td>

Scripted rule that runs on each record in the app.

</td><td rowspan="2">

Current scripted deny rules include, but aren't limited to:-   Custom metadata: The app has tables that extend the sys\_metadata table.
-   Scoped administration: The app has scoped administration turned on.
-   Template execution in progress: The template associated with the source app is currently being executed.

</td></tr><tr><td>

Scripted\_app

</td><td>

Scripted rule that runs once for the app.

</td></tr></tbody>
</table>