---
title: Delete a UI interaction
description: Delete a UI interaction when it’s no longer needed or when you must replace it with a new version. Although UI interactions can be edited after creation, some foundational properties are intentionally locked to avoid data and runtime errors. In those cases, deletion might be required.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [UI interactions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Delete a UI interaction

Delete a UI interaction when it’s no longer needed or when you must replace it with a new version. Although UI interactions can be edited after creation, some foundational properties are intentionally locked to avoid data and runtime errors. In those cases, deletion might be required.

## Before you begin

Before deleting a UI interaction, verify whether it’s currently in use. Deleting an interaction may break event-driven behavior such as button clicks or modal launches that reference it. The Usage section on the interaction's Settings page shows all pages and declarative actions that reference the interaction.

To avoid data mismatches and runtime errors, some properties of a UI interaction can’t be changed after creation or once the interaction is in use:

-   UI interaction type
-   Input IDs and input types once the interaction is referenced by an active declarative action or page event

Role required: ui\_builder\_admin

**Important:** Deletion is permanent and can’t be undone. An interaction can be deleted only if it isn’t referenced by any declarative actions or page events.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **UI interactions** tab.

3.  In the search field, enter the name of the interaction you want to delete.

    ![UI interactions list with search field highlighted.](../image/uib-uii-search.png "UI interactions list")

4.  Select the interaction from the search results.

5.  Verify that the interaction is not in use.

    1.  Open the Settings tab.

    2.  Review the Usage section.

        If any declarative actions or page events are listed, the interaction can’t be deleted.

    3.  Remove or update those references before proceeding.

    4.  After all references are removed, return to the Settings page and confirm that the Usage section is empty before proceeding with deletion.

6.  From the Settings tab, select **Delete**.

    ![UI interactions Settings page with Delete highlighted.](../image/uib-uii-settings.png "UI interaction Settings page")


## Result

The UI interaction is permanently removed. Any component or page that previously referenced this interaction will no longer trigger its actions. Update or remove related event handlers as needed.

**Parent Topic:**[UI interactions](../concept/uib-ui-interactions.md)

