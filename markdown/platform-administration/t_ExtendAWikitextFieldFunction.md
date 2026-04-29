---
title: Extend the functionality of a Wikitext field
description: Configure the Wikitext field to link to other sources within the system.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Wiki field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Extend the functionality of a Wikitext field

Configure the Wikitext field to link to other sources within the system.

## Before you begin

Role required: personalize\_dictionary

## Procedure

1.  Right-click in the header of the new Wikitext field.

2.  Select **Configure Dictionary**

3.  In the **Dependent** field of the dictionary form, enter the field you want to use for linking to other pages.

    For example, on the Incident table, you might choose the **number** field.

    ![Wiki field dictionary example](../image/WikiPluginNewFieldDict.png)

    This configuration enables you to link to any incident by using that incident's number. For example, to open INC0000002, you enter `[[INC0000002]]`.

    The following [dictionary attributes](../../reference-pages/concept/c_DictionaryAttributes.md) are available for wiki\_text fields.

    -   **preview\_first=true** - sets the preview mode to display on page load, otherwise editor will be displayed
    -   **preview\_selector=true** - enables the toggle button to switch between the editor and preview
    -   **dual\_mode=true** - enables displaying both the editor and the preview simultaneously during edit mode.

