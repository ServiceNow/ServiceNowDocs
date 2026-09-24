---
title: Run script action
description: Run custom JavaScript code within a reusable action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/run-script-action.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [run script, javascript, workflow studio, flow designer, custom script]
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Run script action

Run custom JavaScript code within a reusable action.

## Roles and availability

Available as a Workflow Studio action.

-   **Role requirements**

    Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details. To run script from a MID Server requires a Integration Hub subscription.


## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Run Time**

    Data type: **Choice**

    The runtime environment required to support the script. Choices include:

    -   **Instance**: The action runs the script from the instance. Select this option when the script needs access to the ServiceNow API or instance data. This is the default value.
    -   **MID**: The action runs the script from a MID Server. Select this option when the script needs access to [MID Server script files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/mid-server-script-attach.md) and APIs. Selecting this option displays the **Select MID Server Using** input.
    -   **Vanilla \(Core JavaScript\)**: The action runs the script from either the instance or MID Server. Select this option when the script only needs the core JavaScript APIs and not the ServiceNow API or instance data.
    The runtime you select determines the JavaScript objects and methods displayed in the Context-sensitive help.

-   **Select MID Server Using**

    Data type: **Choice**

    The MID Server selection process to use. Choices include:

    -   **Any MID**. The system runs the action from any available MID Server.
    -   **Use Connection Alias**. The system runs the action using the connection alias you specify. Selecting this option displays the **Connection Alias** field.
    -   **Use Inline Selection**. The system runs the action using the connection details you specify. Selecting this option displays the **Host**, **MID Application**, and **Capabilities** fields.
-   **Connection Alias**

    Data type: **Record**

    Connection &amp; Credential alias record that the system uses to run the action. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates having to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't have to update your custom action. To learn more about connections and credentials, see [credentials, connections, and aliases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/credentials-connections-alias.md).

    The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel.

    **Note:** This input is only visible when Integration Hub is activated, you select **Use Connection Alias** from **Select MID Server Using**, and when **Use Connection Alias** is selected from the Connection list.

-   **Host**

    Data type: **String**

    The fully-qualified domain name of the target host where the system runs the action. For example, `host.domain.com`.

    **Note:** This input is only visible when Integration Hub is activated, and you select **Use Inline Selection** from **Select MID Server Using**.

-   **Mid Selection**

    Data type: **Choice**

    Option to select a specific MID Server or MID Cluster. Choose any one of the following options.

    -   **Auto-Select MID Server**: Your instance selects the MID Server without manual input.
    -   **Specific MID Server**: Your instance uses the MID Server that you specify.
    -   **Specific MID Cluster**: Your instance uses the MID Cluster that you specify.

        A MID Cluster is a group of MID Servers that enables your instance to handle multiple integrations, and improve integration speed. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/t_ConfigureAMIDServerCluster.md).

        **Note:** This input is available when **MID** is selected from the Required Runtime list, and **Use Inline Selection** is selected from the Select MID Server Using list.

-   **MID Clustering**

    Data type: **Record**

    The Data pill for the MID Cluster record that you want to use.

    **Note:** This input is available when **MID** is selected from the Required Runtime list, and **Use Inline Selection** is selected from the Select MID Server Using list.

-   **MID Application**

    Data type: **String**

    The application the MID Server must support to be eligible for selection. The system runs the action from a MID Server that supports the selected application.

    **Note:** This input is only visible when Integration Hub is activated, **Auto-Select MID Server** is selected from the MID Selection list, and you select **Use Inline Selection** from **Select MID Server Using**.

-   **Capabilities**

    Data type: **String**

    Capabilities the MID Server must support to be eligible for selection. The system runs the action from a MID Server that supports the selected capabilities.

    **Note:** This input is only visible when Integration Hub is activated, **Auto-Select MID Server** is selected from the MID Selection list, and you select **Use Inline Selection** from **Select MID Server Using**.

-   **Specific MID Server**

    Data type: **Record**

    Data pill of the required MID Server record.

    **Note:** This field is only visible when Integration Hub is activated, **Specific MID Server** is selected from the MID Selection list, and you select **Use Inline Selection** from **Select MID Server Using**.

-   **Script**

    Data type: **String**

    Script to run within the action. Add data pills to the script to specify dynamic input values. Assign values to the **outputs** object to have the action automatically create a corresponding entries in the **Output Variables** input. For example, these script lines assign values to the message and number output variables.

    ```javascript
    outptus.message = "Hello world";
    outputs.number = 10;
    ```

    For available classes and methods, see the JavaScript API context-sensitive help or the .

    Workflow Studio runs script from the domain from which it is triggered or initiated. See [Domain separation and Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/flow-designer-domain-separation.md).

-   **Output variables**

    Data type: **Varies**

    Map JavaScript output to Workflow Studio data pills. Define output variables when you want other steps in the flow to use the script output.

    By default, the action creates a string-type output variable for each**outputs** object you assign in the **Script** input. Set the name and data type of the output variable to match the assignment you entered in the **Script** input. For example, suppose you assign an output variable to reference a specific incident record. Set the output data type to **Reference** and select the **Incident** source table.


## Outputs

Outputs depend on the output variables defined in the Output variables input. These outputs appear in the Data panel and can be used as inputs elsewhere in your flow.

**Parent Topic:**[Workflow Studio actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/flow-actions.md)

