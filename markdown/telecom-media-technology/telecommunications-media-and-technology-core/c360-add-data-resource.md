---
title: Add the Setup Customer360 Context data resource
description: Add the Setup Customer360 Context data resource to the record page to enable the Telecom Customer 360 component to display the correct consumer or account view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/c360-add-data-resource.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 1
keywords: [Setup Customer360 Context, data resource, Telecom Customer 360]
breadcrumb: [Telecommunications Customer 360 component, Configure, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Add the Setup Customer360 Context data resource

Add the Setup Customer360 Context data resource to the record page to enable the Telecom Customer 360 component to display the correct consumer or account view.

## Before you begin

Role required: sn\_telecom\_c360.admin

## About this task

The Setup Customer360 Context data resource resolves the record on the page to the associated account or consumer and provides the table name and sys ID to the [Telecom Customer 360 component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-add-component.md). The data resource reads the account and consumer fields on the record and returns the populated reference.

-   If only the account field is populated, the data resource returns the account table and the account sys ID. The component displays the 360 view for that account.
-   If only the consumer field is populated, the data resource returns the consumer table and the consumer sys ID. The component displays the 360 view for that consumer.

## Procedure

1.  In the **Data and scripts** section, select **Add data resource**.

2.  Select the **Setup Customer360 Context** data resource.

3.  Configure the data resource with the following inputs:

    -   Table: The table of the record page where the component is placed. Select the page parameter that contains the table name.
    -   Sys ID: The sys ID of the record on the page. Select the page parameter that contains the record sys ID.
4.  Save the page.


## What to do next

Configure the Telecom Customer 360 component properties. For more information, see [Configure the Telecommunications Customer 360 variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-configure-variables.md).

**Parent Topic:**[Telecommunications Customer 360 component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-component.md)

