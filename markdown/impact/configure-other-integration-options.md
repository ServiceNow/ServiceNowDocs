---
title: Configure other integration options
description: Perform the following procedure to configure options other than ServiceNow, Azure, or Jira.The following leading practices are guidelines for creating other integration type scripts.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User story integration, Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure other integration options

Perform the following procedure to configure options other than ServiceNow, Azure, or Jira.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\)

## Procedure

1.  Select **Other** as the integration type.

2.  Enter your:

    -   Integration name
    -   End point
    -   Content type
    -   Issue type
3.  **Payload** contains the script used by the task creation integration.

4.  Enter your username and API token which will allow authentication to your connection point.


## Other integration leading practices

The following leading practices are guidelines for creating other integration type scripts.

-   This integration allows a more generic approach to building a request body object to send to a third-party API.
-   The **Payload** field is used to format the request body.
-   The API called is determined by the endpoint, and the credentials provided on the form are used in a basic authentication authorization to the third-party tool.
-   The endpoint should be the URL to the API you are calling. You will need to know what is needed in the request body to format the payload correctly. Refer to documentation for your third-party API tool to learn what format is needed in the request body.
-   Currently, only basic authentication is supported when using **Other** as the integration type.

There are several predefined variables available for **Other** type integrations:

<table id="table_csf_rdy_2hc"><tbody><tr><td>

payload

</td><td>

The content you want to send in the request body.

</td></tr><tr><td>

grFinding

</td><td>

The glide record of the finding that sends the request.

</td></tr><tr><td>

workItemType

</td><td>

The work item type selected for the Other integration.

</td></tr></tbody>
</table>