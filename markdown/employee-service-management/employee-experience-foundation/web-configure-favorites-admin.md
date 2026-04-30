---
title: Configure favorites option
description: Configure the favorites option to help employees personalize the content and easily access the content they frequently use.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Cross-channel favorites, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Configure favorites option

Configure the favorites option to help employees personalize the content and easily access the content they frequently use.

## Before you begin

Role required: sn\_hr\_sp.esc\_admin and sp\_admin

## About this task

You can set up the favorite card details and use the default favorite icon ![default favorite icon default without selection](../images/myfav-no-selection.jpg) to bookmark content as your favorites. When your employees mark content as favorites, the favorite icon appearance changes to ![default favorite icon default with selection](../images/myfav-selection.jpg).

## Procedure

1.  Navigate to **All** &gt; **Favorites** &gt; **Favorite content configuration**.

2.  Click **New** or update an existing configuration.

3.  On the form, fill in the fields.

<table id="table_nyf_nvh_sqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content Type

</td><td>

The type of content on which the favorites icon can appear. The following content types have the favorite icon by default:-   **Requests**
-   **Articles**
-   **Applications**
-   **Topic page**


</td></tr><tr><td>

Table

</td><td>

Name of the table from which the data is fetched.

</td></tr><tr><td>

Application

</td><td>

The scope of application.

</td></tr><tr><td>

Order

</td><td>

Order in which you want the favorites content to appear.**Note:** The order in the favorite content configuration table doesn’t determine the sequence in which content types appear on the navigation of the Browse favorites section of the ESC portal. See [Manage favorites](web-configure-favorites-employee.md).

</td></tr><tr><td>

Active

</td><td>

Option to activate the favorite functionality on the associated content type.

</td></tr><tr><td>

Condition

</td><td>

Conditions to meet for the Favorite functionality. The conditions available are dependent on the table that you select.

</td></tr><tr><td>

Display Configuration

</td><td>

Display settings for the favorite card. Select appropriate configuration to display on the favorite card. Ensure you select minimum fields for performance improvement.-   **Availability**: The available options are:
    -   Mobile only
    -   Desktop only
    -   Desktop and mobile
-   **Primary field to display** \(Mandatory\): Select name or short description.
-   **Secondary fields to display** \(Optional\): Description of article or catalog item.
-   **Image**
-   **Image URL**

**Note:** When content type has both the image and image URL, the image takes precedence to display.

**Note:** **For optimal performance**, use the primary field and do not specify other fields.

</td></tr><tr><td>

Navigation Configuration

</td><td>

Navigational settings for the favorite icon. Select the following options: -   **Navigation type**
-   **Internal** You can specify the portal page and parameters for navigation.
-   **Specify Portal page**: You can select from the available options such as Page ID or Field. Based on your selection, provide any additional parameters:
    -   **Portal page**
    -   **Field**
    -   **Template**
-   **URL parameters**: Specify the parameters as required.
-   **External**The user selects the external navigation type between URL and field. For **URL**, the user specifies the URL and parameters \(if any\). For **Field**, the user selects the field from the table.


</td></tr></tbody>
</table>    **Note:** When you experience performance issues, use the primary field and do not specify other fields such as Image and image URL.

4.  Click **Submit**.


## Result

The favorites appears on the Employee Center and MESP portal.

Here's a sample illustration of how the configuration looks on the **Favorites** and the message when a favorites is not available for your access.

![Primary and secondary field to display for Favorites](../images/z-ec-favorites-card.png "Favorites card and access")

For more information on how Favorites appear, see [Manage favorites](web-configure-favorites-employee.md).

