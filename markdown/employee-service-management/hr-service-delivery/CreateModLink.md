---
title: Add or modify an HR deep link
description: Use the Define Link \(Link Generator Sources\) to create a record for the target website name and URL.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Link generator for HR Service Delivery, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Add or modify an HR deep link

Use the **Define Link** \(Link Generator Sources\) to create a record for the target website name and URL.

## Before you begin

Role required: link\_generator\_writer

## Procedure

1.  Navigate to **All** &gt; **Link Generator** &gt; **Define Link**.

2.  Click **New** or an existing record.

    |Field|Description|
    |-----|-----------|
    |**Website name**|Enter the external website name that is the target for the link.|
    |**Website URL**|Enter the URL of the website.|

3.  Click **Submit** or **Update**.

4.  Navigate to **Define Link Parameters**.

5.  Click **New** or on an existing record.

<table id="choicetable_xb4_jnt_bbb"><thead><tr><th align="left" id="d315269e135">

Field

</th><th align="left" id="d315269e138">

Description

</th></tr></thead><tbody><tr><td id="d315269e144">

**Deep link name**

</td><td>

Enter a name or location within the website you are linking to.

</td></tr><tr><td id="d315269e153">

**Value**

</td><td>

A unique link generator service value automatically created from the Deep link name entered.

</td></tr><tr><td id="d315269e162">

**Website name**

</td><td>

Enter the name of the website you are linking to.

</td></tr><tr><td id="d315269e171">

**Link type**

</td><td>

Select:-   Button link: Creates a button that links to the website.
-   Generated link: Use to generate a URL that you can copy and paste into any table with a field type of URL. For example, on the **Manage Content** form, create a URL content type. Then, copy and paste the URL in the Content URL field. Other examples include creating links to knowledge articles and catalogs.


</td></tr><tr><td id="d315269e193">

**Script**

</td><td>

Enter a script that directs the user to the external site.

</td></tr></tbody>
</table>6.  Click **Submit** or **Update**.

7.  Navigate to **Define Button**.

8.  Click **New** or on an existing record.

<table id="choicetable_sp1_tnt_bbb"><thead><tr><th align="left" id="d315269e239">

Field

</th><th align="left" id="d315269e242">

Description

</th></tr></thead><tbody><tr><td id="d315269e248">

**Button name**

</td><td>

Enter a name for the button that links to the outside website. What you enter here appears on the button.

</td></tr><tr><td id="d315269e257">

**Button location type**

</td><td>

Select the location type for the button.-   Standard form: Use this type to place a deep link on the legacy HR case form.
-   Custom form: Use this type to work with an API.
-   Agent Workspace: Use this type to work with HR Service Delivery Agent Workspace.


</td></tr><tr><td id="d315269e286">

**Form \(Table\)**

</td><td>

Select the table that contains the field you want the deep link button to appear next to.For example, select the **HR Profile \[sn\_hr\_core\_profile\]** table when you want the deep link button to appear next to a field on the **HR Profile** form.

</td></tr><tr><td id="d315269e304">

**Location \(Field\)**

</td><td>

Select the field from the table selected that you want the deep link button to appear next to.For example, select **User** to place the deep link button next to the **User** field on the **HR Profile** form.

</td></tr><tr><td id="d315269e326">

**Deep link name**

</td><td>

This information is pulled from the **Deep Link Parameters** \(Link Generator Service\) form.

</td></tr><tr><td id="d315269e338">

**Active**

</td><td>

Check to make this mapping active and available for use.

</td></tr></tbody>
</table>9.  Click **Submit** or **Update**.


**Parent Topic:**[Link generator for HR Service Delivery](../concept/HRLinkGenerator.md)

