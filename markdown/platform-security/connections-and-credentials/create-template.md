---
title: Create a configuration template
description: Create a template that defines the inputs required to set up a spoke. Set static key-value pairs to create records and set values that apply to every integration. Set dynamic key-value pairs to gather user input and set field values that may vary. Using this template, admins and flow designers can set up the spoke from a single form.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Connection &amp; Credential configuration templates, Explore credentials, connections, and aliases, Connections and Credentials, Access Management]
---

# Create a configuration template

Create a template that defines the inputs required to set up a spoke. Set static key-value pairs to create records and set values that apply to every integration. Set dynamic key-value pairs to gather user input and set field values that may vary. Using this template, admins and flow designers can set up the spoke from a single form.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Configuration Templates**.

2.  Select **New**.

3.  Select the type of configuration template that you want to create.

<table id="choicetable_brl_cpl_1jb"><thead><tr><th align="left" id="d69520e77">

Configuration type

</th><th align="left" id="d69520e80">

Description

</th></tr></thead><tbody><tr><td id="d69520e86">

**HTTP Connection with OAuth Authorization Code grant type**

</td><td>

Creates a template to register the third-party system as an OAuth provider using an authorization code.

</td></tr><tr><td id="d69520e95">

**HTTP Connection with OAuth JWT Bearer grant type**

</td><td>

Creates a template to register the third-party system as an OAuth provider using a JSON Web Token.

</td></tr><tr><td id="grant-type">

**HTTP OAuth with Client Credentials grant type**

</td><td>

Creates a template to integrate with a third-party application via the OAuth 2.0 authentication that uses the client credentials grant type.

</td></tr><tr><td id="d69520e116">

**HTTP Connection with OAuth Client Credentials grant type \(External Storage\)**

</td><td>

Creates a template that enables the sending of OAuth token request that comprises client credentials stored by an external storage to an OAuth server via the MID Server.

</td></tr><tr><td id="d69520e129">

**HTTP Connection with Basic Auth Credential**

</td><td>

Creates a template to integrate with the third-party system using basic authentication.

</td></tr><tr><td id="d69520e138">

**HTTP Connection with API Key Credential**

</td><td>

Creates a template to integrate with the third-party system using an API key.

</td></tr><tr><td id="d69520e147">

**Other Configuration**

</td><td>

Creates a blank template, enabling you to set up a template for custom authentication.

</td></tr></tbody>
</table>4.  In the **Name** field, add a name to identify the template.

5.  In the **Default Data Template** field, make any required changes.

    This field sets static information that applies to every integration. For example, you can set the API and token URL if the value applies to every integration.

    These objects in the default data template are required:

    -   `credential`: Creates a credential record with the required fields.
    -   `connection`: Creates a connection record with the required fields. Access connection attributes using the `extended_attributes` child object. For example:

        ```
        "connection": {
                    "extended_attributes": {
                        "api_version": "v1"
                     
                     },
                "connection_url": "https://<provider-domain-name>.com",
                "name": "Spoke Connection",
                "table": "http_connection"
            }
        ```

    You can use the `additional` object to set up data for a custom table, and use the post processing script to insert the data into the table.

    **Note:** In the default data template for the OAuth Authorization Code grant type, the values for the `oauth_entity_profile_scope` and the `oauth_entity_scope` keys must match. In the following example, both keys have the `Read user's email` value.

    ```
    "oauth_entity_profile": [
            {
              "grant_type": "authorization_code",
              "name": "<provider-name> Profile",
              "default": true,
              "oauth_entity_profile_scope": [
                "Read user's email"
              ]
            }
          ],
          "code_challenge_method": "S256",
          "type": "consumer",
          "oauth_entity_scope": [
            {
              "oauth_entity_scope": "Read user's email",
              "name": "email"
            }
          ],
    ```

6.  In the **Dynamic Data Schema** field, make any required changes.

    This field Defines the information that the user must complete to set up the integration. For example, you can add user name and password key-value pairs to gather user-defined values.

    Fields in the dynamic data schema include these properties:

    -   `name`: The field that the user's input maps to. For example, to map user input to the Connection URL field in the Connection record, enter `connection.connection_url`.
    -   `label`: The field label that the user sees when completing the template.
    -   `type`: The field type. Make sure that this data type matches the data type of the field you are mapping the value to.
    -   `defaultValue`: Optional. The field's default value. If no default is provided, the hint displays.
    -   `hint`: Optional. Hint text to display when there is no default value.
    **Note:** If setting up a template for OAuth JWT Bearer grant type authentication, you may want user input for a single key-value pair in the `jwt_claim_validation` array. You can refer to a single key-value pair in the dynamic data schema by referring to its index in the array. For example, your default data template might include this snippet.

    ```
    "jwt_claim_validation" : [ {
            "name" : "iss",
            "is_standard" : true,
            "data_type" : "string",
            "value":"<docusign-iss-claim>"
          }, {
            "name" : "sub",
            "is_standard" : true,
            "data_type" : "string",
            "value":"<docusign-sub-claim>"
          }, {
            "name" : "aud",
            "is_standard" : true,
            "data_type" : "string",
            "value":"<docusign-aud-claim>"
          }, {
            "name" : "scope",
            "is_standard" : false,
            "data_type" : "string",
            "value" : "signature impersonation"
          } ],
    ```

    Refer to the `iss` key-value pair using the item's zero-based index: `credential.jwt_provider.jwt_claim_validation[0].value`.

