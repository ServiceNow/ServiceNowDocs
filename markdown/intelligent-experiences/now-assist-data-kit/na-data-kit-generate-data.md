---
title: Generate synthetic data
description: Create synthetic data with a sample dataset and a prompt through generative AI by using the Now Assist Data Kit application. You can use synthetic data to create training for a test model or an evaluation dataset.
locale: en-US
release: zurich
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# Generate synthetic data

Create synthetic data with a sample dataset and a prompt through generative AI by using the Now Assist Data Kit application. You can use synthetic data to create training for a test model or an evaluation dataset.

## Before you begin

Role required: sn\_data\_kit.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Data Kit** &gt; **Home**.

2.  Select the **Synthetic datasets** tab.

3.  Select **Generate dataset**.

4.  Choose how you want to generate data.

    |Method|Description|
    |------|-----------|
    |Standard data generator|The standard data generator creates flat records based on a fixed schema with files like name, description, and short description. By providing a few examples, the model learns the structure and generates consistent, realistic data, making it suitable for typical use cases. These configurations can also be saved as templates for easy reuse.|
    |Multi-table data generator|A multi-table data generator creates realistic test data for several related tables at once. It automatically figures out the right order, groups linked records into meaningful scenarios, and fulls in details using rules or AI. This enables you to use the data generated for testing or demos.|

5.  On the Add job info page, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Job name|Name of the generated data.|

6.  Navigate to **Define data** .

7.  Select a template.

    |Template|Description|
    |--------|-----------|
    |Catalog item|Service Catalog is a user-friendly interface that allows end-users to browse, request, and manage services and products offered by the organization, streamlining self-service and improving operational efficiency.|
    |Incident data|Information Technology Service Management is a business function that involves managing IT services and processes to meet business needs effectively.|

    ![Define data screen.](../image/nadk-data-template.png)

8.  Select the language for the data generation.

9.  On the form, fill in the rest of the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Department or industry where the data belongs.|
    |Type|Data that you want to generate.|
    |Category|Data that has been categorized with keywords.|
    |Count|Number of records to generate.|

    **Note:** If you have sample data available, you can navigate to [Select the sample data](select-sample-data.md) to enhance the accuracy of the generated data. If you don't have sample data, refer to the in-product help for guidance.

10. Select **Continue**.

11. Add your sample data by navigating to [Define columns to generate data](na-data-kit-define-columns.md).

    The columns are populated when you add the sample data. If no sample data is available, you must manually populate the columns with data.

12. Select **Continue**.

13. Add additional rules to improve generated data.

14. Select the number of records to generate for testing.

15. Select **Start generation**.


