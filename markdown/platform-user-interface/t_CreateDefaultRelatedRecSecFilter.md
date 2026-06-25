---
title: Create a default filter for list selector records
description: You can set a default filter to restrict which related records users can select when editing a reference field. Default filters are simple to set up but lack a dynamic filtering element, which prevents the end user from changing the default filter.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/t\_CreateDefaultRelatedRecSecFilter.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Related lists, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a default filter for list selector records

You can set a default filter to restrict which related records users can select when editing a reference field. Default filters are simple to set up but lack a dynamic filtering element, which prevents the end user from changing the default filter.

## Before you begin

Role required: personalize\_list

## About this task

A filter is used to restrict the records that are listed in the slushbucket that displays when a user clicks **Edit** in a related list.

## Procedure

1.  Right-click any column heading and select **Configure** &gt; **List Control**.

2.  Configure the List Control form to add the **Edit default filter** field, if necessary.

3.  In the **Edit default filter** field, use the condition builder to create a default filter.

4.  Select **Update**.

    When users click the **Edit** button in the related list, the list of records they can select is filtered according to the default filter.


**Parent Topic:**[Related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_RelatedLists.md)

**Related topics**  


[Select or create records in a related list]()

[Configure when a related list loads]()

[Create a default filter for a related list]()

[Configure the edit option]()

[Create defined related lists]()

[Add fields to selections in a related list]()

[Configure reference qualifiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ConfigureReferenceQualifiers.md)

[Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md)

