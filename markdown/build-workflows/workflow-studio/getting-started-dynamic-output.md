---
title: Get started with dynamic outputs
description: Create a sample action that builds dynamic outputs for use in a flow.Create the aliases, connections, and credentials that REST steps will use to connect to your local instance.Create a data gathering action to look up a table schema and convert into a JSON object.Create a data gathering action to generate an array of objects from a list of records.Create a sample action to dynamically generate two action outputs, Record and Records which refresh dynamically when the value for the Table input changes.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 15
breadcrumb: [Dynamic outputs, Create an action in Workflow Studio, Building actions, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Get started with dynamic outputs

Create a sample action that builds dynamic outputs for use in a flow.

## Before you begin

Role required: action\_designer or admin

## Procedure

1.  [Create connection and credential records for dynamic outputs](getting-started-dynamic-output.md#)

    This connection &amp; credential alias will provide the base URL and user account needed to configure the REST steps of your data gathering actions.

2.  [Create a data gathering action to get a record schema](getting-started-dynamic-output.md#)

    This data gathering action will convert a single record into a JSON object for a record dynamic output.

3.  [Create a data gathering action to get an array of records schema](getting-started-dynamic-output.md#)

    This data gathering action will convert a list of records record into JSON array of objects for a records dynamic output.

4.  [Create a custom action to test dynamic outputs](getting-started-dynamic-output.md#)

    This custom action illustrates two types of dynamic output data. One dynamic output generates an object for a single record. Another dynamic output generates an array of objects for a list of records.


**Parent Topic:**[Dynamic outputs](../concept/dynamic-outputs.md)

**Related topics**  


[Create a data gathering action for a dynamic object](create-data-gathering-action-dynamic-object.md)

[Dynamic output configuration options](../reference/dynamic-output-options.md)

## Create connection and credential records for dynamic outputs

Create the aliases, connections, and credentials that REST steps will use to connect to your local instance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**, select **Basic Auth Credentials**, and enter these field values.

    1.  For **Name**, enter `Local Admin`.

    2.  For **User name**, enter a user account with access to Flow Designer and the REST API.

        For example, enter `admin`.

    3.  For **Password**, enter the account password.

3.  Select **Submit** to create the credential record.

4.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

5.  Select **New** and enter these fields values.

    1.  For **Name**, enter Local Instance.

    2.  Accept the default value of HTTP for the **Connection type**.

    3.  Select **Submit** to create the Connection &amp; Credential Alias record.

6.  Select the alias you created.

    For example, select **Local Instance**.

7.  From the Connections related list, select **New**, and enter these field values.

    1.  For **Name**, enter `My Instance`.

    2.  For Credential, select the basic authentication credential record you created.

        For example, select the **Local Admin** credential.

    3.  For Connection URL, enter the base URL for your instance including the forward slash at the end.

        Include the URL prefix https:// and add a slash character at the end of the URL.

        For example, `https://example.service-now.com/`.

    4.  Select **Submit** to create the HTTP\(s\) Connection record.


## Create a data gathering action to get a record schema

Create a data gathering action to look up a table schema and convert into a JSON object.

### Before you begin

Role required: action\_designer or admin

### About this task

In this task, you create a data gathering action that collects the schema for a record on your instance. The goal is to create a complex object for use as a dynamic output. This data gathering action consists of the following:

-   A REST step to gather table schema data for a selected table. The REST step Response Body is in JSON format.
-   A script step to transform the REST step's JSON Response Body into a dynamic object. The dynamic object consists of JSON name-value pairs, where there is an entry for each field in the table.
-   An output variable named `output` of type JSON to store the dynamic object.

**Note:** This task re-creates the demo actions that are installed when you [Request an Integration Hub plugin](https://www.servicenow.com/docs/access?context=request-integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) for your instance.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Actions**.

3.  Select **New** and select **New Action**.

    1.  On the Action Properties screen, in the **Name** field, enter `Get ServiceNow Object Schema (Dynamic)`.

    2.  Select **Submit**.

4.  In the Action Outline, select **Inputs**.

    1.  In the Action Input header, select **Create Input**.

    2.  In the **Label** and **Name** fields, enter `Table`.

    3.  In the **Type** field, select `String`.

    4.  To make this input required, toggle the **Mandatory** slider so that it is active.

5.  In the Action Outline, select the add a new step icon \(![Add a new step icon](../images/add-new-step-icon.png)\) under Inputs and select **REST Step**.

6.  Under the REST step header, fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Connection|Leave the **Use Connection Alias** option selected.|
    |Connection Alias|select the create new record icon \(![Create new record icon](../images/create-new-record-icon.png)\) to create a new [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), or use an existing connection for your instance. The **Credential** for the HTTP\(s\) connection must use [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US). Additionally, the **Connection URL** must be the base URL for your instance, including the forward slash at the end. For more information on connections and credentials, see [Getting started with connections](https://www.servicenow.com/docs/access?context=connection-information&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) and [Getting started with credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).|
    |Build Request|Leave the **Manually** option selected.|
    |Resource Path|Enter `api/now/processflow/table/` and then select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\). Select **Inputs** &gt; **Table**. Next, enter `/schema`.|
    |HTTP Method|Enter `GET`|
    |Query Parameters|select the plus icon \(![Plus icon](../../../build/app-engine-studio/image/plus-icon.png) to add a new query parameter. Then, in the **Name** field, enter `get_choices` and `true` in the **Value** field.|

7.  In the Action Outline, select the add a new step icon \(![Add a new step icon](../images/add-new-step-icon.png)\) under your REST step and select the **Script** step.

    1.  In the Input Variables section, select **Create Variable**.

    2.  In the **Name** field, enter `payload`.

    3.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **REST Step** &gt; **Response Body**.

    4.  In the **Script** field, enter the following code.

        ```
        
        (function execute(inputs, outputs) {
          var payload = JSON.parse(inputs.payload);
          
          var columns = payload.result.data.columns;
          var schema = columns.map(function(column) {
            var value = {
              label: column.label,
              name: column.name,
              type: getCOType(column.definition.base_type),
            };
            if (column.definition.type === 'choice') {
              value.type = 'choice';
              value.choices = column.definition.choices;
            } 
            if (column.definition.base_type === 'GUID') {
              value.children = [
                { label: 'Link', name: 'link', type: 'string' },
                { label: 'Value', name: 'value', type: 'string' },
              ];
            }
            return value;
          });
          outputs.schema = { 
            data: {
              type: 'object',
              children: schema,
            },
          };
          
          function getCOType(type) {
            if (type === 'GUID') return 'reference';
            return type;
          }
        })(inputs, outputs);
        ```

    5.  In the Output Variables section, select **Create Variable**.

    6.  In the **Label** and **Name** fields, enter `schema`.

    7.  In the **Type** field, select `JSON`.

8.  In the Action Outline, select **Outputs**.

    1.  In the Action Output header, select **Create Output**.

    2.  In the **Label** and **Name** fields, enter `output`.

    3.  In the **Type** field, select `JSON`.

    4.  In the Action Output header, select **Exit Edit Mode**.

    5.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Script Step** &gt; **schema**.

9.  In the Action header, select **Save** and then select **Test** to [test the action](test-action.md).

    1.  On the Test Action screen, enter `incident` for the **Table** input.

    2.  Select **Run Test**.

    3.  Check the action's execution details.

    Your data gathering action runs successfully if the runtime value for `fields` is a complex object in a format that is similar to the following abbreviated example.

    ```
    {
           "data": {
               "type": "object",
               "children": [
                   {
                       "name": "active",
                       "label": "Active",
                       "type": "boolean"
                   },
                   {
                       "name": "activity_due",
                       "label": "Activity due",
                       "type": "datetime"
                   }, ...
    ```

10. In the Action header, select **Publish** to make the **Get ServiceNow Object Schema \(Dynamic\)** action available to other flows and actions within the Global scope.


## Create a data gathering action to get an array of records schema

Create a data gathering action to generate an array of objects from a list of records.

### Before you begin

Role required: action\_designer or admin

### About this task

In this task, you create a data gathering action that collects the schema for a record on your instance. The goal is to create a complex object for use as a dynamic output. This data gathering action consists of the following:

-   A REST step to gather table schema data for a selected table. The REST step Response Body is in JSON format.
-   A script step to transform the REST step's JSON Response Body into a dynamic object. The dynamic object consists of a JSON array of objects, where each source record is converted into one object of the array.
-   An output variable named `output` of type JSON to store the dynamic object.

**Note:** This task re-creates the demo actions that are installed when you [Request an Integration Hub plugin](https://www.servicenow.com/docs/access?context=request-integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) for your instance.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Actions**.

3.  Select **New** and select **New Action**.

    1.  On the Action Properties screen, in the **Name** field, enter `Get ServiceNow Array.Object Schema (Dynamic)`.

    2.  Select **Submit**.

4.  In the Action Outline, select **Inputs**.

    1.  In the Action Input header, select **Create Input**.

    2.  In the **Label** and **Name** fields, enter `Table`.

    3.  In the **Type** field, select `String`.

    4.  To make the input required, toggle the **Mandatory** slider so that it is active.

5.  In the Action Outline, select the add a new step icon \(![New step icon](../images/add-new-step-icon.png)\) under Inputs and select the **REST** step.

6.  Under the REST step header, fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Connection|Leave **Use Connection Alias** selected.|
    |Connection Alias|select the create new record icon \(![Create new record icon](../images/create-new-record-icon.png)\) to create a new [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), or use an existing connection for your instance. The **Credential** for the HTTP\(s\) connection must use [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US). Additionally, the **Connection URL** must be the base URL for your instance, including the forward slash at the end.|
    |Build Request|Leave **Manually** selected.|
    |Resource Path|Enter `api/now/processflow/table/` and then select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\). Select **Inputs** &gt; **Table**. Finally, enter `/schema`|
    |HTTP Method|Enter `GET`|
    |Query Parameters|select the plus icon \(![Plus icon](../../../build/app-engine-studio/image/plus-icon.png) to add a new query parameter. Then, in the **Name** field, enter `get_choices` and `true`in the **Value** field.|

7.  In the Action Outline, select the **Add a new step**\(![New step icon](../images/add-new-step-icon.png)\) icon under your REST step and select the **Script** step.

    1.  In the Input Variables section, select **Create Variable**.

    2.  In the **Name** field, enter `payload`.

    3.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **REST Step** &gt; **Response Body**.

    4.  In the **Script** field, enter the following code.

        ```
        
        (function execute(inputs, outputs) {
          var payload = JSON.parse(inputs.payload);
          
          var columns = payload.result.data.columns;
          var schema = columns.map(function(column) {
            var value = {
              label: column.label,
              name: column.name,
              type: getCOType(column.definition.base_type),
            };
            if (column.definition.type === 'choice') {
              value.type = 'choice';
              value.choices = column.definition.choices;
            }
            return value;
          });
          outputs.schema = { 
            data: {
              type: 'array.object',
              attributes: {
                child_type: 'object',
              },
              children: schema,
            },
          };
          
          function getCOType(type) {
            if (type === 'GUID') return 'string';
            return type;
          }
        })(inputs, outputs);
        ```

    5.  In the Output Variables section, select **Create Variable**.

    6.  In the **Label** and **Name** fields, enter `schema`.

    7.  In the **Type** field, select `JSON`.

8.  In the Action Outline, select **Outputs**.

    1.  On the Action Output header, select **Create Output**.

    2.  Enter `output` in the **Label** field and **Name** field.

    3.  Select `JSON` for the **Type** field.

    4.  Select **Exit Edit Mode**.

    5.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Script Step** &gt; **schema**.

9.  In the Action header, select **Save** and then select **Test** to [test the action](test-action.md).

    1.  On the Test Action screen, in the **Table** field, enter `incident`.

    2.  Select **Run Test**.

    3.  Check the action's execution details.

        Your data gathering action runs successfully if the runtime value for `fields` output is a complex object that contains an array of key-value pairs for `label`, `name`, and `value` as shown in the following abbreviated example.

        ```
        {
               "data": {
                   "type": "array.object",
                   "children": [
                       {
                           "name": "active",
                           "label": "Active",
                           "type": "boolean"
                       },
                       {
                           "name": "activity_due",
                           "label": "Activity due",
                           "type": "datetime"
                       }, ...
        
        ```

10. In the Action header, select **Publish** to make the **Get ServiceNow Array.Object Schema \(Dynamic\)** action available to other actions within the Global scope.


## Create a custom action to test dynamic outputs

Create a sample action to dynamically generate two action outputs, `Record` and `Records` which refresh dynamically when the value for the **Table** input changes.

### Before you begin

Role required: action\_designer or admin

### About this task

This custom action uses two data gathering actions to populate dynamic outputs.

### Procedure

1.  In the main header, select the create flow, subflow, or action icon \(![Create flow, subflow, or action icon](../images/create-flow-subflow-or-action-icon.png)\) and select **Action**.

    1.  In the Action Properties modal, in the **Name** field, enter `Get ServiceNow Records (Dynamic)`.

    2.  Select **Submit**.

2.  In the Action Outline, select **Inputs**.

    1.  In the Action Input header, select **Create Input**.

    2.  In the **Label** and **Name** fields, enter `Table`.

    3.  In the **Type** field, select `Dynamic Choice`.

    4.  To make the input required, toggle the **Mandatory** slider so that it is active.

    5.  Select the Toggle advanced inputs icon \(![Toggle advanced inputs icon](../images/toggle-advanced-inputs-icon.png) to display the advanced options for the `Table` input.

    6.  In the **Default value** field, enter `incident`.

    7.  Under Dynamic Options, in the **Action** field, select **Get ServiceNow Tables - Dynamic**.

    8.  Select **Create Input** to create another action input.

    9.  In the **Label** and **Name** fields, enter `NumberOfRecords`.

    10. In the **Type** field, select **Integer**.

    11. To make the input required, toggle the **Mandatory** slider so that it is active.

    12. Select the Toggle advanced inputs icon \(![Toggle advanced inputs icon](../images/toggle-advanced-inputs-icon.png) to display the advanced options for the `Table` input.

    13. In the **Default value** field, enter `3`.

3.  In the Action Outline, select the add a new step icon \(![New step icon](../images/add-new-step-icon.png)\) under Inputs and select the **REST** step.

4.  Under the REST step header, fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Connection|Leave **Use Connection Alias** selected.|
    |Connection Alias|Select the create new record icon \(![Create new record icon](../images/create-new-record-icon.png)\) to create a new [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), or use an existing connection for your instance. The **Credential** for the HTTP\(s\) connection must use [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US). Additionally, the **Connection URL** must be the base URL for your instance, including the forward slash at the end.|
    |Build Request|Leave **Manually** selected|
    |Resource Path|Enter `api/now/table/` and then select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\). Select **Inputs** &gt; **Table**.|
    |HTTP Method|Enter `GET`|
    |Query Parameters|Select the plus icon \(![Plus icon](../../../build/app-engine-studio/image/plus-icon.png) to add a new query parameter. Then, enter `sysparm_limit` in the **Name** field. Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and then select **Inputs** &gt; **NumberOfRecords**.|

5.  In the Action Outline, select the add a new step icon \(![New step icon](../images/add-new-step-icon.png)\) under **Inputs** and select the **Script** step.

    1.  In the Input Variables section, select **Create Variable**.

    2.  In the **Name** field, enter `payload`.

    3.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **REST Step** &gt; **Response Body**.

    4.  In the **Script** field, enter the following code.

        ```
        
        (function execute(inputs, outputs) {
          var response = JSON.parse(inputs.payload);
          var records = response.result;
          outputs.record = records[0];
          outputs.records = JSON.stringify(records);
        })(inputs, outputs);
        ```

    5.  In the Output Variables section, select **Create Variable**.

    6.  In the **Label** and **Name** fields, enter `record`.

    7.  Select **JSON** for the **Type** field.

    8.  Toggle the **Mandatory** slider so that it is active.

    9.  Select **Create Variable** to create another output variable for the script step.

    10. In the **Label** and **Name** fields, enter `records`.

    11. In the **Type** field, select `JSON`.

    12. To make the input required, toggle the **Mandatory** slider so that it is active.

6.  In the Action Outline, select **Outputs**.

    1.  In the Action Output header, select **Create Output**.

    2.  In the **Label** and **Name** fields, enter `Records`.

    3.  In the **Type** field, select **Dynamic Object**.

    4.  Select the Toggle advanced inputs icon \(![Toggle advanced inputs icon](../images/toggle-advanced-inputs-icon.png) to display the advanced options for the `Records` output.

    5.  Under Dynamic Options, select **Get ServiceNow Array.Object Schema \(Dynamic\)** as the **Action**.

    6.  To make the Table input dependent on another input, toggle the **Depends-On Another Input** slider to make it active.

    7.  In the **Table**e field, select **Table**.

    8.  In the Action Output header, select **Exit Edit Mode**.

    9.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Script Step** &gt; **records**.

    10. In the Action Output header, select **Edit Outputs** &gt; **Create Output** to create another action output.

    11. In the **Label** and **Name** fields, enter `Record`.

    12. In the **Type** field, select `Dynamic Object`.

    13. Select the Toggle advanced inputs icon \(![Toggle advanced inputs icon](../images/toggle-advanced-inputs-icon.png) to display the advanced options for the `Record` output.

    14. Under Dynamic Options, in the **Action** field, select **Get ServiceNow Object Schema \(Dynamic\)**.

    15. To make the Table input dependent on another input, toggle the **Depends-On Another Input** slider to make it active.

    16. In the **Table** field, select **Table**.

    17. In the Action Output header, select **Exit Edit Mode**.

    18. For the **Value**, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Script Step** &gt; **record**.

7.  In the Action header, select **Save** and then select **Test** to [test the action](test-action.md).

    1.  On the Test Action screen, select any dynamically generated choice value for the **Table** input.

    2.  Select **Run Test**.

    3.  Check the action's execution details.

        Your action runs successfully if the runtime value for `Record` is a properly formatted complex object and the runtime value for `Records` is a properly formatted complex object array.

8.  In the Action header, select **Publish** to make the **Get ServiceNow Records \(Dynamic\)** action available to flows within the Global scope.


### Result

![Use the Get ServiceNow Records Dynamic sample action in a flow.](../images/getting-started-dynamic-output-result.png)

You can now add the **Get ServiceNow Records \(Dynamic\)** action to a flow. This sample action dynamically generates two action outputs, `Record` and `Records`, which can be accessed as data pills in the data panel. The data pills refresh dynamically when the value for the **Table** input changes.

