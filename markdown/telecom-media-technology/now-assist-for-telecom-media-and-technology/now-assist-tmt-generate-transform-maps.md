---
title: Automate transforms with Now Assist for TMT
description: Use the Now Assist for TMT Transform Mapping Assist feature to automatically transform inbound and outbound data between provider and consumer tables.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Automate transforms with Now Assist for TMT

Use the Now Assist for TMT Transform Mapping Assist feature to automatically transform inbound and outbound data between provider and consumer tables.

## Before you begin

Role required: admin

## About this task

The Transform Mapping Assist skill is designed to do the following:

-   Automatically generate choice mappings between provider and consumer tables.
-   Provide meaningful error messages if the inbound or outbound data cannot be transformed.
-   Help save time and reduce manual effort by automating the transformation mapping process.
-   Help reduce errors and enhance the quality of integrations through automatic mapping.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Transforms**.

2.  Click **New** and create a simple transform.

    See [Create a transform in Service Exchange](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-transform&version=australia&pubname=australia-service-bridge&ft:locale=en-US) for instructions. The Now Assist for TMT Transform Assist Mapping can be used only with simple transforms.

3.  Select the provider and consumer tables and the related fields.

4.  Click **Mapping Assist**.

    Transform mappings are generated and inserted into the Transform lines related list.

    **Note:**

    -   The Transform Mapping Assist feature can be used only if you select choice list fields in the Provider and Consumer fields.
    -   You can delete all the generated transform lines to rerun the mapping if needed.
    -   If you try to create a transformation mapping between different types of fields, you will see the following warning message:

        `The selected fields are different. Are you sure you want to map these fields? This action may lead to unintended results.`

        Click **OK** to continue with the mapping. If no mappings are found, an error message is displayed. You can either review the configuration settings and modify as required or create the mappings manually.


**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

