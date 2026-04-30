---
title: Category users and stakeholders
description: Users who take assessments are individuals in your organization who have specific knowledge of the assessment categories and the records being assessed.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Category users and stakeholders

Users who take assessments are individuals in your organization who have specific knowledge of the assessment categories and the records being assessed.

A person who is qualified to answer assessment questions from metrics in a specific category becomes a category user when associated to that category. A category user then becomes a stakeholder when associated to a specific assessable record.

The system determines which assessable records and questions a user receives by looking at the metric categories and assessable records for which those users are stakeholders. Assessment administrators can create and manage category users and stakeholders.

**Note:** Category users and stakeholders are used only for scheduled assessments.

## Category users

Category users are users who can potentially answer assessment questions about a particular metric category for scheduled assessments. Category users should have special knowledge of the categories and the metrics those categories contain. A category user becomes a stakeholder when associated to an assessable record. Create at least one category user for each category you want to use for assessment questionnaires. There is no need for category users if the category contains only scripted [metrics](../concept/c_AssessmentMetrics.md).

## Stakeholders

A stakeholder is a category user with specific product or service knowledge, who is associated to an assessable record. A stakeholder is familiar with the assessable record and all the metrics within a specific category. The same category user can be associated to multiple assessable records, in which case the system creates a stakeholder record for each association.

There are multiple ways to create stakeholders:

-   Configure the system to create stakeholders automatically.
-   [Associate multiple category users to multiple assessable records](../task/t_AssocMultCatUsrsToMultAssessRecs.md).
-   [Associate multiple category users to one assessable record](../task/t_AssocMultCatUsrsToOneAssessRec.md).
-   [Associate one category user to one assessable record](../task/t_AssocOneCatUsrToOneAssessRec.md).

**Note:** Ensure you establish the desired user and assessable record associations to categories before attempting to creating stakeholders.

-   **[Create a category user](../task/t_CreateACategoryUser.md)**  
Create category users by associating users in the system to metric categories.
-   **[Create stakeholders automatically](../task/t_CreateAStakeholderAutomatically.md)**  
You can configure the system to create stakeholders automatically from all category users and assessable records associated with a category using the **Create stakeholders** check box on the Metric Category form.
-   **[Associate multiple category users to multiple assessable records](../task/t_AssocMultCatUsrsToMultAssessRecs.md)**  
The stakeholder list helper in the create stakeholders module is the most efficient way to associate multiple category users to multiple assessable records in a single interface.
-   **[Associate one category user to one assessable record](../task/t_AssocOneCatUsrToOneAssessRec.md)**  
Create a single stakeholder using the list in the Assessment Stakeholders module.
-   **[Associate multiple category users to one assessable record](../task/t_AssocMultCatUsrsToOneAssessRec.md)**  
Create many stakeholders for a single assessable record from the Assessable Record form.

**Parent Topic:**[Assessment administrator tasks](../concept/c_AssessmentProcess.md)

**Related topics**  


[Create a category user](../task/t_CreateACategoryUser.md)

[Associate multiple category users to multiple assessable records](../task/t_AssocMultCatUsrsToMultAssessRecs.md)

[Associate multiple category users to one assessable record](../task/t_AssocMultCatUsrsToOneAssessRec.md)

[Associate one category user to one assessable record](../task/t_AssocOneCatUsrToOneAssessRec.md)

[Delete a stakeholder for multiple assessable records](../task/t_DelAStakeholderForMultAssessRecs.md)

[Delete a stakeholder for one assessable record](../task/t_DelAStakeholderForOneAssessRec.md)

