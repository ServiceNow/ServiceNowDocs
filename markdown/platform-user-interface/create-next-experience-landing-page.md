---
title: Create a Next Experience landing page
description: Provide users the information that they need to start working by creating custom Next Experience landing pages for different audiences.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Landing pages, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Create a Next Experience landing page

Provide users the information that they need to start working by creating custom Next Experience landing pages for different audiences.

## Before you begin

Creating custom Next Experience landing pages requires configuring page components in UI Builder. For a quick tutorial on using UI Builder, see [UI Builder quick start](https://www.servicenow.com/docs/access?context=ui-builder-quick-start&version=zurich&pubname=zurich-application-development&ft:locale=en-US) in the UI Builder documentation.

Role required: ui\_builder\_admin or admin

## About this task

Administrators can set various types of pages as the start pages that different users see when they log in to an instance. By default, a Next Experience landing page is the start page for all users.

To customize a Next Experience landing page for different audiences and use cases, you can create a variant of the default Next Experience landing page using UI Builder, as described in this procedure. You can also create a Next Experience landing page from scratch by creating a new page in UI Builder.

**Note:** This procedure doesn’t apply to creating landing pages for Configurable Workspaces.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  From the Experiences list, select **Unified Navigation App**.

3.  In the Pages and variants list, under Home, select either **Next Experience Landing Page** or **Next Experience Landing Page - Admin Role**.

    The Next Experience Landing page is the default landing page for non-admin users, and the Next Experience Landing Page - Admin Role is the default landing page for admin users. Select the page that aligns with the audience for which you need to create a custom landing page.

4.  From the top bar, change the application scope you work in by selecting the application scope from the application picker.

5.  Create a variant of the default landing page by duplicating it.

    1.  From the left vertical bar, select the context menu and then select **Duplicate variant**.

        ![Duplicate the Next Experience default landing page](../image/duplicate-landing-page.png)

    2.  In the **Name** field, enter a name for the page variant.

    3.  Next to the **Audiences** field, select **Add** and then select an audience from the list.

        The audience defines who can see a page. By default, all users can see a page. For more information about audiences, see [Learn about audiences](https://www.servicenow.com/docs/access?context=add-audiences&version=zurich&pubname=zurich-application-development&ft:locale=en-US) in the UI Builder documentation.

    4.  In the **Conditions** field, add criteria for when to display the page by entering an encoded query string.

        For example, the query string `table=incident^sysId!=-1` will only show this page variant if the table field is incident and the sysId field isn’t -1.

    5.  Select **Create**.

6.  Customize the components on the page according to the needs of your audience.

    You can customize what components are included on the page, the data they connect to, their style, and event mappings. To learn more about how to customize components on a page, refer to [Customize UI Builder pages using components](https://www.servicenow.com/docs/access?context=work-components&version=zurich&pubname=zurich-application-development&ft:locale=en-US) in the UI Builder documentation.

    To enable a footer for the page, see [Configure a Next Experience landing page footer](configure-next-experience-landing-page-footer.md).

    ![Customize the landing page in UI Builder staging](../image/create-landing-page.png "Customize a landing page in UI Builder")

7.  Select **Save**.

8.  Set this page variant as the start page for the selected audience.

    1.  From the top bar, select **Settings**.

    2.  In the **Order** field, set the priority order of the page variant to a lower number than the order of the default Next Experience landing page.

        By default, the order of the default Next Experience Landing page is set to 1000, and the order of the Next Experience Landing Page – Admin is set to 99. The lower the number, the higher the priority.

    3.  Select **Save**.


**Parent Topic:**[Next Experience landing pages](../concept/next-experience-landing-pages.md)

