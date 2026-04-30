---
title: Questions in data visualizations
description: You can group or filter table data in data visualizations by questions. The table must support questions.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-03-11"
reading_time_minutes: 1
breadcrumb: [Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Questions in data visualizations

You can group or filter table data in data visualizations by questions. The table must support questions.

Creating data visualizations grouped by questions is helpful to:

-   Determine whether questions that customers ask are getting answered.
-   Gain more information from customers during the request process.

The data source must be a non-service catalog table that has questions associated with it. You can filter or group by questions on a table extended from the Task \[task\] table, for example the Incident \[incident\] or Problem \[problem\] tables, or from the Record Producer table \[sc\_cat\_item\_producer\].

You can use questions when you create custom conditions to filter the data source. You can also use questions in any Group by or Alternative group by fields that the type of data visualization supports.

**Note:**

If there is a Record Producer associated with the table, variables defined in that Record Producer are available as Questions in the condition builder for filtering the data source, except for the following question types:

-   Label
-   Rich text label
-   Macro
-   Container

You cannot group by Record Producer variables. For more information, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

-   **[Use questions in data visualizations](../task/use-questions-dv.md)**  
In visualizations of data from the Task \[task\] hierarchy of tables, you can use questions defined for the table to filter or group the data.

**Parent Topic:**[Configure data visualizations](../../performance-analytics/concept/configure-data-visualizations.md)

