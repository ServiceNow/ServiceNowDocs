---
title: Mapping View of the Associate Info to the entry point list
description: Map the associated info view to the newly added entry point list using the Map Associated Info View action.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure SI design time investigation, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Mapping View of the Associate Info to the entry point list

Map the associated info view to the newly added entry point list using the Map Associated Info View action.

## Before you begin

**Note:** This step is required for the entry point list to be visible on the Investigation page. Even if you don’t want any associated info lists to be shown under an entry point, you still need to create a dummy view and map it.

Role required: admin

## Procedure

1.  Click **Map Associated Info View** button on the **Entry Point Configs** page.

    ![Map associated info view](../image/map-associated-info-view.png)

2.  Select the newly added entry point list from the **Entry Point List** drop down list.

3.  Enter the view name containing the associated info related lists in the **Associated Info View** field.

    For information on how to create a view for the associated info related lists, see [Creating View for associated info tables](creating-view-for-associated-info-tables.md).

    ![Entry point selection for the associated info view](../image/entry-point-list-selection.png)

4.  **Save** the form.

5.  Additionally, if required you can add or remove more associated lists using the **Edit Associated Info View**.

    You can also configure the entry point list layout using **Edit Entry Point List Layout** action. Add or remove columns from the slush bucket as desired, and save the form.


**Parent Topic:**[Configure SI design time investigation](../concept/configure-investigation-canvas-records.md)

