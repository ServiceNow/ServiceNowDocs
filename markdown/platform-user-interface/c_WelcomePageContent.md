---
title: Welcome pages
description: The welcome page contains instructions and any important information you would like to convey to your customers each time they log in to use the system.You can create company-specific welcome page content.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Welcome pages

The welcome page contains instructions and any important information you would like to convey to your customers each time they log in to use the system.

The base system login page content is customizable by the administrator of the system.

**Note:** This information is only relevant for instances using Core UI instead of the Next Experience. For information about similar options available for Next Experience, see [Edit login theming in Next Experience](../task/edit-login-features-u-n.md).

## Welcome page sections

Welcome pages can contain different sections, including:

-   **Welcome:** General information
-   **Using:**Some tips and tricks for using the system
-   **Login:** Login information
-   **Demonstration:** Information about logging in to a base system demo system
-   **More Information:** A link to the ServiceNow documentation

View, create, and configure the welcome page sections by navigating to **System UI** &gt; **Welcome Page Content**. You can edit any item by clicking its short description. Sections that are not needed can be removed.

|Field|Description|
|-----|-----------|
|Short Description|A description of the section.|
|Active|Mark the section active to display it on the welcome page. Inactive sections are not visible.|
|Display order|A number representing the order in which sections are displayed. Lower numbered sections are displayed above higher numbered sections.|
|Application|The application to which the section belongs.|
|Language|The section appears when the logged in users language matches this value. If no user is logged in, the guest user's language preference is used.|
|Condition|The section appears on the welcome page when the script in this field evaluates to true.|
|Published|The published date of the section.|
|Text|The content of the section.|

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

## Create company-specific welcome page content

You can create company-specific welcome page content.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Welcome Page Content**.

2.  To create a new section, click **New**.

3.  Enter the following in the **Condition** field, where Company is the name of the company whose users see this section.

    ```
    gs.getUser().getCompanyRecord().name.toString() == "Company"
    ```

4.  Complete the form.

5.  Click **Submit**.


