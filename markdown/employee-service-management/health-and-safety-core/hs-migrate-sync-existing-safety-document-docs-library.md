---
title: Migrate existing safety documents to the Document library
description: Migrate your existing safety documents from the deprecated Standards and Documents list to the new Health and Safety document library list.
locale: en-US
release: yokohama
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2025-11-25"
reading_time_minutes: 3
breadcrumb: [Configure settings, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Migrate existing safety documents to the Document library

Migrate your existing safety documents from the deprecated **Standards and Documents** list to the new **Health and Safety document library** list.

## Before you begin

Role required: sn\_ohs\_im.admin

## About this task

To securely maintain version control of safety documents across multiple languages and locations, Health and Safety applications now use the ServiceNow® Document Management \(com.snc.platform\_document\_management\) plugin. The previous **Standards and Documents** list and its associated table \[sn\_ohs\_im\_document\] have been deprecated.

Use the Document Migration tool to seamlessly move your existing safety documents from the deprecated table to the new **Health and Safety document library** list. This new list is based on the Health and Safety document \[sn\_ohs\_im\_document\_v2\] table. The tool supports batch migration of up to 200 records at a time. After migration, all documents can be efficiently managed within the new list.![Health and Safety Document migration tool showing migration records, their migration status, and count of migrated, pending, and failed records.](../image/hs-document-migration-tool.png)

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Standards and documentation \(Deprecated\)** &gt; **Document migration**.

2.  Select **Health and Safety document \(Deprecated\)** \(sn\_ohs\_im\_document\) and then select **Migrate records**.

    A batch of up to 200 documents are migrated and listed in the **Migration records** list.

3.  Repeat step 2 until you have migrated all existing document records.


## Result

-   All migration records with their migration status and logs are listed in the **Migration records** list.
-   The count of documents that have successfully migrated, documents pending migration, and failed migration are listed in the **Migrated records**, **Remaining records**, and **Fail records** widgets.
-   The successfully migrated records appear in the new **Health and Safety document library** list under **Configuration**, and are saved in the Health and Safety document \[sn\_ohs\_im\_document\_v2\] table.

    For information on storing safety-related documents, see [Add a new Health and Safety related document](../../ohs-incident-management/task/add-hs-related-document.md).


**Parent Topic:**[Setting up Health and Safety Core](../concept/setting-up-hs-core.md)

**Related topics**  


[Install Health and Safety Core](install-hs-core.md)

[Set up your workplace location data](../../ohs-incident-management/task/configure-hs-workplace-location-data.md)

[Enable a Health and Safety table for configuring report field mapping](../../ohs-incident-management/task/enable-hs-table-report-field-mapping.md)

[Create a safety report field mapping for generating reports](../../ohs-incident-management/task/create-safety-report-field-mapping.md)

[Configure groups for Health and Safety](../../ohs-incident-management/task/configure-groups-health-and-safety.md)

[Configure scheduled job to generate frequency rates](../../ohs-incident-management/task/configure-job-generate-frequency-rates.md)

[Assign Health and Safety profile to a user](../../ohs-incident-management/task/assign-hs-profile-user.md)

[Add a Health and Safety visitor](../../ohs-incident-management/task/hs-add-health-safety-visitor.md)

