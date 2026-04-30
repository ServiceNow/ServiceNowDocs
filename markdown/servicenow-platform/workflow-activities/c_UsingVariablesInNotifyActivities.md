---
title: Using variables in Notify workflow activities
description: Certain Notify workflow activities support variable substitution for reading text to callers.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using variables in Notify workflow activities

Certain Notify workflow activities support variable substitution for reading text to callers.

Certain Notify workflow activities allow you to use variables, such as those from the workflow scratchpad, to determine the activity behavior. Each activity supports a maximum of 20 variables. The following activities allow variable substitution:

|Activity|Notes|
|--------|-----|
|Say|Supports variable substition in the **Text** field only.|
|Input|Supports variable substition in the **Text** field only.|
|Play|Supports variable substitution in the **URL** field only.|
|Forward call|Supports variable substitution in the **Phone number** field only.|

## Scratchpad variables

You can call variables from the workflow scratchpad or the activity scratchpad using the syntax $\{variable\_name\}. You do not need to include either workflow.scratchpad or activity.scratchpad before the variable name. For example, to use the variable *activity.scratchpad.langCode = ‘en-US’*, call $\{langCode\} within the activity. If the scratchpad does not contain the specified variable, the variable evaluates to an empty value.

You can get values from objects on the scratchpad using the format $\{object.value\}. For example, you can get the name of a user object, such as *workflow.scratchpad.user = \{name:'john.smith'\}* by calling $\{user.name\}.

## The digit variable

The **Input** activity exposes the $\{digit\} variable. Use this variable in each condition presented by the activity. The number read to the user is determined automatically by each condition. The caller can press that number to cause the activity to transition through that condition.

