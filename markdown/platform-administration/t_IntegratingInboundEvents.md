---
title: Integrate inbound events
description: This example illustrates how to create a notification from an inbound JSON request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/t\_IntegratingInboundEvents.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [References, Inbound email, Notifications, Configure core features, Administer]
---

# Integrate inbound events

This example illustrates how to create a notification from an inbound JSON request.

## Before you begin

Role required: admin

## About this task

When complete, you will be able to:

-   Send a JSON request to the \[imp\_notification\] web service import set with the JSON processor
-   Create a new import set in the \[imp\_notification\] table in the instance using data from the JSON request

The following example steps assume you have your own demonstration instance.

## Procedure

1.  Activate the JSON Web Service plugin.

2.  Install the [RESTClient](https://addons.mozilla.org/en_US/firefox/addon/restclient) Firefox plugin.

3.  Open the RESTClient.

4.  Create the following JSON request.

    -   **Method**: POST
    -   **URL**: `http://<instance name>.service-now.com/imp_notification.do?JSON`
    -   **Headers**: Authorization: Basic
    -   **Body**:

        ```
        {"sysparm_action":"insert","message":"this is an event","uuid":"abc"}
        ```

    \[Omitted image "RESTRequest.png"\] Alt text: The REST JSON request

5.  Click **Send**.

6.  Navigate to **Response** &gt; **Response Body \(Raw\)**.

7.  Verify that the instance sends back a response with a `sys_id`.

    \[Omitted image "RESTResponse.png"\] Alt text: The REST response

8.  Login to your development instance.

9.  In Navigation filter, enter `imp_notification.list`.

10. Verify that the import set table has an event matching your JSON request.

    \[Omitted image "RESTImportSetTable.png"\] Alt text: REST import set table


**Parent Topic:**[References for Inbound email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/references-inbound-email.md)

