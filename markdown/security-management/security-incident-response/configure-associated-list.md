---
title: Configure each associated list from the view to handle run time data rendering
description: Configure each associated list from the view to handle run time data rendering.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure SI design time investigation, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure each associated list from the view to handle run time data rendering

Configure each associated list from the view to handle run time data rendering.

## Before you begin

**Note:** This step is mandatory for each associated list configured in the associated info view. Otherwise, the associated list will not be available on the investigation page.

Each of the associated list added \(while mapping an associated info view to an entry point list\) [Mapping View of the Associate Info to the entry point list](map-view-to-the-entry-point-list.md) \(or from the view directly\) need an additional configuration to filter the data with respect to the runtime record selection and filters selection.

Role required: admin

## Procedure

1.  Click **New** from the **Associated List Configs**.

    ![Associated related lists configs](../image/associated-related-lists-config.png)

2.  Select **Associated List** field value.

3.  Use the **Dynamic Filter** column to filter the associated list further based on the selected entry point list records and result type \(latest results from each vendor implementation, all results\).

    Refer to the existing examples that are shipped within the product.

    ![Associated related list - Dynamic filters](../image/associated-related-list.png)

4.  Also, you can configure the associated list layout using **Edit Associated List Layout** action.

    In the slush bucket window, add or remove columns as required.


**Parent Topic:**[Configure SI design time investigation](../concept/configure-investigation-canvas-records.md)

