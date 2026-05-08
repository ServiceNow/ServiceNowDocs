---
title: Create a page variant
description: A page variant in UI Builder is a variation of a page that exists at the same path that targets different audiences using user criteria.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create a page variant

A page variant in UI Builder is a variation of a page that exists at the same path that targets different audiences using user criteria.

This video show you how to perform the following procedure.This video shows you how to create a page variant.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Learn how to create a page variant in UI Builder. A page variant is based on your page with content targeted for a different audience. For example, you can create a homepage for agents, and a variant of that page for managers of those agents. The variant exists at the same URL.

-   When someone who is part of the application admins audience accesses the page URL, the user sees a version of the page that has application admin-specific details, such as application metrics and usage details. For the Special Occasions application the page would show how many users have birthdays and work anniversaries and how many do not. The page would also show how many issues have been reported with special occasions.

-   When someone who is part of the department managers audience accesses the page URL, the user sees department-related information for the application, such as people in their department with upcoming birthdays and work anniversaries, and whether or not those people are okay with their special occasions being shared.

-   When someone who is part of the application users audience accesses the page URL, the user sees a user-specific version of the page with their special occasions that allows them to configure whether or not they want others to see their special occasions.


## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open the experience with the page for which you want to create a variant.

3.  Select the **+** icon in the **Pages** section.

    ![Create page button on the experience view page.](../image/create-page-icon.png)

4.  Select **Add a variant to a page**.

5.  Click **+ Add variant**.

    ![Add variant button to create a variant of a page in UI Builder.](../image/uib-add-variant-button.png)

6.  Click **Build from scratch instead** or select **Use template** when pointing to the template that you want to use.

7.  Enter a name for the variant page.

    The name can be similar to your page name, or what ever you want it to be.

    **Note:** The application scope defaults to the scope that the user is in within the ServiceNow AI Platform®. For more information about application scope, see [Learn about security and roles](security-roles.md).

8.  Specify one or more audiences for your variant page by selecting **Add an audience**.

    The audience is important because it lets you assign your page variant to a specific role or group. If an audience you need is not listed, create one by selecting **View all available audiences**, and then selecting **New**.

9.  Declare conditions for when to display the page by either using the provided dropdown menus or writing an encoded query string.

    To learn more about declaring conditions, see [Control the conditions for a page variant](control-conditions-for-your-variant.md). For more information on writing encoded queries, see Encoded query strings.

10. If creating a page from scratch, select **Continue** and then select the **Build responsive** option \(default\).

11. Click **Create** to create your page variant.


-   **[Edit page variant settings](edit-variant-settings.md)**  
Edit page variant settings to add additional criteria to determine when the page variant displays to users.
-   **[Control the conditions for a page variant](control-conditions-for-your-variant.md)**  
Set the conditions and manage the criteria that determine when a page variant is displayed. UI Builder page variants enable you to create different versions of a page to tailor content for a specific audience.

**Parent Topic:**[Manage UI Builder pages and page variants](../concept/work-pages.md)

