---
title: Add a ground truth to each dataset record
description: Add a ground truth, which is the real-world data that is used to train and test AI models to each dataset record. You can perform this task by using the AI Data Kit application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/add-ground-truth.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-10-16"
reading_time_minutes: 4
breadcrumb: [Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Add a ground truth to each dataset record

Add a ground truth, which is the real-world data that is used to train and test AI models to each dataset record. You can perform this task by using the AI Data Kit application.

## Before you begin

The data collection that you want to label must be published. For details, see [Create a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-data-collection.md).

Role required: sn\_data\_kit.admin

## About this task

When you publish a labeling project, it creates one labeling task for each record in the data collection and assigns the tasks to your labelers in turn. Labelers enter the ground truth for each record. When labeling is finished, you mark the project complete, which creates a dataset and a data collection that contain the results.

Templates give you a starting point. The Manual ground truth template sets up a layout in which labelers write each ground truth value themselves. The AI generated ground truth template uses AI to help create ground truth values.

## Procedure

1.  Navigate to **All** &gt; **AI Data Kit** &gt; **Home**.

2.  In the Data labeling section, on the **Projects** tab, select **Create project**.

3.  Select **Use template**, select a template such as **Manual ground truth**, and then select **Create project**.

4.  On the Details tab, fill in the fields, and then select **Continue**.

    |Field|Description|
    |-----|-----------|
    |Project name|Name of the project. The template fills this in. Required.|
    |Description|Description of the project. The template fills this in.|
    |Labeling instructions|Instructions that tell labelers what to write for each record. The field shows example text until you enter your own. For example: "Write a one- or two-sentence summary of the incident that an agent could read at a glance. Include the affected service and the main symptom. Don't include names or contact details." Required.|
    |Add labelers you'll assign tasks to|People who complete the labeling tasks. Only users with an AI Data Kit role are available. Required.|

5.  On the Add data tab, select the data collection to label, and then select **Continue**.

    Only published data collections are available. The tab shows the number of records in the collection and a preview of the records.

6.  On the Add a preprocessor tab, select **Add preprocessor** to process the data before labeling.

    A preprocessor runs a subflow on the data, such as one that generates ground truth values for labelers to review. Enter a **Display name** and select a **Subflow**. Other fields depend on the subflow. If you add more than one preprocessor, they run in the order listed.

    You can't continue while a preprocessor has empty required fields. To remove a preprocessor, select the delete icon.

7.  Select **Continue**.

8.  On the Project layout tab, set up the components that labelers see in each task.

    A layout has one or more sections. Each section has one or more columns, and each column contains components. A typical layout shows the record's fields in one column and an editor for the ground truth in the other.

    To change a component, select its edit icon. To add one, select **Add Component**.

    |Setting|Description|
    |-------|-----------|
    |Component name|Label for the component. It also becomes the column name in the dataset that's created when you mark the project complete. Give the ground truth component a clear name, such as Ground truth. Required.|
    |Component type|Kind of field, such as Short text, Text area, or Rich text. Required.|
    |Read only component|Whether labelers can change the value.|
    |Input source|Where the value comes from. **From data source** shows a column from the data collection. **From preprocessor** shows a value that a preprocessor produced. **Manually** uses a value that you enter. Required.|
    |Map to column|Column in the data collection that the component shows. Available when the input source is From data source.|

    The layout doesn't list the collection's column names. Before you map components, check the column names on the data collection's page.

    Don't map the ground truth component to a column in the collection. If you do, every task starts with that column's value instead of an empty field for the labeler.

9.  Check the preview, and then select **Continue**.

10. On the Project summary tab, review the project, and then select **Publish**.

    **Important:**

    After you publish a project, you can't change it. Make sure that the labeling instructions, labelers, data collection, and layout are correct.

11. In the Publish project dialog box, select **Publish**.

    The project page opens with a state of In progress. It shows task counts and a list of the labeling tasks, each with its assigned labeler and source record.


## What to do next

Labelers complete their tasks. For details, see [Complete labeling tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/complete-labeling-tasks.md). When labeling is finished, mark the project complete. For details, see [Mark a labeling project complete](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/mark-labeling-project-complete.md).

To reuse this project's setup, select **Create template** on the project page.

