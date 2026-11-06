---
title: Generate synthetic data
description: Generate synthetic records for evaluating AI skills and agents when you don't have suitable data or can't use it for privacy reasons.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/na-data-kit-generate-data.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 5
keywords: [synthetic data, data generator, AI Data Kit]
breadcrumb: [Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Generate synthetic data

Generate synthetic records for evaluating AI skills and agents when you don't have suitable data or can't use it for privacy reasons.

## Before you begin

The Generative AI Controller plugin \(sn\_generative\_ai\) must be installed. Synthetic data generation uses a large language model \(LLM\) through this plugin.

Role required: sn\_data\_kit.admin

## About this task

A guided setup walks you through five stages: Define dataset, Select sample data, Define columns, Test data generation, and Review and generate. Selecting sample data is optional. Each stage includes a Help panel with guidance for its fields.

Generation runs as a data generation job. When the job finishes, you add the generated records to a dataset so that you can curate them, add ground truth, and use them in AI Skill Kit.

Only users with the sn\_data\_kit.admin role can view data generation jobs. Datasets that you create from generated data don't have table access controls, so anyone with an AI Data Kit role can view their records.

## Procedure

1.  Navigate to **All** &gt; **AI Data Kit** &gt; **Home**.

2.  In the An overview of your data assets section, on the **Synthetic datasets** tab, select **Generate Dataset**.

3.  In the Select a generator type dialog box, select **Standard data generator**.

    The standard data generator creates flat records from the fields that you define. The **Multi-table data generator \(beta\)** option creates data for several related tables, and this topic doesn't cover it.

4.  In the Define dataset stage, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the synthetic dataset. Required.|
    |Choose a template|Template that fills in the dataset and column definitions for a type of data, such as catalog items or incidents. Templates that you save also appear in this list. You can change the values after the template fills them in. Optional.|
    |Describe department or industry|Business area that the data comes from, such as IT service management. Required.|
    |Describe the data you want to generate|What each record represents and the information that it contains. Required.|
    |Add categories to generate a diverse dataset|Keywords that define the kinds of records to generate, such as software, hardware, and network. Enter at least three categories, and press Enter after each one. Required.|
    |Select language to generate data in|Language of the generated data. The default is English. The list includes the languages that are installed on your instance.|

5.  Select **Next**.

6.  In the Select sample data stage, choose records to use as examples.

    The LLM doesn't copy your sample data. It uses the examples to understand the structure, format, length, and tone of the records to generate.

    1.  Select where to add sample data from: **Instance table** or **Data Collection**.

    2.  Select the table and the columns to use.

    3.  Select records by using **Random sampling** or **Manually**.

        For random sampling, enter the number of records and select **Run**. To select records manually, select the check box for each record.

7.  Select **Next**.

8.  In the Define columns stage, add the columns to generate, and describe the data for each column.

    If you chose a template, the columns are already filled in. To keep the generated data accurate, use no more than 30 columns.

    |Field|Description|
    |-----|-----------|
    |Column Label|Name of the column. Required.|
    |Data type|Type of data in the column: String, Number, or JSON. The default is String. Required.|
    |Describe the data to generate for this column|What the column contains and how the values should look, such as "The letters INC followed by 7 numbers." Required.|

    To add a column, select **Add column**. To fill in descriptions for every column, select **Generate column descriptions**.

9.  Select **Next**.

10. In the Test data generation stage, enter the **Number of records to generate**.

    Enter a whole number from 10 to 1,000. Optionally, enter **Additional rules** for the generated data.

11. To check the results before you generate the full dataset, select **Generate preview**.

    The preview generates five records. The full dataset contains similar, but not identical, records.

    If a Generation error message appears, make sure that the Generative AI Controller plugin is installed on your instance.

12. Select **Review summary**.

13. In the Review and generate stage, review the settings, and then select **Start generation**.

    To change a stage, select **Edit** in its section.

    The data generation job page opens with a state of Generation in progress. You can leave the page and come back later. The job is listed on the **Synthetic datasets** tab. When the job finishes, the state changes to Generation completed.

    If a Generation error message appears, make sure that the Generative AI Controller plugin is installed on your instance.

14. On the **Output data** tab, review the generated records.

    The records are generated by AI, so check them for accuracy. To remove records, select their check boxes and select **Delete records**. Deleting is unavailable until the job finishes calculating data insights.

15. To reuse these settings for another dataset, select **Save as Template** and enter a template name.

    The template appears in the **Choose a template** list the next time that you generate data with the standard data generator. A template saves the dataset and column definitions, but not the sample data.

16. Select **Add to data asset**.

17. In the Add generated data to data assets dialog box, fill in the fields.

    Enter a **Dataset name**, which is required. Optionally, enter a **Dataset description** and **Tags**.

18. Select **Confirm**.

    The dataset page opens with a state of Active. The page includes a Data Insights tab. The dataset is listed on the **Datasets** tab, and the data generation job stays on the **Synthetic datasets** tab.


## What to do next

After the dataset is Active, you can [scan it for sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/sensitive-data.md), [create a derived dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-derived-dataset.md), [add ground truth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/add-ground-truth.md), or [add it to a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-data-collection.md).

