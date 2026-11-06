---
title: Service Test Group form fields
description: Review the fields on the Service Test Group form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/test-group-fields.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [service test group fields, execution type, automated test group]
breadcrumb: [Reference, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Service Test Group form fields

Review the fields on the Service Test Group form.

To create a test group, see [Create a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/create-test-group.md).

<table id="table_test_group_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Identifier that the system generates for the test group. Read-only.

</td></tr><tr><td>

Name

</td><td>

Name of the test group. Required. Maximum 80 characters.

</td></tr><tr><td>

Description

</td><td>

Description of the test group. Maximum 4,000 characters.

</td></tr><tr><td>

State

</td><td>

State of the test group: Draft, Published, or Retired. Read-only. A new test group starts in the Draft state.

</td></tr><tr><td>

Execution Type

</td><td>

How the test group runs. Manual is the default. You can't change this field after the test group is published.

 -   **Manual**

The test group runs the test definitions that are mapped to it. A manual test group needs at least one test definition before you can publish it. See [Map test definitions to a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/add-test-definitions-to-test-group.md).

-   **Automated**

The test group runs the flow in the **Flow** field.


</td></tr><tr><td>

Flow

</td><td>

Flow that an automated test group runs. For how to create a flow, see [Create a flow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/create-flow.md).

</td></tr><tr><td>

Active

</td><td>

Option that makes the test group available for use. Selected by default.

</td></tr></tbody>
</table>**Related topics**  


[Service Test Management automation framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-automation-framework.md)

[Flows, subflows, and actions installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-flows-and-actions.md)

