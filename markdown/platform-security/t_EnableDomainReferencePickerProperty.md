---
title: Enable domain selection menus in Core UI
description: Displaying the domain picker in Core UI enables the domain selector by default. After enabling the domain selector, you can add a system property to enable the domain reference picker.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use domain selection menus, Advanced domain separation administration, Domain separation setup and administration, Domain separation for service providers, Access Management]
---

# Enable domain selection menus in Core UI

Displaying the domain picker in Core UI enables the domain selector by default. After enabling the domain selector, you can add a system property to enable the domain reference picker.

## Before you begin

**Note:** The domain separation \(plugin com.snc.pa.domain\_support\) is required to enable the domain reference picker.

Role required: admin

## About this task

## Procedure

1.  Click the gear icon in the header.

2.  On the General tab, click the **Show domain picker in header** switch.

    The domain selector appears in Core UI header.

3.  Enable the domain reference picker.

    **Note:** Enabling the domain reference picker removes the global option from the list. To return to your home domain, click the return arrow next to the reference field. Admin users can click the return arrow to return to the global domain.

    1.  Enter `sys_properties.list` in the application navigator.

    2.  If not already present, add the `glide.ui.domain_reference_picker.enabled` property and set the value to **true**.

    3.  Refresh the browser.

    The domain reference picker appears in Core UI header.


**Parent Topic:**[Use domain selection menus](../concept/c_DisplayingDomainSelectionMenus.md)

**Related topics**  


[Restrict access to the domain picker](t_RestrictAccesstoDomainPicker.md)

