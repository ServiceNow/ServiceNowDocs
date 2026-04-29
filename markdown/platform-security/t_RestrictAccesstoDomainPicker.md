---
title: Restrict access to the domain picker
description: Use a system property to restrict access to the domain picker in Core UI and Next Experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use domain selection menus, Advanced administration, Setup and administration, Domain separation for service providers, Access Management]
---

# Restrict access to the domain picker

Use a system property to restrict access to the domain picker in Core UI and Next Experience.

## Before you begin

Role required: admin

## About this task

By default, users with the ITIL role, and roles that include the ITIL role \(such as the administrator\), can access the domain picker in Next Experience. You can grant other roles access by adding them to the property or restrict roles by removing them. It is recommended to restrict the role to admins only.

Admins can grant access to users by creating a system property in the sys\_properties table.![Polaris domain picker UI](../image/domain-sep-global-polaris.png)

## Procedure

1.  Open the System Properties \[sys\_properties\] table.

2.  Add this property: `glide.ui.polaris.domain_picker.role`

3.  Configure the property value as a comma-separated list of roles: **admin, itil**.

    To learn more, see [Configure Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)


**Parent Topic:**[Use domain selection menus](../concept/c_DisplayingDomainSelectionMenus.md)

**Related topics**  


[Enable domain selection menus in Core UI](t_EnableDomainReferencePickerProperty.md)

