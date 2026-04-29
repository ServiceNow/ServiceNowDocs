---
title: Import a document extraction use case
description: Import a document extraction use case for use in your ServiceNow instance.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage document extraction use cases, Configure, Document Intelligence, Enable AI experiences]
---

# Import a document extraction use case

Import a document extraction use case for use in your ServiceNow instance.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

## Before you begin

-   Update sets for a document extraction use case are downloaded according to the steps provided in [Export a document extraction use case](export-a-use-case.md).
-   Ensure both instances have the same family release and the same version of Document Intelligence installed when exporting and importing use cases.
-   Role required: sn\_docintel.manager

## About this task

Follow these steps to import a document extraction use case along with its fields, field groups, integrations, flows, and all related machine learning \(ML\) models.

For more information, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

2.  Under Related Links, select **Import Update Set from XML**.

3.  Select the exported XML file and upload it.

4.  Open the update set record.

5.  Select **Preview Update Set**.

    There may be a few errors for sys\_di\_extracted\_values, stating `Could not find a record in sys_di_image for column image referenced in this update`.

    This error is because those extracted values are empty and don't have a di\_image.

6.  Select **Accept remote update**.

7.  If there are no other errors, select **Commit Update Set**.

8.  Repeat steps 3 through 7 for each update set.


## Result

The use case is imported into the instance and appears in the use cases list.

**Parent Topic:**[Manage document extraction use cases](../concept/manage-use-cases.md)

**Related topics**  


[Duplicate a document extraction use case](duplicate-a-use-case.md)

[Export a document extraction use case](export-a-use-case.md)

[Delete a document extraction use case](delete-a-use-case.md)

