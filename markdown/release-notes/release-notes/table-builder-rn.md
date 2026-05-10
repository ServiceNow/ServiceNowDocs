---
title: Table Builder release notes
description: The ServiceNow Table Builder application is a centralized way to build tables, forms, and display logic. Table Builder was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Table Builder release notes

The ServiceNow® Table Builder application is a centralized way to build tables, forms, and display logic. Table Builder was enhanced and updated in the Australia release.

## Table Builder highlights for the Australia release

-   Read-only behavior is now controlled by the **Read only option** \[`read_only_option`\] choice field, which provides options such as **Display Read Only** or **Strict Read Only**.
-   The existing **Read only** field will no longer be editable in the UI.

See [Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/tb-landing-page.md) for more information.

**Important:** Table Builder is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## UI changes

-   **[Field configuration in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/field-parameters.md)**

    A new **Read Only Option** has been added to the dictionary tables \(`sys_dictionary` and `sys_dictionary_override`\). The existing **read\_only** field is now locked and cannot be edited in the UI. Field behavior depends on the selected option. With **Display Read Only**, the field appears read-only but can still be updated through APIs. With **Strict Read Only**, the field cannot be changed in the UI or by client scripts such as \[`g_form.setValue()`\]. A new system property,`glide.read_only.legacy_read_only_behavior`, controls whether the old behavior, where client scripts could override read-only settings, is retained.


## Browser requirements

Internet Explorer isn’t supported.

## Related ServiceNow applications and features

-   **[App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/aes-overview.md)**

    App Engine Studio \(AES\) is a guided, low-code tool for developing rich web applications to store information, automate business processes, and solve business problems.


**Parent Topic:**[Workflow Studio release notes](workflow-studio-rn-landing.md)

