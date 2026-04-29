---
title: Support and troubleshooting
description: Common troubleshooting options when you set up the integration for the Service Graph Connector for ServiceNow OT Discovery.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connector for ServiceNow Operational Technology\(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Support and troubleshooting

Common troubleshooting options when you set up the integration for the Service Graph Connector for ServiceNow OT Discovery.

## Test the connection

You can test the connection after configuring your URL and credentials for the integration. If everything is configured correctly, the service graph connection displays a successful connection test without any error. If something goes wrong during the connection, the Service Graph connection displays the error message, error code, and response body from the API.

![Displays error message, error code, and response body from the API.](../../sgc-ot-discovery/image/mission-secure-troubleshooting-test.png)

## Review Outbound HTTP Request records

You can also review the Outbound HTTP Request records associated with the test. Navigate to **All** &gt; **System Logs** &gt; **Outbound HTTP Requests**.

![Review the Outbound HTTP Request records associated with the test](../../sgc-ot-discovery/image/mission-secure-outbound-request.png)

In the list view, you should see the URL hostname that you specified when setting up the connection parameters. Open this record to view the connection details.

![Review the URL hostname that you specified when setting up the connection parameters](../../sgc-ot-discovery/image/mission-secure-outbound-log.png)

By default, the log level is set to Basic, so you can’t see the response body or quest body, but the response status indicates the issue. For example, a 401 in the Response status indicates an unauthorized request. To resolve the issue, navigate to the connection and verify that you have the correct Client ID and Client Secret entered for the connection. For more information, see [Install the Service Graph Connector for ServiceNow Operational Technology Discovery](../../sgc-ot-discovery/task/install-sgc-ot-discovery.md).

## Additional diagnosis

If you must diagnose further, you can override the log level to give more information, for example using the global system properties. Navigate to the system properties by going to **sys\_properties.list** in the application navigator and update the **glide.outbound\_http\_log.override** to the value true and update the **glide.outbound\_http\_log.override.level** to an appropriate value. For example, change value to **All**.

**Note:** You can perform action only for a limited period of time for troubleshooting. Make sure you revert the changes to the original configuration.

![Override log level by modifying global parameters](../../sgc-ot-discovery/image/mission-secure-additional-diagnosis.png)

With extended logging turned on, you can provide additional details for requests after that to give more context to the issue.

If you encounter a response status of 401, it’s typically an issue with your credentials. To resolve, navigate to the connection in the Flow Designer and verify that the API Key is filled in as expected with the correct value.

If you encounter any issues with the flattening of the Asset or missing data from the API, you can run a test load and validate the flattened data from the Staging table. Then compare it with the **api\_data** to see if the data was provided from the API.

