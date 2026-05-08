---
title: Example 1: Retrieving all incident records from an external source
description: These are examples of script definitions you might create for retrieval and caching of data from sources external to your current instance. In this first example, we create a script to load all incident records from an external source.
locale: en-US
release: australia
product: Remote Tables
classification: remote-tables
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create script definitions, Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Example 1: Retrieving all incident records from an external source

These are examples of script definitions you might create for retrieval and caching of data from sources external to your current instance. In this first example, we create a script to load all incident records from an external source.

For Remote Table API information, refer to:

-   v\_query – Scoped, Global
-   v\_record - Scoped, Global
-   v\_table – Scoped, Global

```javascript
/**
 * Using `v_query`, add the rows to `v_table`
 */
(function executeQuery(v_table, v_query) {
​
	fetchAllIncidents(v_table, v_query);
​
	/**
	 * fetch all incidents records from the remote instance
	 */
	function fetchAllIncidents(v_table, v_query) {
		// Uses RestMessage with name 'Remote Instance Incidents' and function 'All Incidents'
		// Create a RestMessage first which calls an external REST service
		try {
			var restMessage = new sn_ws.RESTMessageV2('Remote Instance Incidents', 'All Incidents');
			var response = restMessage.execute();
			var responseBody = response.getBody();
			
			// if REST call ends up in an error, set the last error message which shows up
			// at the bottom of the list view
			if (response.haveError()) {
				v_query.setLastErrorMessage(response.getErrorMessage());
				// can use gs.error() or gs.addErrorMessage() while debugging
				// gs.debug() messages visible in session debugger
				// gs.debug(response.getErrorMessage());
				return;
			}
		} catch (ex) {
			v_query.setLastErrorMessage(ex.message);
			// gs.debug(ex.message);
			return;
		}
​
		var transformerDefinition = getTransformerDefinition();
		var transformer = new sn_tfrm.Transformer(transformerDefinition, responseBody);
		// transformer parses the responseBody and extracts rows
		while (transformer.transform()) {
			// row is field-value map e.g. { active:"true", number: "INC0000001"}
			var row = transformer.getRow();
			// you may do any additional transformations to the row like GlideDuration, GlideDataTime etc. For example,
			// row.duration = new GlideDuration(row.duration);
​
			// finally add the row to the remote table
			v_table.addRow(row);
		}
	}
​
	/**
	 * returns a sn_tfrm.TransformerDefinition, which defines the mapping of the table fields and elements in the response body
	 */
	function getTransformerDefinition() {
		// create a rule list to map a field to its element path
		var ruleList = new sn_tfrm.TransformerRuleList()
			.fromJSON() // the response body is a JSON
			// 'active' field maps to path '$.active'
			.addRule("active", "$.active")
			.addRule("caller_id", "$.caller_id.value")
			.addRule("number", "$.number")
			.addRule("short_description", "$.short_description")
			.addRule("sys_id", "$.sys_id")
			.addRule("updates", "$.sys_mod_count");
​
		var recordPath = "$.result";
		return new sn_tfrm.TransformerDefinition(ruleList, recordPath);
	}
	
})(v_table, v_query);
```

These code snippets are of note in this script:

```
function fetchAllIncidents(v_table, v_query) {
		// Uses RestMessage with name 'Remote Instance Incidents' and function 'All Incidents'
		// Create a RestMessage first which calls an external REST service
		try {
			var restMessage = new sn_ws.RESTMessageV2('Remote Instance Incidents', 'All Incidents');
			var response = restMessage.execute();
			var responseBody = response.getBody();
			
			// if REST call ends up in an error, set the last error message which shows up
			// at the bottom of the list view
			if (response.haveError()) {
				v_query.setLastErrorMessage(response.getErrorMessage());
				// can use gs.error() or gs.addErrorMessage() while debugging
				// gs.debug() messages visible in session debugger
				// gs.debug(response.getErrorMessage());
				return;
			}
		} catch (ex) {
			v_query.setLastErrorMessage(ex.message);
			// gs.debug(ex.message);
			return;
		}
```

You can create a RestMessage and directly use it in the script. In this example, it uses a RESTMessageV2 API with the name of `Remote Instance Incidents`, and the function `All Incidents`, which gets all incident data. Once a response is returned from the server, an error message appears if problems are encountered in the data retrieval.

**Note:** To learn more about use of RESTMessageV2 and how to define a direct message, see RESTMessageV2 - Scoped, Global and Direct RESTMessageV2 example.

If no problems are encountered in the data retrieval, it gets the data body for the records.

```
		var transformerDefinition = getTransformerDefinition();
		var transformer = new sn_tfrm.Transformer(transformerDefinition, responseBody);
		// transformer parses the responseBody and extracts rows
		while (transformer.transform()) {
			// row is field-value map e.g. { active:"true", number: "INC0000001"}
			var row = transformer.getRow();
			// you may do any additional transformations to the row like GlideDuration, GlideDataTime etc. For example,
			// row.duration = new GlideDuration(row.duration);
​
			// finally add the row to the remote table
			v_table.addRow(row);

```

It then uses the Transformer API to perform any required data transformations, extracts rows, and then adds a row for each record to the remote table.

```
/**
	 * returns a sn_tfrm.TransformerDefinition, which defines the mapping of the table fields and elements in the response body
	 */
	function getTransformerDefinition() {
		// create a rule list to map a field to its element path
		var ruleList = new sn_tfrm.TransformerRuleList()
			.fromJSON() // the response body is a JSON
			// 'active' field maps to path '$.active'
			.addRule("active", "$.active")
			.addRule("caller_id", "$.caller_id.value")
			.addRule("number", "$.number")
			.addRule("short_description", "$.short_description")
			.addRule("sys_id", "$.sys_id")
			.addRule("updates", "$.sys_mod_count");
​
		var recordPath = "$.result";
		return new sn_tfrm.TransformerDefinition(ruleList, recordPath);
	}
	
})(v_table, v_query);

```

`getTransformerDefinition` defines the schema of the record in the external API response body. It maps each of the fields in the table script to an element in the external record. Any external data elements outside of this mapping are not supported or retrieved.

**Note:** You must map a sys\_id in the transformer definition to an element in the external data. In this case, the sys\_id is mapped to the external incident sys\_id. The maximum length of the sys\_id is 32 characters. You do this sys\_id mapping so forms that use the external data can operate properly.

**Parent Topic:**[Create script definitions for a remote table](../task/create-remote-table-script.md)

**Related topics**  


[Debugging remote table script definitions](debugging-remote-table-scripts.md)

[bundle-crapiref.TransformerDefinitionAPI]

[bundle-crapiref.TransformerRuleListAPI]

[bundle-crapiref.TransformerScriptedAPI]

