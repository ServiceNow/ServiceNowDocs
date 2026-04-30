---
title: Tokens in Proactive Prompts
description: Token placeholders indicate the data that will be replaced during runtime.
locale: en-US
release: xanadu
product: Proactive Prompts
classification: proactive-prompts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference for Proactive Prompts, Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Tokens in Proactive Prompts

Token placeholders indicate the data that will be replaced during runtime.

When creating a signal, the message displayed to the user is written in the Single record display and Multiple record display fields. Use tokens in these messages to indicate data that will be replaced dynamically during runtime. For example, the message "Hey $\{receiving\_user\}, looks like $\{user\_count\} members in your team haven't taken PTO in the last quarter" will be displayed as "Hey Abel Tuter, looks like 2 members in your team haven't taken PTO in the last quarter".

## Types of Tokens

-   receiving\_user: Name of the recipient of the prompt.
-   user\_name: Name of the employee.

    **Note:** If the recipient is the manager and only one employee under that manager qualifies for the signal, use the employee's name directly with this token.

-   user\_count: Count of employees under the manager that qualify for the signal.
-   item\_count: Count of records belonging to the employee that qualified the signal.
-   item: If only one record belongs to the employee that qualifies the signal, the value in the Display field of the data source is stored in this token.
-   score: The score used in the threshold evaluation.

**Note:** \* indicates that tokens can only be used when the **Collect records** field is selected.

|Data source type|Persona|Tokens \(Single record\)|Tokens \(Multiple records\)|
|----------------|-------|------------------------|---------------------------|
|Simple|Manager|None|receiving\_user, user\_count|
|Aggregate as count|Manager|receiving\_user,item\_count, user\_name|receiving\_user, user\_count|
|Aggregate as none|Manager|receiving\_user,item\_count, user\_name|receiving\_user, user\_count|
|Script|Manager|receiving\_user,item\_count\*, user\_name|receiving\_user, user\_count|
|Performance Analytics Indicator|Manager|receiving\_user,score, item\_count\*,user\_name|receiving\_user, user\_count|
|Simple|Employee| | |
|Aggregate as count|Employee|receiving\_user,score, item\*|receiving\_user, item\_count|
|Aggregate as none|Employee|receiving\_user, score, item\*|receiving\_user, item\_count|
|Script|Employee|receiving\_user, score, item\*|receiving\_user, item\_count\*|
|Performance Analytics Indicator|Employee|receiving\_user, score, item\*|receiving\_user, item\_count\*|

**Parent Topic:**[Reference for Proactive Prompts](proactive-prompts-reference.md)

**Related topics**  


[Components installed with Proactive Prompts](proactive-prompts-components.md)

[Types of data sources in Proactive Prompts](proactive-prompts-data-source.md)

[Actions and action groups in Proactive Prompts](proactive-prompts-actions.md)

[Signal data source form](proactive-prompts-signal-datasource-form.md)

[Signal configuration form](proactive-prompts-create-signal-form.md)

