---
title: MID Server support for Data Stream actions
description: Get data through a ServiceNow MID Server when running a Data Stream action.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data Stream actions and pagination, Build integrations, Integration Hub, Workflow Data Fabric]
---

# MID Server support for Data Stream actions

Get data through a ServiceNow® MID Server when running a Data Stream action.

When selected, the MID Server retrieves the data and sends each page to the instance as an attachment to process.

**Important:** When running the Data Stream action within flow, the actions in the **For Each** block always run on the instance.

These steps can run on either the MID Server or the instance:

-   Action Preprocessing Script
-   Request Script step
-   REST or SOAP step

**Note:** Avoid shifting the execution environment between the instance and the MID Server multiple times. For example, you might configure the Request Script step to run on the MID Server, but the REST step to run on the instance. In this case, the system shifts environments between the instance and MID Server for every page of data, which may degrade performance.

To learn more about running a step on a MID Server, see [Integration steps](integration-steps.md).

## Size limits

If your system encounters a timeout or size limit issue, try making one of these adjustments:

-   **Increase the REST transaction quota rule**

    If the connection between the instance and the MID Server slows down, you may encounter a timeout while waiting for a response from the REST step. Increase the default timeout by updating the **REST Attachment API request timeout** transaction quota rule.

    -   Default: 60 seconds
    -   Maximum: 300 seconds
-   **Increase the instance timeout**

    By default, the instance waits for 600 seconds to retrieve a single page of data from a MID Server. If you encounter a timeout when running a Data Stream action through a MID Server, change this default by increasing the **datastream\_alternative\_env\_fetch\_page\_timeout\_seconds** system property.

    -   Default: 600 seconds
    -   Maximum: 7200 seconds
-   **Increase attachment size**

    The MID Server sends each page of data to the instance as an attachment. If a page of data is large, it may exceed the allowed attachment size. Increase the allowed size by updating the **com.glide.attachment.max\_size** system property.

    -   Default: 1024 MB
    -   Maximum: None

**Parent Topic:**[Data Stream actions and pagination](data-stream-actions.md)

