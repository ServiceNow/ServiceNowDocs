---
title: Generate the Parsing phase for REST-based Data Stream actions
description: Automatically configure the splitter step, script parser step, and outputs for REST-based Data Stream actions. The Test REST step functionality in REST-based Data Stream actions executes a request to the configured REST endpoint, analyzes the response payload, and automatically sets up the parsing and output components.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Data Stream actions and pagination, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Generate the Parsing phase for REST-based Data Stream actions

Automatically configure the splitter step, script parser step, and outputs for REST-based Data Stream actions. The Test REST step functionality in REST-based Data Stream actions executes a request to the configured REST endpoint, analyzes the response payload, and automatically sets up the parsing and output components.

## Before you begin

Role required: action\_designer or admin

## About this task

When a REST step is added to the Request section of a Data Stream action, you can use the REST step's **Test REST Step** button to auto-generate the Parsing section and Outputs. The Parsing section includes the splitter step and parser step. Auto-generating also puts complex object output in the Outputs section. To learn more about the parts of a Data Stream action, see [Data Stream actions and pagination](../concept/data-stream-actions.md).

**Note:** Auto-generating the Parsing phase only applies to REST steps within a Data Stream action. It doesn't apply to other types of steps, such as SOAP or JDBC steps. For REST steps outside of a Data Stream action, the **Run Test** button [tests the step](../../flow-designer/reference/rest-request-action-designer.md).

To auto-generate the Parsing section requires the following.

-   The response body must be valid JSON. You can't auto-generate if the response is not JSON, if the JSON is empty or invalid.
-   The response body must not contain any errors. The response status code can't be 400-599.
-   The object in the response body must contain an array of objects. A valid array of objects is required to parse the data and set the parsing and output components.

The following procedure starts in the REST step of a Data Stream action. For step-by-step instructions on creating a Data Stream action, see [Create a Data Stream action](create-data-stream-action.md).

## Procedure

1.  Navigate to the REST step in your Data Stream action and fill out the fields.

    For field descriptions, see [REST step](../../flow-designer/reference/rest-request-action-designer.md).

2.  Select the **Test REST step** button.

3.  In the Test REST Step box, select **Run Test**.

4.  In the REST Step box, review the results of the test.

5.  If the results are what you expect, select **Continue**.

    -   If the Parsing phase can't be generated because of an issue, such as invalid JSON, there will be an error message in the Test REST Step box. Select **Cancel**, address the issue, and try again.
    -   If there are no issues, and there aren't already configurations for the splitter step, parser step, or Outputs, the Parsing phase and Outputs are automatically generated.
    -   If there are no issues, and there are already configurations for the splitter step, parser step, or Outputs, the Choose which overrides to apply window opens. You can choose to override the splitter step, parser step, Outputs, or a combination of the three. You must select at least one check box to continue. After making your selection\(s\), select **Create Steps**. The selected sections will be regenerated.

## Result

The splitter step, parser step, and outputs are automatically generated. All three can be edited if needed.

**Parent Topic:**[Data Stream actions and pagination](../concept/data-stream-actions.md)

