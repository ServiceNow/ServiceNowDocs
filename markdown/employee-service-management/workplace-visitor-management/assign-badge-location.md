---
title: Assign badge templates to a workplace location
description: Assign a badge template to a workplace location.
locale: en-US
release: australia
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a visitor badge template, Configure, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Assign badge templates to a workplace location

Assign a badge template to a workplace location.

## Before you begin

Role required: sn\_wsd\_visitor.manager, sn\_wsd\_core.workplace\_manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Visitor Management** &gt; **Administration** &gt; **Visitor badge templates**.

2.  On the Html Templates list, select the badge template that you want to use.

3.  On the Workplace Locations related list, select **Edit**.

4.  From the **Collection** column, select the workplace locations that the template must be assigned to.

5.  Move the workplace location to the **Workplace location List** column by using the add-remove icon \(![Add-remove icon.](../../wsd-reservation-management/image/add-remove-icon.png)\).

    **Note:** You can remove workplace locations from the **Workplace location list** column by using the add-remove icon \(![Add-remove icon.](../../wsd-reservation-management/image/add-remove-icon.png)\).

6.  Select **Save**.


## Result

The badge template is assigned to the selected locations. After a visitor is checked-in, you can print a badge from the visitor registration record.

You can verify the badge template that is assigned to a location in the **Badge template** field of the workplace location record. If the **Badge template** field isn’t available on the workplace location record, you can add it by configuring the form layout.

If a location doesn't have an assigned badge template, the nearest template from its location hierarchy is selected while printing a badge. If a template doesn't exist in the hierarchy, the badge template specified in the **sn\_wsd\_visitor.default\_badge\_template** system property is selected.

If the visitor picture is not found, a default avatar is used for the badge template. You can change the avatar picture in the **sn\_wsd\_visitor.visitor\_avatar.png** record of the Images \[db\_image\] table.

**Parent Topic:**[Create a visitor badge template](create-visitor-badge-template.md)

