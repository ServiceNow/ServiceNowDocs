---
title: Configure input form pages
description: Create input form pages to enable users to view data over multiple organized pages, rather than scrolling through a long list of entries. Input form pages host data from inputs and sections. You control the layout of the pages, and which inputs and sections belong to each page of the input form screen.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure input form pages

Create input form pages to enable users to view data over multiple organized pages, rather than scrolling through a long list of entries. Input form pages host data from inputs and sections. You control the layout of the pages, and which inputs and sections belong to each page of the input form screen.

## Before you begin

You must create an input form screen that contains inputs before you create pages. For information about creating an input form screen and inputs, see [Configure an input form screen](parameter-screen-config.md) and [Configure input form screen inputs](param-screen-config-inputs.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category and then select the input form screen for which you want to configure a page.

4.  Scroll down to the **Input form page display** section and make sure that **Custom page and section setup** is selected.

    If **Custom page and section setup** is not selected, the option to configure Pages does not appear in the form.

5.  Scroll down to the Pages section of the form and select an existing Page name or select **New** to configure a new input form screen page.

    The Input Form Page appears.

6.  Complete the following fields as needed.

<table id="table_zy2_y1v_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of your page. This name appears as the title of your mobile app page.

</td></tr><tr><td>

Title

</td><td>

The displayed title for the input form screen page. You can have a different title for each page you configure.

</td></tr><tr><td>

Order

</td><td>

Enter a number to define the placement order of the page.**Note:** An input form page displays variables and sections according to the number entered. Sections and variables do not have priority over each other.

</td></tr><tr><td>

Active

</td><td>

Whether the input form screen page is active. Inactive pages do not appear on the input form screen.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  Map inputs to designated pages.

    1.  Select the input form screen where you want to use the page you configured.

        The input form screen appears.

    2.  Scroll down to the Inputs section and select the input you want to map to a page.

    3.  In the Input form, scroll down to the Input placement section, and make sure the Input form screen you want to use if selected.

    4.  In the Input form page field, select the page to which you want to map this input.

9.  Select **Save**.


## Result

An input form screen can contain any number of pages. Each page can comprise inputs and reusable sections.

![Input form screen displaying two pages containing inputs and sections.](../image/input-form-screen-pages.png)

