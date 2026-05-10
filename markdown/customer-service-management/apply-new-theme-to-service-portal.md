---
title: Match the theme of the decision tree component with the Service Portal page
description: Customize the theme of the decision tree component to match the Service Portal theme.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add Guided Decisions to Service Portal, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Match the theme of the decision tree component with the Service Portal page

Customize the theme of the decision tree component to match the Service Portal theme.

## Before you begin

A variant UX theme to match the theme of the decision tree component with the Service Portal theme must exist. For more information, see [Manage the visual style of UI Builder experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/manage-the-visual-style-of-ui-builder-experiences.md).

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the **Search** field, enter `ux_portal_theme_to_uib_theme_mapping` and select the record.

3.  Copy the value of the **Name** field from the ux\_portal\_theme\_to\_uib\_theme\_mapping record.

    The **Name** field contains the system property name appended with the existing portal theme ID, for example, `ux_portal_theme_to_uib_theme_mapping.f548bd34845a1110f87767389929c667`.

4.  Select **New** to create a system property.

5.  In the **Suffix** field, paste the copied value.

6.  Provide the UX theme ID of the theme that you want to apply in the **Value** field.

    1.  On the UX theme record, select the Additional actions icon \(![Additional actions icon](../../../use/collaboration/image/IconMenu.png)\).

    2.  Select **Copy sys\_id** from the menu.

7.  Select **Update**.


## Result

The Service Portal theme is applied to the decision tree component.

