---
title: Mobile UI Rules
description: Use Mobile UI rules to build rules that modify the mobile UI. These modifications can include hiding and displaying fields, making fields mandatory, performing field value calculations, and applying UI styles to different UI elements.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Mobile styles, Mobile app components, Building mobile apps, Mobile Platform]
---

# Mobile UI Rules

Use Mobile UI rules to build rules that modify the mobile UI. These modifications can include hiding and displaying fields, making fields mandatory, performing field value calculations, and applying UI styles to different UI elements.

## Mobile UI rules and actions

To modify the appearance of your mobile views and input form screens UI, you must create a mobile UI rule, and at least one associated mobile UI action.

-   **Mobile UI rules**

    A mobile UI rule applies to a single mobile view and input form screen. When you create a rule, you select a record to apply the rule to, as well as conditions that define when your rule applies.

-   **Mobile UI rule actions**

    Each mobile UI rule uses mobile UI rule actions. These actions define the changes made to your target record. When you create an action, you select an operation, which defines the kind of change you want to make. You then define a value, which gives the rule more detail on the specifics of the change you're making.


For more detail on the kinds of changes you can make with mobile UI rules, see the next section. For detailed steps on creating mobile UI rules and actions, see [Create a mobile UI rule](../task/create-mobile-ui-rule.md).

## Available mobile UI rule operations

-   **Allow calculations on input form screen inputs**

<table id="table_qc2_xls_lnb"><tbody><tr><td>

Use calculations to quickly and accurately fill in field values based on calculations you define. These calculations can include values from other fields. These rules can save time and reduce complexity on your mobile screens.**Note:** Calculations can only be applied to input form screens.

</td><td>

![Demonstration of a UI rule performing a calculation.](../image/mobile-ui-rule-calc.png)

</td></tr></tbody>
</table>-   **Apply UI styling to mobile view elements**

<table id="table_csy_5ls_lnb"><tbody><tr><td>

Use mobile UI rules to apply UI styling to your screens. Using JSON code, you can set a background color, font color, and text decorator icons.**Note:** UI styling is only applicable for mobile views.

</td><td>

![Example UI styles.](../image/ui-styles.png)

</td></tr></tbody>
</table>-   **Disable buttons**

<table id="table_jfq_jdy_lnb"><tbody><tr><td>

Use mobile UI rules to conditionally disable buttons. De-clutter your interface and avoid mistakes by ensuring buttons are only available in situations where your users need them.**Note:** The disable buttons option is only applicable for mobile views.

</td><td>

![Disabled buttons in the mobile interface.](../image/disable_buttons-mobile.png)

</td></tr></tbody>
</table>-   **Hide or display inputs or mobile view elements**

<table id="table_gbj_xls_lnb"><tbody><tr><td>

Use mobile UI rules to control the visibility of your inputs or elements on your mobile views. Present a clean UI and avoid confusion by displaying inputs only when they are relevant to your users.

</td><td>

![Fields made mandatory using screen UI policies.](../image/hide-disable-input.png)

</td></tr></tbody>
</table>-   **Make inputs read-only or mandatory**

<table id="table_i4g_xls_lnb"><tbody><tr><td>

Make your inputs read-only or mandatory to control which inputs are required and which are uneditable. With these rules, you can ensure that required information is added and prevent unintentional editing of fields that do not require updates.**Note:** The option to make inputs read only or mandatory can only be applied to input form screens.

</td><td>

![Demonstration of a UI rule performing a calculation](../image/mobile-read-only.png)

</td></tr></tbody>
</table>
