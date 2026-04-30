---
title: Export a document extraction use case
description: Export a document extraction use case for use in another ServiceNow instance by adding it to an update set.
locale: en-US
release: yokohama
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage document extraction use cases, Configuring Document Intelligence, Document Intelligence, Enable AI experiences]
---

# Export a document extraction use case

Export a document extraction use case for use in another ServiceNow instance by adding it to an update set.

## Before you begin

-   Ensure both instances have the same family release and the same version of Document Intelligence installed when exporting and importing use cases.
-   Role required: sn\_docintel.manager

## About this task

Follow these steps to add a document extraction use case to an update set along with its fields, field groups, integrations, flows, and all related machine learning \(ML\) models. The update set can then be exported for use in another instance.

The update set\(s\) are automatically created and set to "Completed" as a background process. This process takes several minutes. The resulting update set\(s\) should not be manually set to "Completed" or exported before the background job finishes.

For more information, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction Administration** &gt; **Use Cases**.

2.  In the list, select the display name of the use case you want to export.

3.  On the use case screen, select the options icon \(![Options icon](../image/icon-docintel-field-options-menu.png)\) and select **Add to update set**.

4.  Select **Add to update set**.

    The use case is added to a system update set.

5.  Navigate to **System Update Sets** &gt; **Local Update Sets**.

6.  Select the update set you added.

7.  On the update set form, select **Export to XML** under Related Links.


**Parent Topic:**[Manage document extraction use cases](../concept/manage-use-cases.md)

**Related topics**  


[Duplicate a document extraction use case](duplicate-a-use-case.md)

[Import a document extraction use case](import-a-use-case.md)

[Delete a document extraction use case](delete-a-use-case.md)

