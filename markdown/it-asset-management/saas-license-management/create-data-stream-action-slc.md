---
title: Create a data stream action to get users
description: Create a data stream action to get a list of user subscriptions from the SaaS application.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a data stream action to get users

Create a data stream action to get a list of user subscriptions from the SaaS application.

## Before you begin

If you're using an existing ServiceNow® Integration Hub spoke, find out if it has a data stream action to get a list of users that you can use instead of creating one. For more information about data stream actions, see Data Stream actions.

Role required: flow\_designer

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Select **New**.

3.  Select **Data Stream**.

4.  On the form, fill in the fields.

<table id="table_j2c_w4j_rjb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your choice. For example, `Get Users`.

</td></tr><tr><td>

Accessible From

</td><td>

**All application scopes**.

</td></tr><tr><td>

Category

</td><td>

Leave this field empty.

</td></tr><tr><td>

Protection

</td><td>

**None**.

</td></tr><tr><td>

Application

</td><td>

Spoke app to integrate with the SaaS application. This spoke app can be an existing Integration Hub spoke or a new spoke that you created.

</td></tr><tr><td>

In-Flow Annotation

</td><td>

Leave this field empty.

</td></tr><tr><td>

Description

</td><td>

Description of your choice.

</td></tr></tbody>
</table>5.  Select **Submit**.

6.  If the API that you're working with requires user authentication for requests, select **Inputs** in the Action Outline and add inputs for authentication.

    Examples of common user authentication inputs are `admin user id` and `site name`. See the documentation for your chosen API to learn about the requirements for user authentication in your specific case. If the API requires an access token, a *Credential Value* variable is automatically created later. You don't need to add an access token as an input.

    When you use your completed data stream action in a subflow, you define what values to pass as these inputs.

7.  Select **Request** in the Action Outline.

8.  On the form, fill in the fields.

<table id="table_k2c_w4j_rjb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

How will you get data

</td><td>

Choose either **REST Step** or **SOAP step**.Your choice depends on the API for the SaaS application that you're integrating with.

</td></tr><tr><td>

Enable pagination

</td><td>

Selected.

</td></tr><tr><td>

Run a script before each request

</td><td>

Not selected.

</td></tr></tbody>
</table>9.  Select **Pagination Setup step** in the Action Outline.

10. Define pagination variables based on the query parameters used by the SaaS API.

    If you're using offset-based pagination, use the Limit/Offset pagination template to preload the pagination configuration.

    **Note:** The value of the reserved `getNextPage` variable determines whether to request another page of results. As long as the `getNextPage` variable is **true**, the action continues to send requests for the next page.

11. Write a `Pagination Variables` script to update the pagination variables.

    The script runs on each request. If you're using a pagination template, adjust the preloaded script as needed.

    The following image shows an example of the pagination setup step completion. This example is from the Get Users data stream action used in the Webex Download Subscriptions subflow.

    ![Pagination Setup step](../image/slc-pagination-webex.png)

    **Note:** Pagination variables only support the string data type. To perform math operations, you must convert the value to an integer, perform any required operations, then convert it back to a string.

12. Select **SOAP step** or **REST step** in the Action Outline to receive data.

    -   If you selected **SOAP step**, fill in the details.

<table id="table_azz_st4_rcc"><thead><tr><th>

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

This value is automatically populated when you select the connection alias. This value is set to the Connection URL from the HTTPs Connection record linked to the alias.

</td></tr><tr><td colspan="2">

Request Details

</td></tr><tr><td>

Build Envelope

</td><td>

**Manually**.

</td></tr><tr><td>

SOAP Action

</td><td>

API request to get a list of all users. See the documentation for your chosen API to select the appropriate request.

</td></tr><tr><td>

SOAP Envelope

</td><td>

XML request message to get a list of all users. See the documentation for your chosen API to learn how to write an XML request message. In general, the header should have your input variables for user authentication as well as the *Credential Value* variable as the access token. The body should include the request to get a list of all users and your variables from the pagination setup step. **Note:** For an example of a SOAP envelope, see the Get Users data stream action used in the Webex Download Subscriptions subflow.

