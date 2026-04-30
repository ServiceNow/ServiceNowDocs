---
title: Migrated question review
description: To maintain accurate result calculations, you may need to make minor adjustments to some of the migrated survey records to ensure results are calculated correctly.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Legacy survey migration, Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Migrated question review

To maintain accurate result calculations, you may need to make minor adjustments to some of the migrated survey records to ensure results are calculated correctly.

**Note:** The assessment engine provides a built-in result calculation feature that converts each survey response to a score between 0 and 10. The configuration required to maintain accurate result calculations is advanced and is not recommended for basic survey implementations. If you do not plan to use result calculation data, ignore the information in this section.

For each legacy question migrated, the system creates a survey question record on the Assessment Metric \[asmt\_metric\] table. For legacy questions of the **Multiple Choice** and **Select Box** types, the system also creates a metric definition record, on the Assessment Metric Definition \[asmt\_metric\_definition\] table, for each legacy question choice.

|Survey question choice field|Related metric definition field|
|----------------------------|-------------------------------|
|Text|Display|
|Value \(can be any string value\)|Value \(must be a numerical value\)|
|Order|Value \(metric definition with smallest **Value** is first\)|

When the system migrates legacy survey question choices, it uses the legacy **Order** to set each metric definition **Value**. For the legacy question choice with the smallest **Order**, the corresponding metric definition **Value** is set to **1**. For the legacy question choice with the next smallest **Order**, the metric definition **Value** is **2**, and so on.

The **Scale definition** field on the migrated Survey Question form determines whether smaller or bigger metric definition values equate to a good score in survey result calculations. By default, the scale definition is set to **High**, meaning bigger values are good. When you migrate a legacy survey, check that the default scale definition makes sense for each question.

For example, the following tables depict a sample migrated question and the metric definitions automatically created for it. Recall that the system uses the order of the legacy survey question choices to set the metric definition value. **Excellent** has the lowest **Order** value, so when the system creates a metric definition for this question choice, the **Value** is set to **1**. In this case the default scale definition value, **High**, does not make sense, as the system will calculate the worst scores for responses of **Excellent**.

|Question choice text|Question choice vlue|Question choice order|
|--------------------|--------------------|---------------------|
|Excellent|A|100|
|Good|B|200|
|Fair|C|300|
|Poor|D|400|

|Metric definition display|Metric definition value|
|-------------------------|-----------------------|
|Excellent|1|
|Good|2|
|Fair|3|
|Poor|4|

If there are no **Order** values for the legacy survey question choices, the system sets each corresponding metric definition **Value** based on the alphanumeric order of the legacy **Text** value.

|Metric definition display|Metric definition value|
|-------------------------|-----------------------|
|Excellent|1|
|Good|2|
|Fair|3|
|Poor|4|

You may also need to change the **Scale definition** setting for other migrated questions. For details, see the scale definition recommendations for each survey question data type.

**Parent Topic:**[Legacy survey migration](../concept/c_MigrateSurveys.md)

**Related topics**  


[Migrate a legacy survey](../task/t_MigrateALegacySurvey.md)

[Survey question migration](r_SurveyQuestionMigration.md)

[Migrated components](r_MigratedComponents.md)

