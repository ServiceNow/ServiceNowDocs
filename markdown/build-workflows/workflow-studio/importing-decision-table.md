---
title: Import a Decision table from an Instance to another using update sets
description: Importing a decision table from one instance to another using update sets. This process reduces the time required to recreate the table across different instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/importing-decision-table.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [decision table, export, migration]
breadcrumb: [Decision tables reference, Reference, Workflow Studio, Build workflows]
---

# Import a Decision table from an Instance to another using update sets

Importing a decision table from one instance to another using update sets. This process reduces the time required to recreate the table across different instances.

## Before you begin

Role required: admin

## Procedure

1.  Importing the Decision Table Using the Update Set
2.  In the target instance, navigate to **All** &gt; **System Update Sets** &gt; **Retrieve Update Sets**.

3.  Under **Related Links**, select **Import Update Set from XML**.

4.  In the file selection dialog, choose the XML file and select **Upload**.

5.  From the list, select the uploaded update set to view the record.

6.  Select **Preview Update Set** to preview the data.

7.  Select **Commit Update Set** to commit the changes.

8.  Navigate to **All** &gt; **Decision Tables**.

    The exported decision table appears in the list.

9.  Select **Create Draft**.

10. To validate that the correct values are mapped to the table, under **Decision Tables**, select **Import** and upload the Excel file.

    The decision table imports successfully to the target instance.


**Parent Topic:**[Decision tables reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/decision-builder-reference.md)