</td></tr></tbody>
</table>    -   If you selected **REST step**, fill in the details.

        |Field|Value|
        |-----|-----|
        |Connection Details|
        |Connection|**Use Connection Alias**.|
        |Connection Alias|Connection alias that you created when you created the integration profile. If you have not yet created an integration profile, follow the steps to [create a custom integration profile with a connection alias.](create-integration-custom.md)|
        |Base URL|This value is automatically populated when you select the connection alias. It's set to the Connection URL from the HTTP\(s\) Connection record linked to the alias.|
        |Request Details|
        |Build Request|**Manually**.|
        |Resource Path|Path to the resource. This value gets appended to the Base URL. See the documentation for the API that you're working with to learn how to construct the resource path.|
        |HTTP Method|**GET**.|
        |Query Parameters|Add parameters for pagination. Set the values as the variables that you created in the pagination setup step.|

        The following image shows a completed example of the REST step. This example is from the Get Jira Users data stream action used in the Jira Download Subscriptions subflow.

        ![REST step](../image/slc-rest-step.png)

13. Select **Parsing** in the Action Outline.

14. On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |How will you identify each record|**JSON/XML Splitter**|
    |How will you parse each item into an object|**Script Parser**|

15. Select **Splitter step** in the Action Outline.

16. On the form, fill in the fields.

<table id="table_r2c_w4j_rjb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Source Format

</td><td>

Select **XML** or **JSON**, depending on the format returned by the API response.

</td></tr><tr><td>

Item Path

</td><td>

Absolute path to a user element in the response message. See the documentation for the API that you're working with for information about the format of the response message.-   Example XML item path: `/message/body/user`
-   Example JSON item path: `$.data.user`


</td></tr></tbody>
</table>17. Select **Outputs** in the Action Outline.

18. Select **Create Output** and edit the variable as shown.

    |Label|Name|Type|Required|
    |-----|----|----|--------|
    |targetObject|targetObject|Object|No|

19. Add child items for *targetObject* based on the user child elements returned in the response message.

    For example, an XML response might look like this.

    ```
    <message>​
      <body>​
        <user>
          <userID>​12345</userID>​
          ​<email>​email@email.com</email>​
          <firstName>​Jane</firstName>​
          <lastName>​Doe</lastName>​
          <lastLoginTime>​08/13/2019 20:08:16</lastLoginTime>​
          <active>​TRUE</active>​
        </user>​
        <user>
          ...
        </user>
      </body>​
    </message>
    ```

    For this response, add the child items as shown.

    |Label|Name|Type|Required|
    |-----|----|----|--------|
    |userID|userID|String|No|
    |email|email|String|No|
    |firstName|firstName|String|No|
    |lastName|lastName|String|No|
    |lastLoginTime|lastLoginTime|String|No|
    |active|active|True/False|No|

20. Select **Script Parser step** in the Action Outline.

21. Create a *targetObject* output object for each user element in the response and then map each user child element to a *targetObject* child item.

    The parser script is executed for each user element.

    **Note:** These examples show the types of elements that are generally contained in a response to a get users request. Don’t directly copy these scripts. Use element names from the documentation for the API that you're working with.

    Example script that parses an XML response.

    ```
    (function parse(inputs, outputs) {
        var xmlDoc = new XMLDocument(inputs.sourceItem, false);
        outputs.targetObject.userID = xmlDoc.getNodeText('/user/userID');
        outputs.targetObject.email = xmlDoc.getNodeText('/user/email');
        outputs.targetObject.firstName = xmlDoc.getNodeText('/user/firstName');
        outputs.targetObject.lastName = xmlDoc.getNodeText('/user/lastName');
        outputs.targetObject.lastLoginTime = xmlDoc.getNodeText('/user/lastLoginTime');
        outputs.targetObject.active = xmlDoc.getNodeText('/user/active');
    })(inputs, outputs)
    ```

    Example script that parses a JSON response.

    ```
    (function parse(inputs, outputs) {
        var record = JSON.parse(inputs.sourceItem);
        outputs.targetObject.userID = record.userID;
        outputs.targetObject.email = record.email;
        outputs.targetObject.firstName = record.firstName;
        outputs.targetObject.lastName = record.lastName;
        outputs.targetObject.lastLoginTime = record.lastLoginTime;
        outputs.targetObject.active = record.active;
    })(inputs, outputs)
    ```

22. To test your data stream action, select **Test**.

    1.  View the test results and system logs for details about any errors.

        To view system logs, navigate to **System Logs** &gt; **System Log** &gt; **All**.

    2.  If your data stream action has errors, make sure that you're using the correct endpoints and that the API requests and responses are structured as expected.

23. After verifying that the data stream action is working as expected, select **Publish**.


## What to do next

[Create a subflow to get users](create-subflow-get-users.md#).

