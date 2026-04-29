---
title: Enable text resize in your portal
description: Enable text resize to increase the size of your text up to 200% through your browser settings.Set the HTML base CSS font size in your portal.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Defining portal styles, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable text resize in your portal

Enable text resize to increase the size of your text up to 200% through your browser settings.

## Before you begin

-   If you upgraded to a Rome instance from a prior release, the property is created for you. The property default is set to **False** for Service Portal and Mobile Employee Service Portal \(MESP\). Follow the steps in this task to manually set the property to **True**.
-   If you have a new portal or a zBoot instance, the property is set to True by default. There are no actions you need to take.
-   If you haven't upgraded to a Rome instance, the property is created, but is set to **False** by default.

Role required: admin

## Procedure

1.  Enter `sys_properties.list` in the Filter navigator.

2.  Select **glide.service\_portal.resize\_text.\{your portal\_url\_suffix\}.enable\_rem\_conversion​** from the list.

    For example, **glide.service\_portal.resize\_text.sp.enable\_rem\_conversion**.

3.  On the form, set the Value field to **true**.

4.  Select **Update**.


**Parent Topic:**[Defining portal styles](../concept/portal-css.md)

## Override the HTML base CSS font size in your portal

Set the HTML base CSS font size in your portal.

### Before you begin

Role required: admin

### Procedure

1.  Enter `sys_properties.list` in the Filter navigator.

2.  Select **glide.service\_portal.resize\_text.\{portal\_url\_suffix\}.base\_font**.

    For example, **glide.service\_portal.resize\_text.mesp.base\_font**.

3.  On the form, set the Value field to the font size you want.

4.  Select **Update**.

    **Note:** If an issue arises with resize text for custom pages coming from styling from custom CSS includes, convert those CSS values from pixels to REMs.​


