---
title: Example 2: Retrieving specific records from a third-party source
description: In this example, we create a script to retrieve specific types of incident records from a third-party source.
locale: en-US
release: xanadu
product: Remote Tables
classification: remote-tables
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create a script definition for a remote table, Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Example 2: Retrieving specific records from a third-party source

In this example, we create a script to retrieve specific types of incident records from a third-party source.

For Remote Table API information, refer to:

-   [v\_table\(\)](https://www.servicenow.com/docs/access?context=v_tableAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
-   [v\_query\(\)](https://www.servicenow.com/docs/access?context=v_queryAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

```
/**
 * Using `v_query`, add the rows to `v_table`
 */
(function executeQuery(v_table, v_query) {
	if (v_query.isGet()) {
		bySysId(v_table, v_query, v_query.getSysId());
	}
	else if (v_query.getParameter("caller_id")) {
		byCallerId(v_table, v_query, v_query.getParameter("caller_id"));
	}
	else {
		fetchAllIncidents(v_table, v_query);
	}
​
	/**
	 * fetch all incidents records from the remote instance
	 */
	function fetchAllIncidents(v_table, v_query) {
		// Uses RestMessage with name 'Remote Instance Incidents' and function 'All Incidents'
		// Create a RestMessage first which calls an external REST service
		var restMessage = new sn_ws.RESTMessageV2('Remote Instance Incidents', 'All Incidents');
		loadData(v_table, v_query, restMessage);
	}
​
	/**
	 * fetches a specific record from the remote instance with Sys Id being `sys_id`
	 */
	function bySysId(v_table, v_query, sys_id) {
		// Uses RestMessage with name 'Remote Instance Incidents' and function 'By SysId'
		var restMessage = new sn_ws.RESTMessageV2('Remote Instance Incidents', 'By SysId');
		// sets variable 'sys_id'
		restMessage.setStringParameterNoEscape("sys_id", sys_id);
		loadData(v_table, v_query, restMessage);
	}
​
	/**
	 * fetches records from the remote instance with Caller (caller_id) being `caller_id`
	 */
	function byCallerId(v_table, v_query, caller_id) {
		var restMessage = new sn_ws.RESTMessageV2('Remote Instance Incidents', 'By CallerId');
		restMessage.setStringParameterNoEscape("caller_id", caller_id);
		loadData(v_table, v_query, restMessage);
	}
​
	/**
	 * Adds rows to `v_table` using `restMessage`
	 */
	function loadData(v_table, v_query, restMessage) {
		try {
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
​
})(v_table, v_query);
```

These code snippets are of note in this script:

```
function fetchAllIncidents(v_table, v_query) {
		// Uses RestMessage with name 'Remote Instance Incidents' and function 'All Incidents'
		// Create a RestMessage first which calls an external REST service
		var restMessage = new sn_ws.RESTMessageV2('Remote Instance Incidents', 'All Incidents');
		loadData(v_table, v_query, restMessage);
	}
```

You can create a RestMessage and directly use it in the script. In this example, it uses a RESTMessageV2 API with the name of `Remote Instance Incidents`, and the function `All Incidents`, which gets all incident data. Once a response is returned from the server, an error message appears if problems are encountered in the data retrieval.

```
	function bySysId(v_table, v_query, sys_id) {
		// Uses RestMessage with name 'Remote Instance Incidents' and function 'By SysId'
		var restMessage = new sn_ws.RESTMessageV2('Remote Instance Incidents', 'By SysId');
		// sets variable 'sys_id'
		restMessage.setStringParameterNoEscape("sys_id", sys_id);
		loadData(v_table, v_query, restMessage);
	}

```

When you query a specific record using `GlideRecord.get(“<sys_id>“)`, then `v_query.isGet()`` is ``true``. It fetches the specific record from the external service.

```
function byCallerId(v_table, v_query, caller_id) {
		var restMessage = new sn_ws.RESTMessageV2('Remote Instance Incidents', 'By CallerId');
		restMessage.setStringParameterNoEscape("caller_id", caller_id);
		loadData(v_table, v_query, restMessage);
	}

```

You can also handle any other specific query conditions in the script, such as using `caller_id` in the preceding code snippet. The remainder of this script operates in a manner similar to Example 1.

```
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
​
})(v_table, v_query);
```

If no problems are encountered in the data retrieval, it gets the data body for the records. It then uses the Transformer API to perform any required data transformations, extracts rows, and then adds a row for each record to the remote table.

`getTransformerDefinition` defines the schema of the record in the external API response body. It maps each of the fields in the table script to an element in the external record. Any external data elements outside of this mapping are not available in the remote table.

**Parent Topic:**[Create a script definition for a remote table](../task/create-remote-table-script.md)

