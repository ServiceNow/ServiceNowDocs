---
title: Assign field values to your mobile card
description: Use Mobile Card Builder to show field labels and values from your tables in mobile cards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/mcb-assign-fields.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Customize a screen, Mobile Card Builder, Building tools, Building mobile apps, Mobile Platform]
---

# Assign field values to your mobile card

Use Mobile Card Builder to show field labels and values from your tables in mobile cards.

## Before you begin

Role required: admin or delegated developer

For more information about the delegated developer role, see [Exploring Delegated Development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md).

## About this task

Data from your records is displayed on your cards using text elements. These elements can display either the label of a field or the value of a field from a record.

\[Omitted image "mcb-field-values-1.png"\] Alt text: Text element used to display data from an incident record

In this example, the top three text elements display the values of the **State**, **Number**, and **Short Description** fields. Under these elements, you can see pairs of text elements to display both the label and value of the **Opened by** and **Priority** fields. The dotted outlines around these fields are containers used to organize the text.

## Procedure

1.  Open your mobile card in Card Builder using one of the following methods.

<table id="choicetable_pm3_x3t_xnb"><tbody><tr><td id="d34535e97">

**Open Mobile Card Builder from Mobile App Builder**

</td><td>

In Mobile App Builder, open the screen where you want to modify your card, and select open in Mobile App Builder

</td></tr><tr><td id="d34535e119">

**Open Card builder from the web-based UI**

</td><td>

Navigate to **System Mobile** &gt; **Mobile Card Builder**, then select the card or card template you want to modify using the pop-up window that displays when Card Builder first opens.

</td></tr></tbody>
</table>2.  Select a text in your mobile card, or create a new one.

    For details on creating elements, see [Mobile Card Builder user interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mcb-stage-ui.md).

    With your text element selected, you can see the configuration properties in the **Component configuration** panel on the right of the screen. If you do not see this panel, select the **Expand configuration panel** \(\[Omitted image "expand-config-panel-icon.png"\] Alt text: Expand configuration panel icon\) button. \[Omitted image "mcb-field-values-2.png"\] Alt text: Component configuration for a text element.

3.  Under **Field type**, select either an option.

<table id="choicetable_wfv_4hz_xnb"><tbody><tr><td id="d34535e189">

**Field Value**

</td><td>

The text element displays the value of a field on your table. For example, if you select **Number**, the field displays the record number.

</td></tr><tr><td id="d34535e201">

**Field Label**

</td><td>

The text element displays the name of a field on your table. For example, if you select **Number**, the field displays the word **Number**.

</td></tr></tbody>
</table>4.  Under **Mapped field**, select the list button \(\[Omitted image "mcb-dropdown-icon.png"\] Alt text: List icon\) to select a field from your table.

5.  Use the **Select a field** window to select a field.

    When you have chosen your field, select **Select.**

    \[Omitted image "mcb-select-field-window.png"\] Alt text: Select a field window in Mobile Card Builder

6.  Repeat steps 2 through 5 to assign any other values from your table that you want to appear on your card.

    If you want to display both the name and value of the field, use two text elements side by side, as shown in this example.

    \[Omitted image "mcb-side-by-side.png"\] Alt text: Two text element used to display a field label and value on a mobile card

7.  Select **Save**.


