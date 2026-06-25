---
title: Create a serverless discovery schedule for Rubrik cluster discovery
description: Set up a dedicated discovery schedule for each Rubrik cluster \(Brik\) to identify cluster resources using a serverless pattern and credential alias.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-rubrik.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 2
keywords: [Rubrik discovery, serverless discovery]
breadcrumb: [Rubrik Cluster, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create a serverless discovery schedule for Rubrik cluster discovery

Set up a dedicated discovery schedule for each Rubrik cluster \(Brik\) to identify cluster resources using a serverless pattern and credential alias.

## Before you begin

-   Verify the MID Server is set to Active and can reach the target Rubrik cluster.
-   Create an alias for the basic authentication credential. For more information, see [Create a basic authentication credential alias for Rubrik discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-rubrik.md).
-   Obtain the IP address of one of the Rubrik nodes in the target cluster.

Role required: discovery\_admin

## About this task

Each Rubrik cluster \(Brik\) requires a separate serverless discovery schedule. Each schedule must include the IP address of one of the Rubrik nodes in that cluster, and the credential alias associated with the Rubrik basic authentication credential record.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  Create the discovery schedule record.

    1.  Select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for this discovery schedule. For example, `Discover Rubrik`.|
        |Discover|Scan type. Select **Serverless**.|
        |MID server|Name of the MID Server to use for this schedule.|
        |Active|When selected, activates this schedule for discovery runs.|

    3.  Select **Submit**.

3.  Create the execution pattern.

    1.  In the Discovery Schedules page, select the record you created.

    2.  In the **Serverless Execution Patterns** tab, select **New**.

    3.  On the form, fill in the fields.

<table id="table_tvt_glv_rubrik"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for this record.

</td></tr><tr><td>

Pattern

</td><td>

Pattern to use for this schedule. Select the Rubrik cluster \(LP\) pattern.

</td></tr><tr><td>

Run Child Patterns

</td><td>

Set to **true** for each Rubrik discovery pattern. All child patterns associated with the Rubrik discovery pattern run automatically. This behavior is required by the Large Payload \(LP\) mechanism, which discovers the Rubrik cluster and all corresponding CI types.

</td></tr><tr><td>

Active

</td><td>

When selected, activates this schedule for discovery runs.

</td></tr></tbody>
</table>    4.  Select **Submit**.

4.  Set the pattern launcher parameters.

    1.  In the **Discovery Pattern Launcher Parameters** tab, select the record you created.

    2.  On the form, fill in the fields.

        |Parameter|Value|
        |---------|-----|
        |**ip\_address**|IP address of one of the Rubrik nodes in the cluster.|
        |**credential\_alias**|ID of the credential alias you created for the Rubrik Basic Auth credential record.|

    3.  Select **Submit**.


## What to do next

Either execute discovery immediately by selecting **Discover now** or wait until the predefined schedule triggers the discovery.

**Parent Topic:**[Rubrik Cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/rubrik-discovery.md)

**Related topics**  


[Rubrik Cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/rubrik-discovery.md)

