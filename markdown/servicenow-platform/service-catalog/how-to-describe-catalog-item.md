---
title: Suggestions to describe catalog items
description: Now Assist uses the description that you write to generate a catalog item for you. If you're using Now Assist for creating a catalog item, use these suggestions to describe your catalog item.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [generative AI, Now Assist in Catalog Builder]
breadcrumb: [Catalog item generation reference, Now Assist in Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Suggestions to describe catalog items

Now Assist uses the description that you write to generate a catalog item for you. If you're using Now Assist for creating a catalog item, use these suggestions to describe your catalog item.

-   Provide the necessary details of the catalog item that you want to build.
-   If you want, you can add details of one or more questions that you want to include in the catalog item. For accurate results, describe all aspects of the question, including type, properties such as mandatory, choices, and default value.
-   Specify the exact table name for reference questions.
-   For a record producer, provide the exact field name to which you want to map the question.

## Defining dynamic behavior

You can add dynamic behavior by specifying actions and conditions in the Now Assist prompt. While generating the item, Now Assist creates dynamic behavior for the catalog item based on the text input.

Let's see an example. Specify the text in the prompt as "`Create a catalog item for a standard mobile; color (Black, Space Grey, Silver); storage (512 GB and 256 GB) If color is Black or Silver, then set the storage to 256 GB and make it read only.`" Generate the item. For the storage question, Now Assist creates a dynamic behavior that sets the field to 256 GB and makes it not editable if Black or Silver is specified as the color.

## Configuring auto-populate

Using Now Assist, you can configure the value of a question to populate automatically whenever the value of another question of the reference type changes. For more information about auto-populate, see [Configure an auto-populate value for a question in Catalog Builder](../task/config-auto-populate-value-for-question-cat-builder.md#).

`Create a catalog item requesting for replacement of access card with the following questions: - Who is it for?: (The question type should be "Requested for") - Manager: (Reference type on the sys_user table. This field should auto-populate based on the value of the Requested for question.) - Upload your profile picture: (Attachment, mandatory)`

After generating the catalog item, you can verify the **Auto-populate** tab. It's configured based on your text input.

**Parent Topic:**[Catalog item generation reference](catalog-item-generation-reference.md)

**Related topics**  


[Creating a catalog item conversationally using Now Assist](../task/create-catalog-item-using-now-assist.md)

