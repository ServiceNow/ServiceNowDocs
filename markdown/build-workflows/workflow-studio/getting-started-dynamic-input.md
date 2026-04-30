---
title: Get started with dynamic inputs
description: Create a sample action that illustrates using all available types of dynamic inputs in a flow.Create the aliases, connections, and credentials needed to connect to your local instance.Create a custom data gathering action to fetch a list of table names from the Table API.Create a data gathering action to get a list of fields from a table.Create a data gathering action to add a reference type dynamic input.Create a custom action to test dynamic inputs.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 20
breadcrumb: [Dynamic inputs, Create an action in Workflow Studio, Building actions, Use, Workflow Studio, Build workflows]
---

# Get started with dynamic inputs

Create a sample action that illustrates using all available types of dynamic inputs in a flow.

## Before you begin

Role required: action\_designer or admin

## Procedure

1.  [Create credential and connection records for your instance](getting-started-dynamic-input.md#).

    This connection &amp; credential alias will provide the base URL and user account needed to configure the REST steps of your data gathering actions.

2.  [Create a data gathering action to get table names](getting-started-dynamic-input.md#).

    This data gathering action will provide JSON data for dynamic choice inputs.

3.  [Create a data gathering action to get field names](getting-started-dynamic-input.md#).

    This data gathering action provides JSON data for dynamic template inputs.

4.  [Create a data gathering action to add dynamic inputs](getting-started-dynamic-input.md#).

    This data gathering action provides JSON data to create arbitrary dynamic inputs.

5.  [Create a custom action to test dynamic inputs](getting-started-dynamic-input.md#).

    This custom action illustrates different types of dynamic inputs.


**Parent Topic:**[Dynamic inputs](../concept/dynamic-inputs.md)

**Related topics**  


[Create a data gathering action for a dynamic choice](create-data-gathering-action-dynamic-choice.md)

[Create a data gathering action for a dynamic template](create-data-gathering-action-dynamic-template.md)

[Create a data gathering action for a dynamic inputs type input](create-data-gathering-action-dynamic-inputs.md)

[Dynamic input configuration options](../reference/dynamic-input-options.md)

## Create credential and connection records for your instance

Create the aliases, connections, and credentials needed to connect to your local instance.

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


### Result

You can use the Local Instance alias to connect to your local instance when configuring REST steps.

## Create a data gathering action to get table names

Create a custom data gathering action to fetch a list of table names from the Table API.

### Before you begin

Role required: action\_designer or admin

### About this task

This data gathering action consists of these elements.

-   A REST step to gather table names from the REST [Table API](https://www.servicenow.com/docs/access?context=c_TableAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)
-   A script step to construct a JSON payload from the REST step's Response Body
-   An action output variable named `output` to store table name and value pairs as a JSON document

This custom action uses a REST API call to duplicate the functionality of the ServiceNow core [Look Up Record action](../reference/lookup-record-flow-designer.md) and [Look Up Records action](../reference/lookup-records-flow-designer.md). Typically, you do not need to create custom actions to perform basic record operations. This action illustrates working with the REST and Script steps to gather table data for dynamic inputs.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Actions**.

3.  Select **Create new** &gt; **Action**.

    1.  On the Action properties screen, in the **Action name** field, enter `Data Gathering Action for Tables`.

    2.  For **Application**, select Global.

    3.  Select **Submit**.

    ![Example action properties created from step 2](../images/create-dga-tables-01.png)

4.  In the Action Outline under the Inputs section, select the add a new step icon \(![Add a new step icon](../images/add-new-step-icon.png)\).

5.  From the **Integrations** section, select the **REST** step, and enter these field values.

<table id="table_pvd_ftf_mjb"><thead><tr><th>

Input

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Connection

</td><td>

Leave **Use Connection Alias** selected.

</td></tr><tr><td>

Connection Alias

</td><td>

Select the alias you created earlier, or select the Create new record icon \(![Create new record icon](../images/create-new-record-icon.png)\) to [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).**Note:** The **Credential** for the HTTP\(s\) connection must use [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US). Additionally, the **Connection URL** must be the base URL for your instance, including the forward slash at the end. For more information on connections and credentials, see [Getting started with connections](https://www.servicenow.com/docs/access?context=connection-information&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) and [Getting started with credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Build Request

</td><td>

Leave the **Manually** option selected

</td></tr><tr><td>

Resource Path

</td><td>

Enter `api/now/doc/table/schema`

</td></tr><tr><td>

HTTP Method

</td><td>

Enter `GET`

</td></tr></tbody>
</table>    ![Example REST step configuration from steps 3 and 4](../images/create-dga-tables-02-rest-step.png)

6.  In the Action Outline under your REST step, select the Add a new step icon \(![New step icon](../images/add-new-step-icon.png)\), and select the **Script** step.

    1.  In the Input Variables section, select **Create Variable**.

    2.  In the **Name** field, enter `payload`.

    3.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **REST Step** &gt; **Response Body**.

    4.  In the **Script** field, enter the following code.

        ```
        
        (function execute(inputs, outputs) {
          var payload = JSON.parse(inputs.payload);
          var tables = payload.result // Get the value of the result array
            .filter(function(table) { return table.value.indexOf('_') < 0; }) // Filter the tables we want
            .map(function(table) { 
              return { label: table.label, name: table.value }; // Set values for label and name 
          });
          outputs.tables = { data: tables }; // Final, properly formatted output
        })(inputs, outputs);
        ```

        The REST API returns a JSON-formatted string that describes each table with the image, reference, rawLabel, selected, label, missing, used, and value properties. The label and value properties provide the values needed by for a dynamic choice. A dynamic choice requires that each choice option have a label and a name. This script maps the value property to a name property.

    5.  In the Output Variables section, select **Create Variable**.

    6.  In the **Label** and **Name** fields, enter `tables`.

    7.  In the **Type** field, select `JSON`.

    ![Example Script step configuration from step 5](../images/create-dga-tables-03-script-step.png)

7.  In the Action Outline, select **Outputs**.

    1.  Select **Create Output**.

    2.  In the **Label** and **Name** fields, enter `output`.

    3.  In the **Type** field, select `JSON`.

    4.  Select **Exit Edit Mode**.

    5.  Next to the **Value**, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Script step** &gt; **tables**.

    ![Example action output configuration from step 6](../images/create-dga-tables-04-outputs.png)

8.  In the Action header, select **Save** and then select **Test** to [test the action](test-action.md).

    1.  Select **Run Test**.

    2.  View the action's execution details.

        Your data gathering action runs successfully if the runtime value for `tables` is a complex object containing an array of key-value pairs for `label` and `name` as shown in the following abbreviated example.

        ```
        {
          "data": [
            {
              "name": "evaluation",
              "label": "A/B Testing Evaluation"
            },
            {
              "name": "sla",
              "label": "Agreement"
            },
            {
              "name": "announcement",
              "label": "Announcement"
            },
            {
              "name": "cmdb",
              "label": "Base Configuration Item"
            },
            {
              "name": "checklist",
              "label": "Checklist"
            },
            {
              "name": "collaborator",
              "label": "Collaborator"
            },
            {
              "name": "conflict",
              "label": "Conflict"
            },
            {
              "name": "clone",
              "label": "Database Clone"
            },
            {
              "name": "dsl",
              "label": "DML"
            },
            {
              "name": "global",
              "label": "Global"
            },
            {
              "name": "goal",
              "label": "Goal"
            },
            {
              "name": "incident",
              "label": "Incident"
            },
            {
              "name": "interaction",
              "label": "Interaction"
            },
            {
              "name": "map",
              "label": "Map"
            },
            {
              "name": "ola",
              "label": "OLA"
            },
            {
              "name": "problem",
              "label": "Problem"
            },
            {
              "name": "question",
              "label": "Question"
            },
            {
              "name": "reminder",
              "label": "Reminder"
            },
            {
              "name": "instance",
              "label": "ServiceNow Instance"
            },
            {
              "name": "label",
              "label": "Tag"
            },
            {
              "name": "task",
              "label": "Task"
            },
            {
              "name": "taxonomy",
              "label": "Taxonomy"
            },
            {
              "name": "ticket",
              "label": "Ticket"
            },
            {
              "name": "topic",
              "label": "Topic"
            },
            {
              "name": "expert",
              "label": "Wizard"
            }
          ]
        }
        ```

    ![Example action execution details from step 7](../images/create-dga-tables-06-execution-details.png)

9.  In the Action header, select **Publish** to make this action available to other flows and actions within the Global scope.


## Create a data gathering action to get field names

Create a data gathering action to get a list of fields from a table.

### Before you begin

Role required: action\_designer or admin

### About this task

This data gathering action consists of these elements.

-   A REST step to gather fields from the REST [Table API](https://www.servicenow.com/docs/access?context=c_TableAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)
-   A script step to construct a JSON payload from the REST step's Response Body
-   An action output variable named `output` to store field name and value pairs as a JSON document

This custom action uses a REST API call to duplicate the functionality of the ServiceNow core [Look Up Record action](../reference/lookup-record-flow-designer.md) and [Look Up Records action](../reference/lookup-records-flow-designer.md). Typically, you do not need to create custom actions to perform basic record operations. This action illustrates working with the REST and Script steps to gather field data for dynamic inputs.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Actions**.

3.  Select **Create new** &gt; **Action**.

    1.  On the Action properties screen, in the **Action name** field, enter `Data Gathering Action for Fields`.

    2.  For **Application**, select Global.

    3.  Select **Submit**.

    ![Example action properties from step 2](../images/create-dga-fields-01-action-properties.png)

4.  From the Action Outline, select **Inputs**.

    1.  In the Action Input header, select **Create Input**.

    2.  In the **Label** and **Name** fields, enter `Table`.

    3.  In the **Type** field, select **String**.

    4.  Toggle the **Mandatory** slider so that it is active.

    5.  Select the Toggle Advanced Inputs icon to show the advanced inputs.

    6.  For **Default value**, enter `incident`.

    ![Example input configuration from step 3](../images/create-dga-fields-02-inputs.png)

5.  In the Action Outline under the REST step, select the Add a new step icon \(![New step icon](../images/add-new-step-icon.png)\).

6.  From the **Integrations** section, select the **Script** step, and enter these field values.

    1.  In the Input Variables section, select **Create Variable**.

    2.  In the **Name** field, enter `table`.

    3.  Next to the **Value**, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Action** &gt; **Table**.

    4.  In the **Script** field, enter the following code.

        ```
        
        (function execute(inputs, outputs) {
            if(!inputs.table || inputs.table === "-- None --") { // check for empty or no table 
              outputs.table = "incident"; // set default table to incident
            } else {
              outputs.table = inputs.table; // use input value provided
            }
        })(inputs, outputs);
        ```

        This script ensures that the REST step always has a table name.

    5.  In the Output Variables section, select **Create Variable**.

    6.  In the **Label** and **Name** fields, enter `table`.

    7.  In the **Type** field, select **String**.

    ![Example Script step configuration from step 5](../images/create-dga-fields-02-script-input-default-value.png)

7.  In the Action Outline under the Inputs section, select the Add a new step icon \(![New step icon](../images/add-new-step-icon.png)\).

8.  From the **Integrations** section, select the **REST** step, and enter these field values.

<table id="table_gym_n5f_mjb"><thead><tr><th>

Input

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Connection

</td><td>

Leave **Use Connection Alias** selected.

</td></tr><tr><td>

Connection Alias

</td><td>

Select the alias you created earlier, or select the Create new record icon \(![Create new record icon](../images/create-new-record-icon.png)\) to [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).**Note:** The **Credential** for the HTTP\(s\) connection must use [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US). Additionally, the **Connection URL** must be the base URL for your instance, including the forward slash at the end. For more information on connections and credentials, see [Getting started with connections](https://www.servicenow.com/docs/access?context=connection-information&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) and [Getting started with credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Build Request

</td><td>

Leave **Manually** selected.

</td></tr><tr><td>

Resource Path

</td><td>

Enter `api/now/table/` and then select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\). Select **Script step** &gt; **Table**.

</td></tr><tr><td>

HTTP Method

</td><td>

Enter `GET`

</td></tr><tr><td>

Query Parameters

</td><td>

Add this query parameter to make the REST API only return one record.-   **Name**: sysparm\_limit
-   **Value**: 1


</td></tr></tbody>
</table>    ![Example REST step configuration from step 7](../images/create-dga-fields-03-rest-step.png)

9.  In the Action Outline under the REST step, select the Add a new step icon \(![New step icon](../images/add-new-step-icon.png)\).

10. From the **Integrations** section, select the **Script** step, and enter these field values.

    1.  In the Input Variables section, select **Create Variable**.

    2.  In the **Name** field, enter `payload`.

    3.  Next to the **Value**, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **REST Step** &gt; **Response Body**.

    4.  In the **Script** field, enter the following code.

        ```
        
        (function execute(inputs, outputs) {
          var payload = JSON.parse(inputs.payload);
          var fields = Object.keys(payload.result[0]) // Get first record of array
            .map(function(property) {
              return {
                label: property.charAt(0).toUpperCase() + property.slice(1).replace(/_/g, ' '), // Create label from field name
                name: property, // Set name to field name
                value: '' // Set value to empty so that dynamic template can set value
              };
            });
          outputs.fields = { data: fields }; // final properly formatted output
        })(inputs, outputs);
        ```

        The REST API returns a JSON-formatted string that describes each field as a set of name value pairs where the name is the field name and value is the field value. A dynamic template only needs the field name and label. The field value must be blank so that it can be set by the template value. The label property is calculated from the field name by capitalizing the first letter and replacing underscore characters with spaces.

    5.  In the Output Variables section, select **Create Variable**.

    6.  In the **Label** and **Name** fields, enter `fields`.

    7.  In the **Type** field, select **JSON**.

    ![Example Script step configuration from step 9](../images/create-dga-fields-04-script-step.png)

11. In the Action Outline, select **Outputs**.

    1.  On the Action Output header, select **Create Output**.

    2.  In the **Label** and **Name** fields, enter `output`.

    3.  In the **Type** field, select **JSON**.

    4.  Select **Exit Edit Mode**.

    5.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and then select **Script step** &gt; **fields**.

    ![Example output configuration from step 8](../images/create-dga-fields-05-outputs.png)

12. In the Action header, select **Save** and then select **Test** to [test the action](test-action.md).

    1.  On the Test Action screen, in the **Table** field, enter `incident`.

    2.  Select **Run Test**.

    3.  View the action's execution details.

        Your data gathering action runs successfully if the runtime value for `output` is a complex object containing an array of key-value pairs for `label`, `name`, and `value` as shown in the following abbreviated example.

        ```
        {
            "data": [
              {
                "name": "parent",
                "label": "Parent",
                "value": ""
              },
              {
                "name": "made_sla",
                "label": "Made sla",
                "value": ""
              },
              {
                "name": "caused_by",
                "label": "Caused by",
                "value": ""
              },
              {
                "name": "watch_list",
                "label": "Watch list",
                "value": ""
              },
              {
                "name": "upon_reject",
                "label": "Upon reject",
                "value": ""
              },
              {
                "name": "sys_updated_on",
                "label": "Sys updated on",
                "value": ""
              },
              {
                "name": "...",
                "label": "...",
                "value": ""
              },
              {
                "name": "category",
                "label": "Category",
                "value": ""
              }
            ]
          }
        ```

    ![Example action execution details from step 9](../images/create-dga-fields-07-execution-details.png)

13. In the Action header, click **Publish** to make this action available to other actions within the Global scope.


## Create a data gathering action to add dynamic inputs

Create a data gathering action to add a reference type dynamic input.

### Before you begin

Role required: action\_designer or admin

### About this task

This data gathering action includes these elements.

-   An action input variable to store a table name
-   A script step to construct two dynamic inputs as a JSON object
-   An action output variable named `output` to store the dynamic inputs

This custom action uses a reference type input to duplicate the functionality of the ServiceNow core [Look Up Record action](../reference/lookup-record-flow-designer.md) and [Look Up Records action](../reference/lookup-records-flow-designer.md). Generally, you don’t need to create custom actions to perform basic record operations. This action illustrates working with the Script steps to gather field data for dynamic inputs.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Actions**.

3.  Select **Create new** &gt; **Action**.

    1.  On the Action properties screen, in the **Action name** field, enter `Data Gathering Action for Dynamic Inputs`.

    2.  For **Application**, select Global.

    3.  Select **Submit**.

    ![Example action properties from step 2](../images/create-dga-dynamic-01-action-properties.png)

4.  From the Action Outline, select **Inputs**.

    1.  In the Action Input header, select **Create Input**.

    2.  In the **Label** and **Name** fields, enter `Table`.

    3.  In the **Type** field, select **String**.

    4.  Select the Toggle Advanced Inputs icon \(![Toggle advanced input icon](../images/icon-toggle-advanced-input.png)\).

    5.  In the **Default value** field, enter `sys_user`.

    ![Example action input configuration from step 3](../images/create-dga-dynamic-02-inputs.png)

5.  In the Action Outline under Inputs, select the Add a new step icon \(![New step icon](../images/add-new-step-icon.png)\).

6.  From the **Integrations** section, select the **Script** step, and enter these field values.

    1.  In the Input Variables section, select **Create Variable**.

    2.  In the **Name** field, enter `table`.

    3.  Next to the **Value**, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Inputs** &gt; **Table**.

    4.  In the **Script** field, enter the following code.

        ```
        
        (function execute(inputs, outputs) { 
            // Define JSON for desired dynamic input type
            outputs.data = { 
                data: [{
                  label: 'Reference type input',
                  name: 'referencetype',
                  reference: inputs.table,
                  type: 'reference',
                }]
              }
          })(inputs, outputs);
        ```

        Each type of dynamic input has its own JSON structure. A reference field dynamic input needs these properties.

        -   **label**

            The text to display next to the input. For example, Reference field input.

        -   **name**

            The internal name of the dynamic input used to identify it and to store values. For example, referencetype.

        -   **reference**

            The target table name of the reference field. For example, sys\_user. In this script, the table name is a variable.

        -   **type**

            The data type of the dynamic input. For example, reference. The type property determines how Workflow Studio displays the input and what other properties are required to configure it.

    5.  In the Output Variables section, select **Create Variable**.

    6.  In the **Label** and **Name** fields, enter `data`.

    7.  In the **Type** field, select **JSON**.

    ![Example script step configuration from steps 4 through 5](../images/create-dga-dynamic-03-script-step.png)

7.  In the Action Outline, select **Outputs**.

    1.  On the Action Output header, select **Create Output**.

    2.  In the **Label** and **Name** fields, enter `output`.

    3.  In the **Type** field, select **JSON**.

    4.  Select **Exit Edit Mode**.

    5.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and then select **Script step** &gt; **data**.

    ![Example output configuration from step 6](../images/create-dga-dynamic-04-outputs.png)

8.  In the Action header, select **Save** and then select **Test** to [test the action](test-action.md).

    1.  Select **Run Test**.

    2.  View the action's execution details.

        If your data gathering action runs successfully, then the runtime value for `output` is a JSON string as shown in the following example.

        ```
        {
          "data": [
            {
              "reference": "sys_user",
              "name": "referencetype",
              "label": "Reference type input",
              "type": "reference"
            }
          ]
        }
        ```

    ![Example action execution details from step 7](../images/create-dga-dynamic-06-execution-details.png)

9.  In the Action header, select **Publish** to make this action available to other actions within the Global scope.


## Create a custom action to test dynamic inputs

Create a custom action to test dynamic inputs.

### Before you begin

Role required: action\_designer or admin

### About this task

This helper action duplicates the functionality of the [Create Record step](../reference/create-record-action-designer.md) to illustrate gathering data from a REST step. Generally, you use dynamic inputs for integrations to third-party systems and data.

This custom action includes these elements.

-   An input of type Dynamic Choice to select a table
-   An input of type Dynamic Template to select and set field values
-   A script step to create a record from the [GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)
-   An action output variable named `output` to store the sys\_id of the record created

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Actions**.

3.  Select **Create new** &gt; **Action**.

    1.  On the Action properties screen, in the **Action name** field, enter `Create Record from Dynamic Inputs`.

    2.  For **Application**, select Global.

    3.  Select **Submit**.

    ![Example action properties configuration from step 2](../images/create-custom-action-01-action-properties.png)

4.  In the Action Outline, select **Inputs**.

    1.  Select **Create Input**.

    2.  In the **Label** and **Name** fields, enter `Table`.

    3.  In the **Type** field, select **Dynamic Choice**.

    4.  Turn on the **Mandatory** toggle switch.

    5.  In **Default value**, enter `incident`.

    6.  Accept the default value for **Choice**.

    7.  Under Dynamic Options for the **Action** field, select **Data Gathering Action for Tables**.

    8.  Select **Create Input** to create another action input.

    9.  In the **Label** and **Name** fields, enter `Fields`.

    10. In the **Type** field, select **Dynamic Template**.

    11. Turn on the **Mandatory** toggle switch.

    12. Under Dynamic Options in the **Action** field, select **Data Gathering Action for Fields**.

    13. Next to the **Table** field, turn on the **Depends-On Another Input** toggle switch.

    14. In the **Table** field, select the **Table** input.

    15. Select **Create Input** to create another action input.

    16. In the **Label** and **Name** fields, enter `Dynamic Input`.

    17. In the **Type** field, select **Dynamic Inputs**.

    18. Under Dynamic Options in the **Action** field, select **Data Gathering Action for Dynamic Inputs**.

    19. Leave the **Table** field blank to use the default value of sys\_user provided by the data gathering action.

    ![example inputs configuration from step 3](../images/create-custom-action-02-inputs.png)

5.  In the Action Outline under the Inputs section, select the Add a new step icon \(![New step icon](../images/add-new-step-icon.png)\).

6.  From the **Integrations** section, select the **Script** step, and enter these field values.

    1.  In the Input Variables section, select **Create Variable**.

    2.  In the **Name** field, enter `table`.

    3.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Inputs** &gt; **Table**.

    4.  Select **Create Variable** to create another input variable.

    5.  In the **Name** field, enter `fields`.

    6.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Inputs** &gt; **Fields**.

    7.  Select **Create Variable** to create another input variable.

    8.  In the **Name** field, enter `payload`.

    9.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and select **Inputs** &gt; **Dynamic Input**.

    10. In the **Script** field, enter the following code.

        ```
        
        (function execute(inputs, outputs) {
            var payload = inputs.payload.referencetype; // match name from data gathering action
            var obj = JSON.parse(payload);
            var user = obj.value;
            var gr = new GlideRecord(inputs.table); // dynamic choice input
            gr.applyEncodedQuery(inputs.fields); // dynamic template input
            gr.applyEncodedQuery("caller_id=" + user); // dynamic inputs reference field
            gr.insert();
            outputs.record = gr;
            })(inputs, outputs);
        ```

    11. In the Output Variables section, select **Create Variable**.

    12. In the **Label** and **Name** fields, enter `record`.

    13. In the **Type** field, select **Document ID**.

    ![Example Script step configuration from steps 4 through 5](../images/create-custom-action-03-script-step.png)

7.  In the Action Outline, select **Outputs**.

    1.  On the Action Output header, select **Create Output**.

    2.  In the **Label** and **Name** fields, enter `Record Created`.

    3.  In the **Type** field, select **Document ID**.

    4.  Select **Exit Edit Mode**.

    5.  Next to the **Value** field, select the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and then select **Script step** &gt; **record**.

    ![Example outputs configuration from step 6](../images/create-custom-action-04-outputs.png)

8.  In the Action header, select **Save** and then select **Test** to [test the action](test-action.md).

    1.  On the Test Action screen, in the **Table** input, select any dynamically generated table choice option.

        For example, select the Incident table.

    2.  Select **Add Field Value**, select any field, and enter any value.

        For example, select the Short description field and enter the value test.

    3.  In the Dynamic inputs section and the **Reference type input** field, select a reference field value.

        For example, select the user Abel Tuter.

    4.  Select **Run Test**.

        **Note:** Records you create from the Table API bypass data policies and required fields normally related with record creation. This action is for illustration purposes only. Use the [Create Record step](../reference/create-record-action-designer.md) instead to create records with standard protections and validations.

    5.  View the action's execution details.

        You can use the Record Created output to verify that the runtime values for `Table` and `Field` match the test values you entered.

    ![Example action execution details from step 7](../images/create-custom-action-06-execution-details.png)

9.  In the Action header, select **Publish** to make this action available to flows within the Global scope.


### Result

You can add this action to a flow in Workflow Studio. This sample action dynamically generates a list of tables and related fields in your instance whose values that you can assign during flow design.

![Example flow using the Create Record from Dynamic Inputs action](../images/example-flow-using-create-record-dynamic-inputs.png)

