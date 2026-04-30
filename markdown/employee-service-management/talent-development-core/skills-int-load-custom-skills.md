---
title: Load your custom skills into Skills Foundation
description: Upload the skills specific to your organization or human capital management practices in your ServiceNow instance.
locale: en-US
release: zurich
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Load your custom skills into Skills Foundation

Upload the skills specific to your organization or human capital management practices in your ServiceNow instance.

## Before you begin

For information about the format to add and upload the custom skills in your organization, see [Custom Skills Sample Data](https://store.servicenow.com/appStoreAttachments.do?sys_id=a7fc82771ba835105c1e0d08624bcbf3).

Role required: import\_admin, sn\_skills\_int.admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load data**.

2.  In the **Import set table** field, select **Existing table**.

3.  Select the Skills Staging \[sn\_skills\_int\_skills\_staging\] table from the drop-down list.

    **Note:** If no values appear in the table for the level types and proficiencies for a skill, the skill will be created without this information. For more information, see [Define a skill level type](https://www.servicenow.com/docs/access?context=define-skill-level-type&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

4.  In the **Source of the import** field, select **File**.

5.  Select the source of the CSV file by selecting **Choose File**.

6.  Select **Submit**.

7.  Transform the data from the staging table format to the job architecture table format by selecting **Run transform**.

8.  Select **Transform**.


## Result

The custom skills are added to the existing skills in the Skills \[cmn\_skills\] table.

