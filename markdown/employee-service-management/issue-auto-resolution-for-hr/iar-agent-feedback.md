---
title: Using agent feedback to improve your case criticality predictions
description: By using your agent's feedback to determine how critical a case is, you can improve the machine learning \(ML\) models of the Issue Auto Resolution \(IAR\) application to predict cases more correctly over time.
locale: en-US
release: xanadu
product: Issue Auto Resolution for HR
classification: issue-auto-resolution-for-hr
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Issue Auto Resolution for HR to handle cases, Issue Auto Resolution for HR, HR Service Delivery, Employee Service Management]
---

# Using agent feedback to improve your case criticality predictions

By using your agent's feedback to determine how critical a case is, you can improve the machine learning \(ML\) models of the Issue Auto Resolution \(IAR\) application to predict cases more correctly over time.

When an agent creates a case, Issue Auto Resolution predicts how critical the issue is. However, in the past, these predictions sometimes needed to be improved. To improve the classification of cases through machine learning \(ML\) models, a new field, called the **Resolution requires** field, was introduced for HR agents to give feedback. Agents can only see this field on an HR case form when Issue Auto Resolution has predicted the criticality of that case.​

## Using the resolution requires field

The **Resolution requires** field includes the values that are based on the feedback that the HR agents gave on the criticality prediction. The **Resolution requires** field includes the options that are listed in the following table.

|Name|Description|
|----|-----------|
|Urgent agent action|Immediate agent attention is required to resolve the case.|
|Self-service content only|User could resolve the case with self-service content.|
|Nonurgent agent action|Case is noncritical.|

Agents can choose the correct feedback from the field options to tell when the Issue Auto Resolution predictions are correct or not.

## Resolution priority mapping

Agents see an informational message on the screen when they change the resolution requires, priority, or state of the case​. For example, let's say that an agent selects the **Urgent agent action** option. The priority of it being selected is **Low**, so the agent sees the message "Resolution requires field is inconsistent with case priority. Please review." By using resolution priority mapping, agents can correct the issue when the priority is inconsistent with the urgency of the case.

Informational messages can also appear as priority changes. The resolution requires that an agent makes changes or state changes.

