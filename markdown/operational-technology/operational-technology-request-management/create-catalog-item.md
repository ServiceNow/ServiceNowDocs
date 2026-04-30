---
title: Create a catalog item for your Operational Technology Service Catalog
description: Create a catalog item for the Operational Technology \(OT\) Service Catalog using the catalog builder so that other users can submit OT requests categorized by catalog item.
locale: en-US
release: xanadu
product: Operational Technology Request Management
classification: operational-technology-request-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [OT service catalog]
breadcrumb: [Configure, Operational Technology Request Management, Operational Technology]
---

# Create a catalog item for your Operational Technology Service Catalog

Create a catalog item for the Operational Technology \(OT\) Service Catalog using the catalog builder so that other users can submit OT requests categorized by catalog item.

## Before you begin

Role required: admin

## About this task

You can create catalog items for the OT Service Catalog in the catalog builder. When other users submit an OT request, they can choose the catalog item that best fits their needs. For example, requesting remote access to an OT device can be a catalog item available in the OT Service Catalog. This allows third parties to work on issues related to OT devices.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  In the **Dashboard** tab under **Start creating your new catalog item**, select **Create a new catalog item**.![Create a new catalog item button in the catalog builder on your instance.](../image/create-catalog-item-buttom-otrm.png)

    Alternatively, select the **Catalog Items** tab and click **New**.

3.  On the **Getting Started** page, select **Continue**.

4.  On the **Select your item template** page, select the **OT Catalog Item Template**.

5.  Select **Use this item template**.

6.  On the **Create catalog item** form, fill in the fields.

    For more information about the Catalog Item form fields, see [Operational Technology Catalog Item form](../reference/catalog-item-form-ot-request.md).

    **Note:** You can’t remove the OT Catalog Item Variable Set from the Questions section. The OT Catalog Item Variable Set is what distinguishes OT requests from other requests. You can instead create new questions for your item form by selecting **Insert New Question**. For more information about inserting a new question, see [Create a question for a catalog item in Catalog Builder](https://www.servicenow.com/docs/access?context=create-question-cat-builder&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

7.  To preview your catalog item, select **Preview**.

8.  To save your progress, select **Save**.

9.  Once you get to the **Review and Submit** section, review the catalog item information you added and select **Submit**.

10. Repeat steps 1 to 9 for each catalog item that you want to create.


## Result

The catalog item is created and available for other users to select when they create an OT request in the OT Service Catalog.

**Parent Topic:**[Configuring Operational Technology Request Management](../concept/configuring-operational-technology-request-management.md)

