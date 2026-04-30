---
title: Create a Data Stream action
description: Create a reusable action to process a stream of response data within a flow.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Data Stream actions and pagination, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a Data Stream action

Create a reusable action to process a stream of response data within a flow.

## Before you begin

-   Set up an application in Guided Application Creator to store Workflow Studio content.
-   Disable any conflicting business rules or workflows before creating an action.
-   Role required: action\_designer or admin

## About this task

Creating a custom application to contain your Workflow Studio content enables you to [deploy](https://www.servicenow.com/docs/access?context=c_SharingApplications&version=zurich&pubname=zurich-application-development&ft:locale=en-US) it using the application repository or the ServiceNow Store.

**Note:** Clearing an option in a configuration page removes the step from the Data Stream outline and deletes all data associated with the step.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click the **Actions** tab and select **Data Stream**.

3.  Fill in the Action Properties and click **Submit**.

    |Field|Description|
    |-----|-----------|
    |Action name|Enter a unique name for your data stream action.|
    |Description|Description of the data stream action.|
    |Application|Application scope of the data stream action.|
    |Domain|Domain scope of the data stream action. For more information about domain separation, see [Domain separation explained](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).|
    |**Additional properties**|
    |Accessible From|Accessible from all application scoped or only within the specified application scope.|
    |Category|Defined category within the application scope for an action. Beginning with the Xanadu release, you can create a custom category to organize your data stream actions.|
    |Protection|Select whether the data stream action is read-only. You can only select a value when you create the data stream action in an application scope you own. The default value is None.|
    |Action annotation|Help text that appears under the data stream action title in Workflow Studio to help data stream action authors understand what the data stream action does when used in a flow.|

    An empty Data Stream action opens.

4.  Define action inputs to make data available to the action steps.

    1.  Select **+ Create Input** and complete the fields.

        Inputs are represented as data pills in the right-hand pane.

    For more information about action inputs, see [Workflow Studio - Building custom actions](https://www.servicenow.com/docs/access?context=actions&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

5.  Click **Action Preprocessing** in the Data Stream outline and configure the desired options.

    1.  Select **Retrieve connection info** to add the Get Connection Info step as the first step in the action preprocessing.

        The Get Connection Info step enables you to retrieve connection and credential details to use in your action. For more information, see [Get Connection Info step](https://www.servicenow.com/docs/access?context=get-connection-info-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

    2.  Select **Enable preprocessing script** to run a preprocessing script before the action sends the initial API request. For example, validate action inputs or set default values. Preprocessing executes once per action, before the first API request.

        Selecting this option adds a script step to the Data Stream action. For more information, see [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

        **Important:** Data Stream actions require a constant connection to the response stream. They do not support preprocessing scripts that pause the action to call a MID Server or pause the action to wait for a condition or duration. A preprocessing script that pauses the action for any reason returns an error message.

6.  Click **Request** in the Data Stream outline and configure the desired options.

    1.  In the **How will you get data** field, select **REST Step**, **SOAP Step**, or **JDBC Step** to add the associated step to the Data Stream action.

        For more information, see [REST step](../../flow-designer/reference/rest-request-action-designer.md), [SOAP step](../../flow-designer/reference/soap-step-action-designer.md), and [JDBC step](../../flow-designer/reference/jdbc-step.md) .

        This section can run on either the MID Server or the instance. The environment is determined by the **Use MID server** field in the associated Connection \[sys\_connection\] record.

        **Note:**

        -   If you are using the JDBC step, you must test it. Upon successful execution, you can use the result to create the step output and data stream action output.
        -   If you are using the REST step or SOAP step, you must manually create the data stream action output.
    2.  Select **Enable pagination** to request results in batches. Once one page of data is processed, the Data Stream action runs the request section again to return the next set of results. This option adds a Pagination Setup step to the Data Stream outline.

        **Note:** For a JDBC step, pagination is not applicable. Each page can retrieve up to 1 GB data and one request can retrieve up to 8 GB data.

    3.  Select **Run a script before each request** to run a script before every request for the next page when calling a paginated API.

        For example, write a script to transform variable data types from the initial response before sending a request for the next page.

        Selecting this option adds a script step to the Data Stream action. For more information, see [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

        **Note:** For a JDBC step, this is not applicable.

        This section can run on either the MID Server or the instance. The environment is determined by the script step's **Required Runtime** field.

        **Important:** Avoid shifting the execution environment between the instance and the MID Server multiple times. For example, you might configure the Request Script step to run on the MID Server, but the REST step to run on the instance. In this case, the system shifts environments between the instance and MID Server for every page of data, which may degrade performance.

7.  If pagination is enabled, configure the Pagination Setup step.

    Configure the Pagination Setup step manually, or select a pre-built template to apply common configurations. For example, apply the **Limit / Offset** template to specify the number of items you want returned per page \(limit\), and the starting number for the first item \(offset\). After applying a template, update the values to ensure that the configuration complies with the API's requirements.

    1.  Create pagination variables.

        For example, if the third-party API takes a `limit` parameter in the request, create the `limit` variable and set the initial value to limit the number of results per page. The initial value is only used in the first request. `getNextPage` is a reserved, read-only variable. As long as the `getNextPage` variable is true and the previous page contains data, the action continues to send requests for the next page.

    2.  In the **Next Value From** field, define how pagination variables receive a value for subsequent requests.

        Choose from:

        -   **Script**: Write a Pagination Variables Script to define how variables are populated. Pagination variables only support the string data type. To perform math operations, you must convert the value to an integer, perform any required operations, then convert it back to a string.
        -   **Response Body**: Use a value in the response from the previous request to populate the variable. If the response is JSON format, set **Extract value using** to **JSONPath Expression** and provide the path to the value in the **Expression** field. If the response is XML format, set **Extract value using** to **XPath Expression** and provide the path to the value.
    In this example, the `getNextPage` variable is true until the `nextOffset` variable reaches the total count value returned in the API response header. As long as the `getNextPage` variable is true and the previous page contains data, the action continues to send requests for the next page. This example includes a common limit/offset pagination configuration. The third-party APIs that your Data Stream action interacts with may use a page token or other method.

    ![Pagination setup with a pagination variables script.](../images/pagination-setup.png)

    **Important:** Avoid infinite loops in pagination requests by creating a condition that sets the `getNextPage` variable to false. Cancel any long-running flows. Always test Data Stream actions before using them in production.

8.  Click **Parsing** in the Data Stream outline and configure the desired options.

    **Note:** For a JDBC step, this is not applicable.

    1.  In the **How will you identify each record** field, select **JSON/XML Splitter** to add a Splitter step to the Data Stream outline.

    2.  In the **How will you parse each item into an object** field, select **Script Parser** to add a Script Parser step to the Data Stream outline.

9.  Configure the Splitter step.

    This step identifies the parent node in the response stream to map to a complex object. For example, identify a user element in an XML payload to create a complex object for each user in the response stream.

    **Note:** For a JDBC step, this is not applicable.

    1.  In the **Source Format** field, select the format returned by the Request section.

        -   **JSON**: Identifies objects from a stream of JSON data. Use a JSONPath expression to identify a JSON array containing repeated data.
        -   **XML**: Identify objects from a stream of XML data. Use an XPath expression to identify an XML element containing repeated data.
    2.  In the **Item Path** field, define the absolute path to the item in the data stream you want to map to an object.

        -   **JSON**

            Identify the absolute path to an array of objects as a JSONPath expression. For example, use `$.result` to separate each item in a JSON `result` array into a `result` object.

            **Note:** If you select an array at the root node of a JSON data stream, the system displays the absolute path as `$.*` in execution details and error messages.

        -   **XML**

            Identify the absolute path to a repeating data object as a XPath expression. For example, use `/result` to separate each instance of a `result` XML element into a `result` object.

            **Note:** The Splitter step ignores XML namespaces.​

        For example, suppose the REST Step returns a stream of JSON data. The item path `$.response.result.companies` returns each item in the `companies` array.

        ```
        {​
          "response": {​
            "result": {​
              "companies": [​
                {​
                  "name": "company1"​
                },​
                {​
                  "name": "company2"​
                },​
                {​
                  "name": "company3"​
                }​
              ],​
              "metadata": {​
                "token": 1558666526​
              }​
            }​
          }​
        } 
        ```

        For example, suppose the REST Step returns a stream of XML data. The item path `/response/result/companies​/company` returns each `company` element from the XML data.

        ```
        <response>​
          <result>​
            <companies>​
              <company>​
                <!-- company 1 info -->​
              </company>​
              <company>​
                <!-- company 2 info -->​
              </company>​
              <company>​
                <!-- company 3 info -->​
              </company>​
              <company>​
                <!-- company 4 info -->​
              </company>​
              <batch>10645C53D4BED73YQ</batch> ​
            </companies>​
            <metadata>​
              <timestamp>1558666526</timestamp>​
            </metadata>​
          </result>​
        </response>
        ```

10. In the Script Parser step, use JavaScript and ServiceNow APIs to map items in the response stream to a complex object output represented by the `targetObject` global object.

    For example, map incident record elements identified in the splitter step to a complex object containing incident fields. If the data stream includes siblings to the item identified in the splitter step that you do not want mapped to a complex object, include conditions to exclude those items.

    **Note:** For a JDBC step, this is not applicable.

    You can access outputs from previous steps in your data stream action using the fd\_data object, excluding:

    -   REST or SOAP step Response Body, Stream, or Error Message outputs.
    -   Splitter step outputs.
    An example script that parses a JSON response.

    ```
    (function parse(inputs, outputs) {
        var record = JSON.parse(inputs.sourceItem);
        outputs.targetObject.id=record.number;
        outputs.targetObject.name=record.short_description;
    })(inputs, outputs)
    ```

    An example script that parses an XML response.

    ```
    (function parse(inputs, outputs) {
        var xmlDoc = new XMLDocument(inputs.sourceItem, false);
        outputs.targetObject.id = xmlDoc.getNodeText("/result/number");
        outputs.targetObject.name = xmlDoc.getNodeText("/result/short_description");
    })(inputs, outputs)
    ```

11. If you selected the JDBC step, click **Transform**.

    After successfully testing the JDBC step, click **Use Result** to create the step output and data stream action output. You can use this result or customize it using the transform script.

    1.  Select the **Enable Transform Script** check box to transform and customize the default data stream output.

12. Create a complex object output.

    **Note:** For a JDBC step, this is not applicable.

    1.  Select **Outputs** in the Action Outline and click **+** to create an output.

    2.  Update the **Label** field to represent the object.

        For example, if the action parses a stream of company records, add the **Company** label.

    3.  Update the **Type** field to **Object**.

        This is the complex object output represented by the `targetObject` global object in the Script Parser step.

    4.  Add child fields to the complex object using the **+** icon.

    5.  Make the name of each child field more user-friendly so that you can meaningfully refer to it in script.

        The value in the **Name** field is the internal name used in the Script Parser step. For example, to refer to the City output in the Script Parser step, you would use `outputs.targetObject.city`.

        ![Default values for child items in the complex object output.](../images/ds-output-label.png)

        **Warning:** After saving the Data Stream action, you cannot change values in the **Name** field.

13. Click **Save**.

    Workflow Studio saves a draft of the action.


## What to do next

[Test a Data Stream action](test-data-stream-action.md).

**Parent Topic:**[Data Stream actions and pagination](../concept/data-stream-actions.md)

