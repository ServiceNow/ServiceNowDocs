---
title: Load job architecture data into your ServiceNow instance
description: Load your existing company job architecture data to build a customized career architecture in your ServiceNow instance.
locale: en-US
release: yokohama
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [About Job Architecture, Configuring Skills Foundation, Skills Foundation, Talent Development, Employee Service Management]
---

# Load job architecture data into your ServiceNow instance

Load your existing company job architecture data to build a customized career architecture in your ServiceNow instance.

## Before you begin

Role required: import\_admin, sn\_skills\_int.job\_arch\_admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load data**.

2.  In the **Import set table** field, select **Existing table**.

3.  Select the Company Job Architecture Staging \[sn\_skills\_int\_company\_job\_arch\_staging\] table from the drop-down.

4.  In the **Source of the import** field, select **File**.

5.  Select **Choose File** and select the source CSV file.

6.  Select **Submit**.

    The data is imported into the job architecture staging table.

7.  Validate the imported data.

    1.  Select the Loaded data related list.

        The newly imported data in the staging table is displayed.

    2.  Select the **Validate latest import set** related link.

        A report is generated with a bar graph showing the insights about missing data in the staging table. The possible errors are:

        -   Empty job code and job title
        -   Empty job family and role group
        -   Skill missing
        -   Skill inactive
        -   Skill level type missing
        -   Proficiency mismatch
    3.  Select the bars on the graph to go the staging table and act on any missing data.

8.  Select **Run transform** to transform the data from the staging table to the Job architecture tables.

    The selected import set is displayed.

9.  Select **Transform**.

    After transformation, the message `Transformation completed` is displayed. The extracted and transformed data is loaded into the respective tables: Job family, Job profile, Role group, and Role level.


