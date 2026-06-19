---
title: Configure a test tool in DevOps
description: Configure a test tool in DevOps to view unit, functional, and performance test results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-change-velocity/create-test-tool-dev-ops.html
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DevOps test tool integration, User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure a test tool in DevOps

Configure a test tool in DevOps to view unit, functional, and performance test results.

## Before you begin

Role required: sn\_devops.admin

## Procedure

1.  Navigate to **All** &gt; **DevOps** &gt; **Integrations** &gt; **Test Type Mappings** and create a record to map the test type to the integration tool.

2.  In the Test Type Mapping record, use the search icon \(\[Omitted image "dev-ops-search-icon.png"\] Alt text: Search icon\) to select **Test type** and **Tool integration** field values.

    \[Omitted image "dev-ops-test-type-mapping.png"\] Alt text: DevOps test type mapping

3.  Click the search icon \(\[Omitted image "dev-ops-search-icon.png"\] Alt text: Search icon\) in the **DevOps Entity Id** field, and fill in the test details.

<table id="table_zrv_f4x_pnb"><tbody><tr><td>

Table name

</td><td>

DevOps table name that contains the entity linked to the test results.

</td></tr><tr><td>

Document

</td><td>

Name of the entity specified in the selected table.

</td></tr></tbody>
</table>    \[Omitted image "dev-ops-test-map-entity-id.png"\] Alt text: DevOps test mapping entity id

    See the [Test type mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/dev-ops-test-tool-integration.md) section for more details.

4.  To capture the raw test payload of non-JUnit or -TestNG tests, enter an .xml filename and path \(comma separate multiple files\).

    You can transform a raw payload using decision tables and a custom Workflow Studio subflow.

    **Note:** You must create the custom subflow that transforms the raw payload.

    See the [Transforming a raw test payload](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/dev-ops-test-tool-integration.md) section for more details on configuring decision tables.

5.  Run the test and view test results by navigating to **DevOps** &gt; **Test Results** \(Test Summaries and Performance Test Summaries\).

    \[Omitted image "dev-ops-test-results-summary.png"\] Alt text: DevOps test summaries


## Example

\[Omitted image "dev-ops-test-scripted-pipeline.png"\] Alt text: DevOps test scripted pipeline

**Parent Topic:**[DevOps test tool integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/dev-ops-test-tool-integration.md)

