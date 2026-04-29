---
title: Create a CSS include to override theming for AI Search in Service Portal
description: Override theming for AI Search in Service Portal to match your company branding.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [AI Search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create a CSS include to override theming for AI Search in Service Portal

Override theming for AI Search in Service Portal to match your company branding.

## Before you begin

Role required: sp\_admin or admin

## About this task

As an example of styling features of AI Search in Service Portal, this procedure removes the borders around the search filters. You can style several other features using additional CSS variables. For more information about these variables, see [Theming for AI Search in Service Portal](../reference/ais-sp-css-vars.md).

**Search filters**: Remove the line borders around search filters.

![Search filters panel showing line borders.](../image/sp-ais-filters-default.png)

## Procedure

1.  Create a style sheet record.

    1.  Enter `sp_css.do` in the Filter navigator.

    2.  On the form, fill in the fields.

<table id="table_qxq_4mh_wqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for your style sheet. For example, sp\_ais.css.

</td></tr><tr><td>

CSS

</td><td>

Field for your CSS code. Enter this code and then customize the variables. To remove the border for the search filters panel, paste this code and customize as desired.

```
sn-search-facets {
  --now-color--divider-tertiary: 0px !important;
}
```

</td></tr><tr><td>

Application

</td><td>

Application this style sheet applies to. Global means the style sheet applies to all applications.

</td></tr></tbody>
</table>    3.  Select **Submit**.

2.  Create a CSS include record.

    1.  Enter `sp_css_include.do` in the filter navigator.

    2.  On the form, fill in the fields.

<table id="table_f1c_zmh_wqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for your CSS include record.

</td></tr><tr><td>

Source

</td><td>

Source for your CSS include. Select **Style Sheet**.

</td></tr><tr><td>

Style sheet

</td><td>

The style sheet you want to incorporate with this CSS include form. Select the style sheet you created in step [1](css-override-ais-theming-sp.md#create-style-sheet-record-step).

</td></tr><tr><td>

Application

</td><td>

Application this CSS include record applies to. Global means the CSS include applies to all applications.

</td></tr><tr><td>

Lazy Load

</td><td>

Option to load the CSS Include asynchronously to improve page load time. This option should be set to the same value for all CSS Includes of a theme. Enabling asynchronous loading for only some CSS Includes associated with a theme isn’t recommended.

 **Note:** Enabling **Lazy Load** isn’t recommended for portals with flashing of unstyled content.

 The CSS Includes with **Lazy Load** enabled are listed in the **Lazy load CSS includes** related list in the theme record.

</td></tr></tbody>
</table>3.  Input your CSS override into the style sheets form and override the theme that's applied to your UI.

    1.  Enter `m2m_sp_theme_css_include` in the filter navigator.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Order|An integer that prioritizes the incorporation of this style sheet against other style sheets. The lower the number, the higher in the list. The typical practice is to make these numbers hundreds, for example, 100, 200, 300, and 400, so you can put new icons between existing ones in the future.|
        |CSS Include|CSS include that includes the overrides you created in previous steps.|
        |Application|Application this style sheet applies to. Global means the style sheet applies to all applications.|
        |Theme|Theme that's applied to your UI that you want to override.|

    3.  Select **Submit**.


## Result

The borders around the search filters are removed.![Search filters panel with line borders removed.](../image/sp-ais-filters-overridden.png)

-   **[Theming for AI Search in Service Portal](../reference/ais-sp-css-vars.md)**  
You can customize the look and feel of the AI Search experience in Service Portal by updating the relevant CSS variables.

**Parent Topic:**[AI Search in Service Portal](../concept/ai-search.md)

