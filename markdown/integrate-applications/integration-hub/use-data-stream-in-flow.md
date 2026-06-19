---
title: Use a Data Stream action in a flow
description: Data Stream actions use the For each flow logic option to process stream data in a flow. For example, suppose that you want to use a Data Stream action that imports document data from a third-party site. When added to a flow, the action appears as a For each flow logic block, enabling flow designers to easily create a record in ServiceNow for each object in the data stream.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/use-data-stream-in-flow.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Stream actions and pagination, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Use a Data Stream action in a flow

Data Stream actions use the **For each** flow logic option to process stream data in a flow. For example, suppose that you want to use a Data Stream action that imports document data from a third-party site. When added to a flow, the action appears as a **For each** flow logic block, enabling flow designers to easily create a record in ServiceNow for each object in the data stream.

## Before you begin

Data Stream actions require an Integration Hub subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Role required: flow\_designer or admin.

## Procedure

1.  Open the flow you want to add the Data Stream action to.

2.  Add the Data Stream action to the flow.

    The action appears as a **For Each** flow logic block.

    \[Omitted image "data-stream-in-flow.png"\] Alt text: Data Stream For Each flow logic block.

3.  Add a child action within the **For Each** flow logic block.

    This action runs on each object within the data stream.

    **Note:** You cannot add an action that pauses the flow to a Data Stream For Each flow logic block. Data Stream actions require a constant connection to the response stream. For example, you cannot use the Ask for Approval or Wait for Condition actions within Data Stream For Each flow logic. For more information, see [Data Stream action design considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/data-stream-design.md).

    \[Omitted image "data-stream-for-each.png"\] Alt text: Create Incident Record child action within flow logic block.

4.  Click **Save**.

    Workflow Studio saves a draft of the flow, trigger, and actions.


## What to do next

Test the flow until it is ready to be activated.

**Note:** The system only triggers active flows.

**Parent Topic:**[Data Stream actions and pagination](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/data-stream-actions.md)

