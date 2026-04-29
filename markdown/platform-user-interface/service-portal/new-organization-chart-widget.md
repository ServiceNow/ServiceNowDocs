---
title: New Organization Chart widget
description: The New Organization Chart widget shows employees in a tree structure relative to their manager. You can use this widget in your portal or duplicate it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# New Organization Chart widget

The New Organization Chart widget shows employees in a tree structure relative to their manager. You can use this widget in your portal or duplicate it to suit your own business needs.

## Using the widget

In the text input field, enter or select a user. The widget uses information from the sys\_user table based on the use sys\_id record to display the organization hierarchy relative to the selected user.

Select a card to open the profile page for that user. To reconfigure the card link, change the **Profile URL** in the widget instance options.

You can drag individual cards to rearrange the chart.

Select the magnifying glass icon to zoom in or out of the chart view.

## Instance options

You can use instance options to customize widget settings. Press the `CTRL` key, select the widget, and then select **Instance Options**.

**Note:** There are no valid values for several instance options. By default, you can set only the Profile URL instance option.

<table id="table_kxy_jds_qhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Primary Fields

</td><td>

Name and Title \(maximum of two fields\)

</td></tr><tr><td>

Secondary Fields

</td><td>

-   department:sitemap
-   location:map-marker
-   email:envelope:email
-   mobile\_phone:phone:phone

</td></tr><tr><td>

Profile URL

</td><td>

?id=user\_profile&amp;sys\_id=\{sys\_id\}

</td></tr><tr><td>

Hide Search

</td><td>

Boolean

</td></tr><tr><td>

Hide Actions

</td><td>

Boolean

</td></tr><tr><td>

max Report To Show

</td><td>

12 \(default\)

</td></tr><tr><td>

Max Manager Level

</td><td>

7 \(default\)

</td></tr><tr><td class="sub-head" colspan="2">

Presentation

</td></tr><tr><td class="sub-head" colspan="2">

Behavior

</td></tr><tr><td>

Profile URL

</td><td>

Web address of the page that opens when you select a card. Use the part of the portal URL that references the page ID. For example, to navigate to the Service Catalog, enter `?id=sc_category`.

 If you leave the URL empty, the card opens the web address in the **URL** field. If the **URL** field is also empty, the card opens the user profile page by default.

</td></tr></tbody>
</table>**Parent Topic:**[Example widgets](sp-example-widgets.md)

