---
title: Create and configure a scripted REST API for your custom chat integration
description: Create a scripted REST API, add a scripted REST resource, set security and content negotiation, and set REST API rate limits.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create conversational custom chat integration, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create and configure a scripted REST API for your custom chat integration

Create a scripted REST API, add a scripted REST resource, set security and content negotiation, and set REST API rate limits.

## Before you begin

[Map rich controls to the channel in your custom chat integration](map-rich-controls-va-cccif.md).

Role required: admin

## Procedure

1.  Create the REST API.

    1.  Navigate to **All** &gt; **System web services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

<table id="table_syk_xhl_1mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your API. For example, `ACME Mobile App Chat Adapter`.

</td></tr><tr><td>

API ID

</td><td>

API identifier. For example, `acme_chat`.

</td></tr><tr><td>

Protection policy

</td><td>

The protection policy for the script.-   **Read-only**: Script is viewable only.
-   **Protected**: Users with password permissions can edit the script.


</td></tr><tr><td>

Application

</td><td>

The application containing the script record. **Global** is selected by default.

</td></tr><tr><td>

API namespace

</td><td>

The namespace the API belongs to. The value depends on the current application scope.

</td></tr></tbody>
</table>    4.  Click **Submit**.

    5.  Open the new record, navigate to **Related Links** and click **Enable Versioning**, and then click **OK**.

        Click **Update** to save your changes.

2.  Add a scripted REST resource to your new REST API.

    The scripted REST resource defines the scripted REST API definition that you created.

    1.  Open the REST API record you created, and then navigate to the **Resources** tab under **Related Links**.

    2.  Click **New**.

        Retrieve the payload from the request, and then write it to a hybrid queue.

    3.  On the form, fill in the fields.

<table id="table_dyh_d3l_1mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

API Definition

</td><td>

Name of the parent API.

</td></tr><tr><td>

Application

</td><td>

The application containing the script record.

</td></tr><tr><td>

Name

</td><td>

Name of your API REST Resource. For example, **ACME chat**.

</td></tr><tr><td>

API version

</td><td>

API version. For example, **v1**.This field displays only if you enabled versioning for the REST API.

</td></tr><tr><td>

Active

</td><td>

Option to make the REST resource active.

</td></tr><tr><td>

HTTP method

</td><td>

HTTP method, such as POST, GET, and so forth.

</td></tr><tr><td>

Relative path

</td><td>

Relative path to the resource.

</td></tr><tr><td>

Script

</td><td>

Script for the REST resource.

</td></tr><tr><td>

Protection policy

</td><td>

The protection policy for the script.-   **Read-only**: Script is viewable only.
-   **Protected**: Users with password permissions can edit the script.


</td></tr></tbody>
</table>        Example of a scripted REST resource:

        ```
        (function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
            var body = request.body;
            var queryParams = request.queryParams; // incoming content is application/x-www-form-urlencoded in this example    
            // get the provider application sys id. this can be done via a glide query using incoming data such as where the original message is being sent to. or it can be hard-coded such as this example.
            var providerAppId = "a5f8b75b7377001042281188caf6a73a";    
            // the time of receipt is recorded for analytics purposes
            var d = new Date();
            var logTime = d.getTime();    
            // add this message to the VA Server queue for processing
            var queued = sn_cs.VASystemObject.enqueueCustomAdapterMessage(providerAppId, JSON.stringify(queryParams), JSON.stringify(request.headers), logTime);
            if (queued == false) {
        	response.setError(new sn_ws_err.BadRequestError('Failed to process the request.'));
            }
        })(request, response);
        ​
        ```

3.  Set security and content negotiation for your scripted REST resource.

    Choose to set authentication and request formats. If your custom integration does not rely on authentication, you may want to remove it as follows.

    1.  In the new record for the Scripted REST Resource, navigate to the **Security** tab.

    2.  Clear **Requires authentication**.

    3.  Click the **Content Negotiation** tab, and then select **Override supported request formats**.

    4.  Click **Submit**.

4.  Set REST API rate limits to define the rate of incoming requests.

    1.  Navigate to **All** &gt; **System web services** &gt; **REST** &gt; **Rate Limit Rules**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

<table id="table_jk5_vdy_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the rate limit rule.

</td></tr><tr><td>

REST API

</td><td>

REST API that you created in an earlier step.

</td></tr><tr><td>

Version

</td><td>

Version of the REST API. Values listed depend on the selected REST API.

</td></tr><tr><td>

Resource

</td><td>

Resource for the specified Version. Values listed depend on the selected Version.

</td></tr><tr><td>

Active

</td><td>

Check box to indicate that the rate limit rule is active.Rate limit rules are activated by default as soon as you create them. You can deactivate rate limit rules to stop enforcing a rate limit or activate rate limit rules to resume enforcing a rate limit.

</td></tr><tr><td>

Request limit per hour

</td><td>

Maximum number of requests allowed per hour.**Note:** Whenever you update the value of this field, the ServiceNow AI Platform resets the count of requests to 0 and deletes all violations for the current hour.

</td></tr><tr><td>

Apply to

</td><td>

Users restricted by this rule. Select **All users**.

</td></tr></tbody>
</table>    4.  Click **Submit**.


## What to do next

[Create the action scripts for your custom chat integration](create-action-scripts-va-cccif.md)

**Parent Topic:**[Create a Virtual Agent conversational custom chat integration](create-adapter-for-virtual-agent.md)

