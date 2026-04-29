---
title: Publish an app from App Engine Studio when linked to source control
description: You can publish a custom application from App Engine Studio \(AES\) when linked to source control.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Publish your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Publish an app from App Engine Studio when linked to source control

You can publish a custom application from App Engine Studio \(AES\) when linked to source control.

## Before you begin

Role required: admin

## About this task

When you publish an application from App Engine Studio that is linked to source control, there is a different outcome than when you publish via the sys\_app or sys\_store\_app **Publish** related link.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  From the app home, select **Publish**.

    App Engine Studio displays the publish app fields.

    ![Provide a version number and release notes for your app.](../image/publish-app-form-purple.png)

4.  Enter the following field values.

<table id="table_skj_zxl_s5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Version

</td><td>

View your current app version and provide a new version number for your application.**Note:** To change the version number, you must have one of the following deployment permissions: **Submit for deployment**, **Publish to app repo**, or **Publish to app store**

</td></tr><tr><td>

Release notes

</td><td>

Provide a brief description of the changes made to your application.

</td></tr><tr><td>

Publish options

</td><td>

Select if you want the application to be published to your application repository or the ServiceNow Store.

</td></tr></tbody>
</table>    **Note:** All application developers on the instance share the credential used to link a Git repository to an application.

5.  Select **Continue**.

6.  The current state of the application is committed to source control, including any untracked or uncommitted changes.

    The value of the **glide.sourcecontrol.default\_commit\_mode** property is ignored.

    This occurs because when the application is published, all the untracked and uncommitted changes are also published. Therefore, the state of the application in the Git repository matches what is published. See the [Commit changes to a repository](source-control-commit-changes.md) topic for more information about the **glide.sourcecontrol.default\_commit\_mode** property.

7.  A source control tag is created for the new version and the application is published.

    If needed, the sys\_app record is updated with the new store correlation ID.

    **Note:** If your application is linked to source control and you publish a new version outside of App Engine Studio, a source control commit and tag are not created.


**Parent Topic:**[Publish your app](../concept/publish-your-app.md)

