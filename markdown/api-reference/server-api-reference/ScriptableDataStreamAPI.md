---
title: ScriptableDataStream - Scoped, Global
description: The ScriptableDataStream API provides methods to interact with a stream of data.Closes the connection to a data stream. Always call this method after performing any desired operations on a data stream.Returns the current index of an item in a data stream.Returns the current index of an item within the current page in a data stream.Returns the current index of a page in a data stream.Returns true if there are more items in the data stream.Returns the next item in a data stream.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ScriptableDataStream - Scoped, Global

The ScriptableDataStream API provides methods to interact with a stream of data.

This class can only be used in a server-side script after retrieving a ScriptableDataStream object using one of these APIs:

-   The executeDataStreamAction\(\) method in the FlowAPI class. See [FlowAPI](../../ScriptableFlowAPI/concept/ScriptableFlowAPI.md#).
-   The getDataStream\(\) method in the ScriptableFlowRunnerResult class. See [ScriptableFlowRunnerResult](../../ScriptableFlowRunnerResultScoped/concept/ScriptableFlowRunnerResultScopedAPI.md#).

After retrieving a ScriptableDataStream object, call the methods in this specific order:

1.  Use the [hasNext\(\)](ScriptableDataStreamAPI.md#) method to determine whether there are more items in the data stream.
2.  Use the [next\(\)](ScriptableDataStreamAPI.md#) method to access the next item in the stream.
3.  Use the [getItemIndex\(\)](ScriptableDataStreamAPI.md#), [getItemInPageIndex\(\)](ScriptableDataStreamAPI.md#), and [getPageIndex\(\)](ScriptableDataStreamAPI.md#) methods to get information from the stream.
4.  Use the [close\(\)](ScriptableDataStreamAPI.md#) method to close the stream.

This class runs is in the `sn_fd` namespace.

**Note:** Always wrap data stream logic in a `try/catch` block to catch errors. Always include a `finally` statement that ends with the close\(\) method from the ScriptableDataStream class to close the data stream and prevent performance issues.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ScriptableDataStream - close\(\)

Closes the connection to a data stream. Always call this method after performing any desired operations on a data stream.

You can only call this method on a ScriptableDataStream object returned from the executeDataStreamAction\(\) method in the FlowAPI class. See [FlowAPI](../../ScriptableFlowAPI/concept/ScriptableFlowAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
(function() {
	
	try {
​
		// Execute Data Stream Action. 
		var stream = sn_fd.FlowAPI.executeDataStreamAction('x_snc_my_scope.data_stream_name');
​
		// Process each item in the data stream
		while (stream.hasNext()) {
​
			// Get a single item from the data stream.
			var user = stream.next();
		
			// Only log the first item in each page
			if (stream.getItemInPageIndex() == 0) {
				gs.info('first user on page is ' + user.name);
			}
		}		
	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	} finally {
		stream.close();
	}
	
})();
```

## ScriptableDataStream - getItemIndex\(\)

Returns the current index of an item in a data stream.

You can only call this method on a ScriptableDataStream object returned from the executeDataStreamAction\(\) method in the FlowAPI class. See [FlowAPI](../../ScriptableFlowAPI/concept/ScriptableFlowAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Current index of an item in a data stream using zero-based indexing.|

```
(function() {
	
	try {

		// Execute Data Stream Action. 
		var stream = sn_fd.FlowAPI.executeDataStreamAction('x_my_scope.data_stream_name');

		// Process each item in the data stream
		while (stream.hasNext()) {

			// Get a single item from the data stream.
			var User = stream.next();

			// Use the item. Example:
			// var now_GR = new GlideRecord(<table_name>);
			// now_GR.<field_name> = User.<field_name>;
			// now_GR.insert();
		
			// By default, this code snippet will terminate after 10 items.
			// Remove or modify this limit after your code has been tested.
			if (stream.getItemIndex() >= 9) {
				break;
			}
		}		
	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	} finally {
		stream.close();
	}
	
})();
```

## ScriptableDataStream - getItemInPageIndex\(\)

Returns the current index of an item within the current page in a data stream.

You can only call this method on a ScriptableDataStream object returned from the executeDataStreamAction\(\) method in the FlowAPI class. See [FlowAPI](../../ScriptableFlowAPI/concept/ScriptableFlowAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Current index of an item within the current page in the data stream using zero-based indexing.|

```
(function() {
	
	try {
​
		// Execute Data Stream Action. 
		var stream = sn_fd.FlowAPI.executeDataStreamAction('x_snc_my_scope.data_stream_name');
​
		// Process each item in the data stream
		while (stream.hasNext()) {
​
			// Get a single item from the data stream.
			var user = stream.next();
		
			// Only log the first item in each page
			if (stream.getItemInPageIndex() == 0) {
				gs.info('first user on page is ' + user.name);
			}
		}		
	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	} finally {
		stream.close();
	}
	
})();
```

## ScriptableDataStream - getPageIndex\(\)

Returns the current index of a page in a data stream.

You can only call this method on a ScriptableDataStream object returned from the executeDataStreamAction\(\) method in the FlowAPI class. See [FlowAPI](../../ScriptableFlowAPI/concept/ScriptableFlowAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Current index of a page in a data stream using zero-based indexing.|

```
(function() {
	
	try {

		// Execute Data Stream Action. 
		var stream = sn_fd.FlowAPI.executeDataStreamAction('x_my_scope.data_stream_name');

		// Process each item in the data stream
		while (stream.hasNext()) {

			// Get a single item from the data stream.
			var item = stream.next();

			// Use the item. 
			var now_GR = new GlideRecord('incident');
			now_GR.setValue('number',item.id);
			now_GR.setValue('short_description',item.name);
			now_GR.insert();
		
			// By default, this code snippet will terminate after 5 pages.
			// Remove or modify this limit after testing your code.
			if (stream.getPageIndex() >= 4) {
				break;
			}
		}		
	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	} finally {
		stream.close();
	}
	
})();
```

## ScriptableDataStream - hasNext\(\)

Returns true if there are more items in the data stream.

You can only call this method on a ScriptableDataStream object returned from the executeDataStreamAction\(\) method in the FlowAPI class. See [FlowAPI](../../ScriptableFlowAPI/concept/ScriptableFlowAPI.md#).

**Note:** By default, the instance waits for 600 seconds to retrieve a single page of data from a MID Server. If you encounter a timeout when running a Data Stream action through a MID Server, change this default by increasing the **datastream\_alternative\_env\_fetch\_page\_timeout\_seconds** system property.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_gcx_d43_bjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that determines whether there are more items in the data stream. Values include:-   true: There are more items to iterate through in the data stream.
-   false: There are no more items in the data stream.

</td></tr></tbody>
</table>This example creates an incident record for each item returned in the data stream.

```
(function() {
	
	try {

		// Execute Data Stream Action. 
		var stream = sn_fd.FlowAPI.executeDataStreamAction('x_my_scope.data_stream_name');

		// Process each item in the data stream
		while (stream.hasNext()) {

			// Get a single item from the data stream.
			var item = stream.next();

			// Use the item. 
			var now_GR = new GlideRecord('incident');
			now_GR.setValue('number',item.id);
			now_GR.setValue('short_description',item.name);
			now_GR.insert();
		
			// By default, this code snippet will terminate after 10 items.
			// Remove or modify this limit after testing your code.
			if (stream.getItemIndex() >= 9) {
				break;
			}
		}		
	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	} finally {
		stream.close();
	}
	
})();
```

## ScriptableDataStream - next\(\)

Returns the next item in a data stream.

You can only call this method on a ScriptableDataStream object returned from the executeDataStreamAction\(\) method in the FlowAPI class. See [FlowAPI](../../ScriptableFlowAPI/concept/ScriptableFlowAPI.md#).

**Note:** By default, the instance waits for 600 seconds to retrieve a single page of data from a MID Server. If you encounter a timeout when running a Data Stream action through a MID Server, change this default by increasing the **datastream\_alternative\_env\_fetch\_page\_timeout\_seconds** system property.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The next item in the data stream. This object contains the outputs defined by the Data Stream action. To view the Data Stream action outputs, navigate to the Outputs section of the Data Stream action in the Flow Designer interface.|

This example creates an incident record for each item returned in the data stream.

```
(function() {
	
	try {

		// Execute Data Stream Action. 
		var stream = sn_fd.FlowAPI.executeDataStreamAction('x_my_scope.data_stream_name');

		// Process each item in the data stream
		while (stream.hasNext()) {

			// Get a single item from the data stream.
			var item = stream.next();

			// Use the item. 
			var now_GR = new GlideRecord('incident');
			now_GR.setValue('number',item.id);
			now_GR.setValue('short_description',item.name);
			now_GR.insert();
		
			// By default, this code snippet will terminate after 10 items.
			// Remove or modify this limit after testing your code.
			if (stream.getItemIndex() >= 9) {
				break;
			}
		}		
	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	} finally {
		stream.close();
	}
	
})();
```

