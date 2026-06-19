---
title: Configure each associated list from the view to handle run time data rendering
description: Configure each associated list from the view to handle run time data rendering.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/configure-associated-list.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure SI design time investigation, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure each associated list from the view to handle run time data rendering

Configure each associated list from the view to handle run time data rendering.

## Before you begin

**Note:** This step is mandatory for each associated list configured in the associated info view. Otherwise, the associated list will not be available on the investigation page.

Each of the associated list added \(while mapping an associated info view to an entry point list\) [Mapping View of the Associate Info to the entry point list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/map-view-to-the-entry-point-list.md) \(or from the view directly\) need an additional configuration to filter the data with respect to the runtime record selection and filters selection.

Role required: admin

## Procedure

1.  Click **New** from the **Associated List Configs**.

    \[Omitted image "associated-related-lists-config.png"\] Alt text: Associated related lists configs

2.  Select **Associated List** field value.

3.  Use the **Dynamic Filter** column to filter the associated list further based on the selected entry point list records and result type \(latest results from each vendor implementation, all results\).

    Refer to the existing examples that are shipped within the product.

    \[Omitted image "associated-related-list.png"\] Alt text: Associated related list - Dynamic filters

4.  Also, you can configure the associated list layout using **Edit Associated List Layout** action.

    In the slush bucket window, add or remove columns as required.


**Parent Topic:**[Configure SI design time investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/configure-investigation-canvas-records.md)

