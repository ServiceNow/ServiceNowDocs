---
title: Import existing data from other systems
description: Import existing data \(third parties, engagements, assessments, questionnaires, issues, and so on\) from other systems \(like the Aravo platform, the ProcessUnity platform, and so on\). You aren’t charged for importing the data.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Import existing data from other systems

Import existing data \(third parties, engagements, assessments, questionnaires, issues, and so on\) from other systems \(like the Aravo platform, the ProcessUnity platform, and so on\). You aren’t charged for importing the data.

## Before you begin

Role required: admin

## About this task

The overall process of importing data into your instance is discussed at [Import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/import-sets-landing-page.md).

You will find a learning module that takes you through the process of importing data at [https://developer.servicenow.com/dev.do\#!/learn/courses/sandiego/app\_store\_learnv2\_importingdata\_sandiego\_importing\_data\_into\_servicenow](https://developer.servicenow.com/dev.do#!/learn/courses/sandiego/app_store_learnv2_importingdata_sandiego_importing_data_into_servicenow).

An article on running transform maps appears at [https://developer.servicenow.com/dev.do\#!/learn/courses/sandiego/app\_store\_learnv2\_importingdata\_sandiego\_importing\_data\_into\_servicenow/app\_store\_learnv2\_importingdata\_sandiego\_importing\_data/app\_store\_learnv2\_importingdata\_sandiego\_run\_a\_transform\_map](https://developer.servicenow.com/dev.do#!/learn/courses/sandiego/app_store_learnv2_importingdata_sandiego_importing_data_into_servicenow/app_store_learnv2_importingdata_sandiego_importing_data/app_store_learnv2_importingdata_sandiego_run_a_transform_map).

**Important:** To import the data without being charged, you must turn off the "Run business rules" option before running the transform map to import the data. If you do not turn off business rules, then the imported data records are marked as activity and you will be charged for a license.

## Procedure

1.  Create a transform map.

    See [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md) for instructions.

    **Important:** Clear the **Run business rules** check box before you run the transform map.

2.  Run the transform map and repeat the process for each data set.


**Related topics**  


[Import a questionnaire from a spreadsheet](../../grc-vendor-risk/task/import-questions-from-excel.md)

