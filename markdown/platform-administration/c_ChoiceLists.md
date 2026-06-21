---
title: Choice list field type
description: A choice list is a type of field that lets the user select from a pre-defined set of choices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/c\_ChoiceLists.html
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Choice list field type

A choice list is a type of field that lets the user select from a pre-defined set of choices.

Administrators can define the available choices and customize the behavior and appearance of choice lists.

\[Omitted image "IncidentStateChoiceList.png"\] Alt text: Choice list with New selected

**Note:** Choice lists do not support a one to many relationship. Only one choice from a choice list can be selected at a time.

-   **[Choice list security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/c_ChoiceListSecurity.md)**  
You can use the personalize\_choices security role to enable non-administrators modify Choice elements options on all tables.
-   **[Values to associate with choice labels for scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/c_DetermValsAssocWChoicesScripting.md)**  
When you write a script that references a choice list, you need to know the value that is associated with each choice.
-   **[Integer values for default choice lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/c_IntValsForDfltChoiceList.md)**  
Choice provide four default values.
-   **[Configure state field choice values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/c_BPForStateFieldChoiceValues.md)**  
State fields are a subset of choice list fields. Keep the following information in mind when you configure choice values for the state field.
-   **[View choice list definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/t_ViewChoiceListDefinitions.md)**  
The Choice Set \[sys\_choice\_set\] table contains a record for every field that uses a choice list.

**Parent Topic:**[Field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/r_FieldTypes.md)