7.  In the **Post Processing Script** field, add a script that c Creates additional records required by the integration. For example, if your spoke includes custom tables, you can create records in those tables based on user input in the configuration template. This script executes after the connection and credential records are created.

    The post-processing script has access to these global objects.

    |Global object|Description|
    |-------------|-----------|
    |aliasId|Sys\_id of the alias record from the Connection &amp; Credential Alias \[sys\_alias\] table.|
    |connectionSysId|Sys\_id of the connection record created by the template.|
    |jsonDefaultData|JSON content from the **Default Data Template** field in String format.|
    |jsonDynamicData|JSON content from the **Dynamic Data Template** field in String format.|

8.  In the **Pre-Edit Script** field, add a script to pre-populate the additional fields when you edit a connection.

    This script returns an array of objects. Each object has a name-value pair for populating the additional fields. For example, if the connection requires fields that are in a custom table, you can map these fields to the custom table.

    The **Pre-Edit Script** has access to the following global objects:

    |Global object|Description|
    |-------------|-----------|
    |aliasId|Sys\_id of the alias record from the Connection &amp; Credential Alias \[sys\_alias\] table.|
    |connectionSysId|Sys\_id of the connection record created by the template.|
    |jsonDefaultData|JSON content from the **Default Data Template** field in String format.|
    |jsonDynamicData|JSON content from the **Dynamic Data Template** field in String format.|

    Each object in the script has the following properties:

    -   `name`: Name of the custom field to specify the value in the connection.
    -   `value`: Value that you want to map to populate the custom field. You can map the field either by using a function, variable, or by hard-coding it.
    The following data types are supported for the fields:

<table id="table_of3_4lg_35b"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Text

</td><td>

String value.

</td></tr><tr><td>

Boolean

</td><td>

Selection box. Selection indicates true value and unselection indicates false value.

</td></tr><tr><td>

Number

</td><td>

Numerical value.

</td></tr><tr><td>

Date

</td><td>

Date value in yyyy-mm-dd format. You can also use the GlideDate object.

</td></tr><tr><td>

Choice

</td><td>

List of valid choices defined in the **Dynamic Data Schema** field.

</td></tr><tr><td>

Reference

</td><td>

Valid GlideRecord.

</td></tr><tr><td>

Radio group

</td><td>

Groups that contains a different set of fields. These groups are available as a choice in a drop-down list when you edit a connection. The fields in each group appear when you select the required group from the drop-down list. For example, consider the following structure of radio group defined in the **Dynamic Data Schema** field:

```
             {
		"name": "radio_groups",
		"label": "Radio Groups",
		"type": "radio",
		"groups": [{
			"name": "radio_group1",
			"label": "Radio Group 1",
			"fields": [{
				"name": "radio_field1",
				"label": "Radio Field 1",
				"type": "text",
				"defaultValue": "efgh",
				"mandatory": true
			}]
		}, {
			"name": "radio_group2",
			"label": "Radio Group 2",
			"fields": [{
				"name": "radio_field2",
				"label": "Radio Field 2",
				"type": "text",
				"defaultValue": "abcd",
				"mandatory": true
			}],
			"default_group": true
		}
```

 For this example, you can use the following code snippet to understand how radio groups are used in the script by using dot-walking:

 ```
            {
            	name: "radio_field.first_radio_group.radio_field1",
            	value: "radio field 1"
            }, {
            	name: "radio_field.second_radio_group.radio_field2",
            	value: "radio field 2"
            }, {
            	name: “radio_groups”,
            	value: gr.getValue(‘radio_groups’)
            }
```

 For more information on how to use dot-walking, see [Dot-walking](https://www.servicenow.com/docs/access?context=c_DotWalking&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>    **Tip:** If the pre-populated values are not appearing in the fields while editing a connection, navigate to **System Diagnostics** &gt; **Session Debug** &gt; **Debug Log** to diagnose the issue.

9.  In the **Test Action** field, enter the name of the test action.

    Creating a test action enables you to test a connection directly from an integration action in the flow view of Workflow Studio. The test action uses an action definition to test the alias that the template is currently attached to. For details, see [Create a test action to test a connection alias from a configuration template](https://www.servicenow.com/docs/access?context=test-alias-configuration-template&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

10. Add the template to a Connection &amp; Credential alias.

    1.  Navigate to **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open the alias record for the spoke.

    3.  In the **Configuration Template** field, click the Lookup icon.

    4.  Select the template that you created from the list.

    5.  Click **Update**.


## Result

When the user navigates to the associated Connection &amp; Credential alias and selects **Create New Connection &amp; Credential**, a dialog appears to collect their input. If you created a template for the OAuth Authorization Code grant type, you can also retrieve an OAuth token from this dialog.

## What to do next

Test the template by navigating to the associated Connection &amp; Credential alias and selecting **Create New Connection &amp; Credential**. Verify that the dialog collects the expected data and creates the required records in the system.

**Parent Topic:**[Connection &amp; Credential configuration templates](../concept/spoke-configuration-template.md)

