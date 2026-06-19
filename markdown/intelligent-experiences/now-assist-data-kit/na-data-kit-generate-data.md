---
title: Generate synthetic data
description: Create synthetic data using the Standard data generator in Now Assist Data Kit. Use synthetic data to imitate real-world records so you can run evaluations or create training for a test model without using production data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-data-kit/na-data-kit-generate-data.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 3
breadcrumb: [Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# Generate synthetic data

Create synthetic data using the Standard data generator in Now Assist Data Kit. Use synthetic data to imitate real-world records so you can run evaluations or create training for a test model without using production data.

## Before you begin

Role required: sn\_data\_kit.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Data Kit** &gt; **Home**.

2.  On the **Synthetic datasets** tab, select **Generate dataset**.

    The **Select a generator type** dialog opens.

3.  Select **Standard data generator**.

    **Note:** A **Multi-table data generator \(beta\)** option is also available. This generator creates test data across multiple related tables simultaneously, maintaining referential integrity. As a beta feature, it may behave unexpectedly.

4.  On the **Define dataset** page, fill in the fields and select **Next**.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the synthetic dataset.|
    |Choose a template \(optional\)|A pre-built configuration for a common data type. Selecting a template pre-fills the industry, data description, and category fields. Available templates include Catalog item and Incident data.|
    |Describe department or industry|The domain area, such as healthcare or finance that the data pertains to. This specification helps generate high-quality data. Find sample descriptions in the "Get help" section.|
    |Describe the data you want to generate|Detailed description to help generate a wide range of relevant keywords, resulting in higher quality data.|
    |Add categories to generate a diverse dataset|Keywords that guide the model to generate relevant data. For example, “software issue”, “laptop”, “password reset”, “payroll”, “benefits”, etc.|
    |Select language to generate data in|The language for the generated records. Defaults to English.|

5.  On the **Select sample data** page, add sample records to help the model understand the expected structure, format, and tone of the generated data, then select **Next**.

    You can select up to 3 records from an instance table or an existing data collection. For detailed steps, see [Select the sample data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/select-sample-data.md).

    **Note:** Sample data is not replicated in the output. It is used only to guide generation.

6.  On the **Define columns** page, review and update the column definitions, then select **Next**.

    Each column requires a label, a data type, and a description of the data to generate. You can use **Generate column descriptions** to auto-populate descriptions, add new columns, or delete all columns and start fresh. For detailed steps, see [Define columns to generate data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/na-data-kit-define-columns.md).

    **Note:** If you selected sample data in the previous step, column definitions are pre-populated based on the columns you chose.

7.  On the **Test and generate data** page, configure the generation settings.

    |Field|Description|
    |-----|-----------|
    |Number of records to generate|The total number of records to generate. Defaults to 20.|
    |Additional rules \(optional\)|Extra constraints or instructions to guide the data generation.|

8.  Select **Generate preview** to review a 5-record sample before committing to full generation.

9.  Select **Review summary**.

    A summary of all dataset settings appears. Select **Edit** next to any section to make changes before generating.

10. Select **Start generation**.

    The generation job starts and a progress page opens. You can leave this page and return later. The records appear on the **Synthetic datasets** tab when generation is complete.


## What to do next

When generation completes, the dataset detail page shows three tabs:

-   **Output data**: The generated records. Review these for accuracy. A disclaimer reminds you that AI-generated content should be verified before use.
-   **Data insights**: A quality score \(0–100\) and a breakdown of metrics including data volume, similarity to sample data, data hygiene, missing or empty values, and temporal consistency. A score of 80 or higher indicates the dataset is ready to use. For more information, see [View data insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/view-data-insights.md).
-   **Input settings**: A record of the data definition, sample data, and column definitions used to generate the dataset.

Select **Save as Template** to save the generator configuration for reuse, or **Add to data asset** to make the dataset available for use in data collections.

