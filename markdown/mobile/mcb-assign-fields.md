---
title: Assign field values to your mobile card
description: Use Mobile Card Builder to show field labels and values from your tables in mobile cards.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customize a screen, Mobile Card Builder, Building tools, Building mobile apps, Mobile Platform]
---

# Assign field values to your mobile card

Use Mobile Card Builder to show field labels and values from your tables in mobile cards.

## Before you begin

Role required: admin or delegated developer

For more information about the delegated developer role, see [Delegated development and deployment](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=australia&pubname=australia-application-development&ft:locale=en-US).

## About this task

Data from your records is displayed on your cards using text elements. These elements can display either the label of a field or the value of a field from a record.

![Text element used to display data from an incident record](../image/mcb-field-values-1.png "Text elements used to display data from an incident record")

In this example, the top three text elements display the values of the **State**, **Number**, and **Short Description** fields. Under these elements, you can see pairs of text elements to display both the label and value of the **Opened by** and **Priority** fields. The dotted outlines around these fields are containers used to organize the text.

## Procedure

1.  Open your mobile card in Card Builder using one of the following methods.

<table id="choicetable_pm3_x3t_xnb"><tbody><tr><td id="d81198e97">

**Open Mobile Card Builder from Mobile App Builder**

</td><td>

In Mobile App Builder, open the screen where you want to modify your card, and select open in Mobile App Builder

</td></tr><tr><td id="d81198e119">

**Open Card builder from the web-based UI**

</td><td>

Navigate to **System Mobile** &gt; **Mobile Card Builder**, then select the card or card template you want to modify using the pop-up window that displays when Card Builder first opens.

</td></tr></tbody>
</table>2.  Select a text in your mobile card, or create a new one.

    For details on creating elements, see [Mobile Card Builder user interface](../reference/mcb-stage-ui.md).

    With your text element selected, you can see the configuration properties in the **Component configuration** panel on the right of the screen. If you do not see this panel, select the **Expand configuration panel** \(![Expand configuration panel icon](../image/expand-config-panel-icon.png)\) button. ![Component configuration for a text element.](../image/mcb-field-values-2.png)

3.  Under **Field type**, select either an option.

<table id="choicetable_wfv_4hz_xnb"><tbody><tr><td id="d81198e189">

**Field Value**

</td><td>

The text element displays the value of a field on your table. For example, if you select **Number**, the field displays the record number.

</td></tr><tr><td id="d81198e201">

**Field Label**

</td><td>

The text element displays the name of a field on your table. For example, if you select **Number**, the field displays the word **Number**.

</td></tr></tbody>
</table>4.  Under **Mapped field**, select the list button \(![List icon](../image/mcb-dropdown-icon.png)\) to select a field from your table.

5.  Use the **Select a field** window to select a field.

    When you have chosen your field, select **Select.**

    ![Select a field window in Mobile Card Builder](../image/mcb-select-field-window.png)

6.  Repeat steps 2 through 5 to assign any other values from your table that you want to appear on your card.

    If you want to display both the name and value of the field, use two text elements side by side, as shown in this example.

    ![Two text element used to display a field label and value on a mobile card](../image/mcb-side-by-side.png)

7.  Select **Save**.


