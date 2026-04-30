---
title: Create a data stream action to get user activity
description: Create a data stream action to get user activity from a SaaS application.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a data stream action to get user activity

Create a data stream action to get user activity from a SaaS application.

## Before you begin

If you're using an existing ServiceNow® Integration Hub spoke, find out if it has a data stream action to get user activity that you can use instead of creating one.

For more information about data stream actions, see [Data Stream actions](https://www.servicenow.com/docs/access?context=data-stream-actions&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

Role required: flow\_designer or admin

## About this task

Monitor user activity to find software subscriptions that your company is paying for but are not being used. You can reclaim these unused subscriptions to reduce your company's software expenses.

Before creating the data stream action, decide how you want to define meaningful user activity. Meaningful activity can be a combination of user actions. Create a separate data stream action for each user activity metric. For example, the base system Webex Meetings integration defines meaningful activity as hosting a meeting. It uses one data stream action to get the dates of the most recently hosted meetings for all users. If you also wanted the Webex Meetings integration to include logging in as meaningful activity, you would create a second data stream action to get the most recent login times for all users.

Your data stream action to get users may return a user activity metric such as last login time. In this case, you don't need to create a data stream action to get user activity or a subflow to get user activity unless you want to define additional user activity metrics. Make sure that your subflow to get users sets this user activity metric as the **Last activity** input in the **Upsert User Subscription** action.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **New** and then select **Data Stream**.

3.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|Name of your choice. For example, `Get User Activity`.|
    |Accessible From|Select **All application scopes**.|
    |Category|Leave this field empty.|
    |Protection|Select **None**.|
    |Application|Spoke app to integrate with the SaaS application. This spoke app can be an existing Integration Hub spoke or a new spoke that you created.|
    |In-Flow Annotation|Leave this field empty.|
    |Description|Description of your choice.|

4.  Click **Submit**.

5.  In the Inputs section of the Action Outline, click **Create Input**.

6.  Add a look back time input.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |Look back time|look\_back\_time|Date/Time|Yes|

7.  If the API that you're working with requires user authentication for requests, add inputs for authentication.

    Examples of common user authentication inputs are admin user id and site name. See the documentation for your chosen API to learn about the requirements for user authentication in your specific case. If the API requires an access token, a *Credential Value* variable is automatically created later. You don't need to add an access token as an input.

    When you use your completed data stream action in a subflow, you define what values to pass as these inputs.

8.  Click **Request** in the Action Outline.

9.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |How will you get data|Choose either **REST Step** or **SOAP step**. Your choice depends on the API for the SaaS application that you're integrating with.|
    |Enable pagination|Selected.|
    |Run a script before each request|Not selected.|

10. Click **Pagination Setup step** in the Action Outline.

11. Define pagination variables based on the query parameters used by the SaaS API.

    If you're using offset-based pagination, use the Limit/Offset pagination template to preload the pagination configuration.

    **Note:** The value of the reserved `getNextPage` variable determines whether to request another page of results. As long as the `getNextPage` variable is **true**, the action continues to send requests for the next page.

12. Write a `Pagination Variables` script to update the pagination variables.

    The script runs on each request. If you're using a pagination template, adjust the preloaded script as needed.

    The following image shows a completed example of the pagination setup step. This example is from the Get Users data stream action used in the Webex Download Subscriptions subflow.

    ![Pagination Setup step](../image/slc-pagination-webex.png)

    **Note:** Pagination variables only support the string data type. To perform math operations, convert the value to an integer, perform any required operations, then convert it back to a string.

13. Click **SOAP step** or **REST step** in the Action Outline depending on the option that you selected for how you will get data.

14. If you selected **SOAP**, fill in the details.

<table id="table_o2c_w4j_rjb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td colspan="2">

Connection Details

</td></tr><tr><td>

Connection

</td><td>

**Use Connection Alias**.

</td></tr><tr><td>

Connection Alias

</td><td>

Connection alias that you created when you created the integration profile. If you have not yet created an integration profile, follow the steps to [create a custom integration profile with a connection alias.](create-integration-custom.md)

</td></tr><tr><td>

Endpoint

</td><td>

This value is automatically populated when you select the connection alias. It's set to the Connection URL from the HTTP\(s\) Connection record linked to the alias.

</td></tr><tr><td colspan="2">

Request Details

</td></tr><tr><td>

Build Envelope

</td><td>

**Manually**.

</td></tr><tr><td>

SOAP Action

</td><td>

API request to get a list of meaningful user activity. For example, the base system Webex Meetings integration defines meaningful user activity as hosting a meeting so that it uses the `LstsummaryMeeting` request to get a list of all meetings. See the documentation for your chosen API to select the appropriate request.

</td></tr><tr><td>

SOAP Envelope

</td><td>

XML request message to get a list of all users. See the documentation for your chosen API to learn how to write an XML request message. In general, the header should have your input variables for user authentication as well as the *Credential Value* variable as the access token. The body should include the request to get a list of meaningful user activities, a start date set as the **Look back time** input, and your variables from the pagination setup step. **Note:** For an example of a SOAP envelope, see the Get User Activity data stream action used in the Webex Update User Activity subflow.

</td></tr></tbody>
</table>15. If you selected **REST**, fill in the details.

<table id="table_p2c_w4j_rjb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td colspan="2">

Connection Details

</td></tr><tr><td>

Connection

</td><td>

**Use Connection Alias**.

</td></tr><tr><td>

Connection Alias

</td><td>

Connection alias that you created when you created the integration profile. If you have not yet created an integration profile, follow the steps to [create a custom integration profile with a connection alias.](create-integration-custom.md)

</td></tr><tr><td>

Base URL

</td><td>

This value is automatically populated when you select the connection alias. It's set to the Connection URL from the HTTP\(s\) Connection record linked to the alias.

</td></tr><tr><td colspan="2">

Request Details

</td></tr><tr><td>

Build Request

</td><td>

**Manually**.

</td></tr><tr><td>

Resource Path

</td><td>

Path to the resource. This value gets appended to the Base URL. See the documentation for the API that you're working with to learn how to construct the resource path.

</td></tr><tr><td>

HTTP Method

</td><td>

**GET**.

</td></tr><tr><td>

Query Parameters

</td><td>

Add parameters for pagination. Set the values as the variables that you created in the Pagination Setup step.Add another parameter for the start date so that the request returns results from the start date to the current date. Set the value as the **Look back time** input.

**Note:** Make sure the **Look back time** input date/time variable is correctly formatted for the API that you're working with. If you need to reformat or convert to another data type such as a string, you can do this in the action preprocessing script step.

</td></tr></tbody>
</table>    The following image shows a completed example of the REST step. This example is from the Get Audit Log data stream action used in the Jira Update User Activity subflow.

    ![REST step](../image/slc-rest-step-2.png)

16. Click **Parsing** in the Action Outline.

17. On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |How will you identify each record|**JSON/XML Splitter**|
    |How will you parse each item into an object|**Script Parser**|

18. Click **Splitter step** in the Action Outline.

19. On the form, fill in the fields.

<table id="table_r2c_w4j_rjb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Source Format

</td><td>

Select **XML** or **JSON** depending on the format returned by the API response.

</td></tr><tr><td>

Item Path

</td><td>

Absolute path to a meaningful activity element in the response message. See the documentation for the API that you're working with for information about the format of the response message.-   Example XML item path: `/message/body/meeting`
-   Example JSON item path: `$.data.meeting`


</td></tr></tbody>
</table>20. Click **Outputs** in the Action Outline.

21. Click **Create Output** and edit the variable as shown.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |targetObject|targetObject|Object|No|

22. Add child items for *targetObject* to store the user email and the date of meaningful activity.

    For example, an XML response might look like this.

    ```
    <message>​
      <body>​
        <meeting>
          <meetingID>​12345</meetingID>​
          <startDate>​08/13/2019 20:08:16</startDate>​
          <hostEmail>​email@email.com</hostEmail>​
        </meeting>​
        <meeting>
          ...
        </meeting>
      </body>​
    </message>
    ```

    For this response, add the child items as shown.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |email|email|String|No|
    |last\_activity|last\_activity|String|No|

23. In the Action Outline, click **Script Parser step**.

24. Create a *targetObject* output object for each meaningful activity element in the response and then map each the activity date and user email to the *targetObject* child items.

    The parser script is executed for each user element.

    **Note:** These examples show the types of elements that could be contained in a response. Don't directly copy these scripts. Use element names from the documentation for the API that you're working with.

    Example script that parses an XML response.

    ```
    (function parse(inputs, outputs) {
        var xmlDoc = new XMLDocument(inputs.sourceItem, false);
        outputs.targetObject.email = xmlDoc.getNodeText('/meeting/hostEmail');
        outputs.targetObject.last_activity = xmlDoc.getNodeText('/meeting/startDate');
    })(inputs, outputs)
    ```

    Example script that parses a JSON response.

    ```
    (function parse(inputs, outputs) {
        var record = JSON.parse(inputs.sourceItem);
        outputs.targetObject.email = record.hostEmail;
        outputs.targetObject.last_activity = record.startDate;
    })(inputs, outputs)
    ```

25. To test your data stream action, click **Test**.

    1.  View the test results and system logs for details about any errors.

        To view system logs, navigate to **System Logs** &gt; **System Log** &gt; **All**.

    2.  If your data stream action has errors, make sure that you're using the correct endpoints and that the API requests and responses are structured as expected.

26. After verifying that the data stream action is working as expected, click **Publish**.


