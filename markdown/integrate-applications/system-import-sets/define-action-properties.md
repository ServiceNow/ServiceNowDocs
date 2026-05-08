---
title: Define action properties
description: Create and configure a Data Source request action in Integration Hub. After the request action is published in Integration Hub, you can choose it as a Request action in the Data Source record.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a REST \(Integration Hub\) type data source, Create a data source, Data sources, Import sets, Imports, Workflow Data Fabric]
---

# Define action properties

Create and configure a Data Source request action in Integration Hub. After the request action is published in Integration Hub, you can choose it as a **Request action** in the Data Source record.

## Before you begin

Role required: import\_admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Data Sources**.

2.  Select **New**.

3.  Select a **Type** of **REST \(IntegrationHub\)**.

4.  Click the link under **Request action**.

5.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the request action.|
    |Accessible From|Scope from which the request action is accessible.|
    |Category|Category of the request action.|
    |Protection|Specifies whether the request action is read-only.|
    |Description|Description of the request action.|
    |Application|Scope of the application.|
    |In-Flow Annotation|Text you want to appear under the **Action** title on the Data Source Request Action page.|

6.  Click **Submit**.

7.  The Data Source Request Action page appears with the following fields:

    |Field|Description|
    |-----|-----------|
    |Limit|Limit set by the user in the REST \(IntegrationHub\) data source record. If the REST API supports pagination and **Support pagination** is selected in the Data Source record, you must supply this input to your REST step.|
    |Offset|Offset set by user in the REST \(IntegrationHub\) data source record. If the REST API supports pagination and **Support pagination** is selected in the Data Source record, you must supply this input to your REST step.|
    |Last Success Import Time|Last time data was successfully imported. A numeric value representing the number of milliseconds since January 1, 1970, 00:00:00 GMT. The data source populates this value. If the REST API supports queries based on time, you must supply this input to your REST step.|
    |Import Start Time|Time the import is actually started. A numeric value representing the number of milliseconds since January 1, 1970, 00:00:00 GMT. The data source populates this value. If the REST API supports queries based on time, you must supply this input to your REST step.|

8.  If desired, you can add a Script step to validate or modify action inputs, set default values, or build request payloads before executing the REST step.

    1.  Select **Data Source Request** from the Action Outline.

    2.  Select **Enable Processing Script**.

    3.  Select **Script step** from the Action Outline.

    4.  Configure the Script step as described in [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

9.  Select **REST step** from the Action Outline.

10. Configure the REST step as described in [REST step](https://www.servicenow.com/docs/access?context=rest-request-action-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

11. Choose from the following:

    -   Click **Properties** to return to the Action Properties window.
    -   Click **Test** to test the request action before publishing it.
    -   Click **Executions** to view the history of executions of the request action.
    -   Click **Save** to save the request action.
    -   Click **Publish** to publish the request action and make it available for use.

**Parent Topic:**[Create a REST \(Integration Hub\) type data source](create-rest-type-data-source.md)

