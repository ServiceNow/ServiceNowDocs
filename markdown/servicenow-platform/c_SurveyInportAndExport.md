---
title: Sharing surveys
description: You can export a survey and then import it to a different ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/c\_SurveyInportAndExport.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Survey distribution, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Sharing surveys

You can export a survey and then import it to a different ServiceNow instance.

**Note:** Update sets are available in the Helsinki release and should be used to move data from one instance to another. For information about update sets, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets.md).

The system exports a single XML file that contains a survey definition \[asmt\_metric\_type\] and the associated records, including the following.

-   Assessment Metric Template \[asmt\_template\]
-   Assessment Template Definition \[asmt\_template\_definition\]
-   Metric definitions \[asmt\_metric\_definition\] \(survey question answer options\)
-   Scheduled Jobs associated with the Survey \[sys\_trigger\]
-   Survey categories \[asmt\_metric\_category\]
-   Survey questions \[asmt\_metric\]
-   Survey users \[asmt\_m2m\_category\_user\]
-   Trigger Condition \[asmt\_condition\]

-   **[Export a survey](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ExportASurvey.md)**  
You can export a survey and then import it to another instance.
-   **[Import a survey](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ImportASurvey.md)**  
You can import a survey that has been exported as an XML file. The exported XML file does not contain result data.
-   **[Use update sets for surveys and assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_UseUpdateSetsForSurveyAssess.md)**  
Use an update set to capture changes to surveys and assessments.

**Parent Topic:**[Survey distribution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SurveyDistribution.md)

**Related topics**  


[Email notifications for surveys]()

[Send survey invitations to users]()

[Define a recipients list for surveys]()

[Add a recipients list to a survey]()

[Embed a survey within the Outlook email client]()

[Enable localization for a survey]()

[Survey URLs]()

[Create a survey module]()

[Configure a survey in the Connect chat support]()

