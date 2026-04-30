---
title: How to describe a catalog item
description: Now Assist uses the description that you write to generate a catalog item for you. If you're using Now Assist for creating a catalog item, use these points to describe your catalog item.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Catalog item generation reference, Now Assist in Catalog Builder, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# How to describe a catalog item

Now Assist uses the description that you write to generate a catalog item for you. If you're using Now Assist for creating a catalog item, use these points to describe your catalog item.

-   Provide the necessary details of the catalog item that you want to build. For example, you can start with entering the following text:

    `Create a travel visa request form.`

-   If you want, you can add details of one or more questions that you want to include in the catalog item. For accurate results, describe all aspects of the question, including type, properties such as mandatory, choices, and default value.
-   Specify the exact table name for reference questions.
-   For a record producer, provide the exact field name to which you want to map the question.

    For example, you can write the following text:

    `Create a travel visa request form`

    `It must include a drop down menu offering three travel types: Internal, External, and Customer visit (with Customer visit as the default option). Add mandatory fields for the travel start date, country of birth, and country traveling to (these must be reference fields from the core_country table). Include an optional field for trip duration and a section prompting the user to provide a business justification.`


**Note:** If your description contains offensive or inappropriate content, Now Assist recognizes such content, and might not generate the catalog item for you.

**Parent Topic:**[Catalog item generation reference](catalog-item-generation-reference.md)

