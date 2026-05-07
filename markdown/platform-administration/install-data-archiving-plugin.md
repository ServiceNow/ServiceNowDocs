---
title: Install Live Archive
description: Install Live Archive to archive data in object storage.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-13"
reading_time_minutes: 1
breadcrumb: [Configure, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Install Live Archive

Install Live Archive to archive data in object storage.

## Before you begin

Role required: admin

|Requirement|Details|
|-----------|-------|
|Entitlement|Check your entitlements to determine whether you have access to RaptorDB Professional v2.|
|Platform release|At least the Australia release.|
|RaptorDB version|At least RaptorDB Professional version 35.1.|

## About this task

Consider the following aspects of Live Archive migration before starting the installation:

-   Archive rule processing is paused during the migration, so plan installations around any time-sensitive archiving schedules.
-   Existing archived data is converted to columnar storage format.
-   Converted data is moved to the object storage as the migration progresses.
-   Archive rule processing resumes after the migration completes.

Migration duration depends on the volume of data in the archive tables. Large archives require longer migration windows. Non-archived data and standard instance operations remain unaffected during the migration.

## Procedure

1.  Navigate to **All** &gt; **Application Manager**.

2.  Search for live archive and select **Live Archive**.

    The Live Archive plugin \[com.glide.db.columnar.archive\] is automatically downloaded with the product.

3.  Select **Install** and review the installation instructions.

4.  Select **Install Now**.

5.  Confirm the installation.

    1.  Select the **Installed** tab.

    2.  In the **Search your licensed applications and plugins** field, enter `Live Archive` and press **Enter**.

    3.  Verify whether Live Archive appears in the results.

6.  Verify that S3 facade endpoints have been created in each datacenter in the instance's datacenter pair.

    1.  Navigate to **All** &gt; **Filter** and search for `sys_service_endpoint_list.do`.

    2.  In the **Name** column, enter `s3_facade`.

    3.  Confirm that the two endpoints are listed, each with **Active** status set to **true**.

7.  Verify whether a new **Object Storage** tile is available by navigating to **System Data Management** &gt; **Data Management Console** and checking the summary section.

    It might take up to 24 hours for data to appear in the tile.


**Parent Topic:**[Configuring Data Management](../concept/configuring-data-management.md)

