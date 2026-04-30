---
title: Add a portal
description: Create a portal in App Engine Studio \(AES\) to give your users a site where they can find information, create requests, and complete business tasks.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Add an application experience, Enhance your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Add a portal

Create a portal in App Engine Studio \(AES\) to give your users a site where they can find information, create requests, and complete business tasks.

## Before you begin

Role required: sn\_app\_eng\_studio.user or delegated\_developer. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

When you add a portal you're creating a basic version of it, which you must then continue editing in UI Builder before it's ready to deploy.

**Note:** If you created an application using a template, a portal may already be added to your application.

Most companies implement a maximum of three portals, which they then populate with catalogs.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  In your application, next to Experience, select **Add**.

4.  Select **Portal**, and then select **Begin**.

5.  On the form, fill in the fields.

<table id="table_wnj_dkh_14b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the portal. By default, the portal shares the same name as your application.**Tip:** Use a name that uniquely identifies the portal from other experiences. For example, `Office art portal`.

</td></tr><tr><td>

Description

</td><td>

Description of the portal.

</td></tr><tr><td>

URL

</td><td>

Web address of the portal. By default, the URL is based on the application name.

</td></tr><tr><td>

Roles

</td><td>

User roles to limit who can access the portal. To use a custom role for your portal, you must create one in **Security** first. For more information, see [Add application security](../concept/add-security.md).

</td></tr></tbody>
</table>6.  Select **Continue**, and then select **Done**.

    After you create the portal in AES, you must edit it in UI Builder by adding or configuring components on each page.

7.  Next to the portal you created, select the menu icon \(![Menu icon](../image/menu-icon-purple.png)\) and then select **Edit**.

    ![Edit a portal to make changes to it](../image/aes-edit-portal-purple-update.png "Edit a portal")

8.  In UI Builder, edit the portal by adding or configuring components on each page.

    You can also add more pages to the portal, if needed.

    **Note:** The default portal pages are read-only and can't be edited. To change the content of each page, create a page variant and edit the variant.


## What to do next

For more information on using UI Builder to edit portals, see [UI Builder](../../../administer/ui-builder/concept/ui-builder-overview.md).

-   **[Sample portals you can build](../concept/portal-example.md)**  
A portal is a site where users inside of your organization can find information, submit requests, and complete business tasks.

**Parent Topic:**[Add an application experience](../concept/add-experience.md)

