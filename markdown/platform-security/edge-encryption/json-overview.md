---
title: JSON APIs
description: JSON APIs can be used after calling getAsJsonContent\(\) on either the request object or a ParameterValue property.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 4
breadcrumb: [Encryption rule objects and APIs, Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# JSON APIs

JSON APIs can be used after calling getAsJsonContent\(\) on either the request object or a ParameterValue property.

When using JSON APIs to write your encryption rule, you can follow a general format:

1.  Call getAsJsonContent\(\) on the request object. This returns an iterable object of the JsonNode underlying class.
2.  Call iterator\(\) or getIterator\(String xPath\) on the JsonNode object. This returns a JsonNodeIterator object that can be used to iterate over nodes in the JSON object.
3.  Call the hasNext\(\) method on the JsonNodeIterator object to determine whether another element is available.
4.  Call next\(\) on the JsonNodeIterator object to return the next JSON element. You cannot call next\(\) without first calling hasNext\(\).
5.  Call valueFor\(String tableName, String fieldName\) on the JSON element. This method tells the proxy that the value for this element maps to the specified field in the specified table. The proxy then checks whether the field must be encrypted.

    **Note:** To determine if you want to call valueFor\(String tableName, String fieldName\) on a JSON element, you can use the getName\(\) method to return the name of the element.


## Mapping to a known table-field on the instance

In this example, the JSON payload is processed on the instance to insert records in the incident table. The description field populates short\_description on the incident.

```
{
    data: {
        records: [
            {
                "name": "Test Record 1",
                "description": "Test Record 1 Description",
                "tag": "security"
            }, 
            {
                "name": "Test Record 1",
                "description": "Test Record 1 Description",
                "tag": "security"
            }],
        "query": "assigned_to=3D4860165813e63a00d00abd322244b092^category=vulnerability"
    },
    "source": "10.11.13.14"
}
```

The following rule can apply:

```
function sampleJsonAction1() {
    var jsonContent = request.getAsJsonContent();
    // This loop iterates over all description elements in the records array
    var jsonNodeIterator = jsonContent.getIterator(’/data/records/description’);    
    while (jsonNodeIterator.hasNext()) {
        var jsonNode = jsonNodeIterator.next();
        jsonNode.valueFor('incident', 'short_decription');
    }
}

```

This action iterates through the **description** nodes and asks the proxy server to encrypt the values and insert them into incident.short\_description on the instance.

**Note:** This rule finds all **description** nodes within the JSON payload. If there is only one occurrence of a node to encrypt, the rule still uses the xPath and iterator structure. However, it iterates only once in the loop.

## Mapping to an unknown table-field on the instance

In this example, the rule iterates over **records**, but is not sure what nodes to expect. The only known is that for each object within **records**, the nodes match the names of the columns specified in the table URL parameter.

The rule also specifies that, if the table is incident, then the data in the **description** node should be encrypted and stored in the short\_description field on the instance.

```
function sampleJsonAction2() {
    var jsonContent = request.getAsJsonContent();
    var tableName = request.urlParam.table;
    // This first iterator will iterate over all record elements
    var jsonNodeIterator = jsonContent.getIterator('data/records');
    while (jsonNodeIterator.hasNext()) {
            encryptFieldsInRecord(jsonNodeIterator.next());
    }
}
function encryptFieldsInRecord(jsonNode) {
    //this time we want to iterate over all nodes
    var fieldIterator = jsonNode.iterator();
    while (fieldIterator.hasNext()) {
            var field = fieldIterator.next();
            var fieldname = childElement.getName();
            if (fieldName == 'description') {
                field.valueFor(tableName, 'short_description');
            } else {
                field.valueFor(tableName, fieldName);
            }
    }
}
```

In the encryptFieldsInRecord\(\) function, the valueFor\(\) method is called on a table and a field that are dynamically assigned based on the request. Even though the table and field names can change, the rule asks the proxy to check whether the field in the table must be encrypted based on the encryption configurations defined.

If the field is not configured for encryption, or if the node name does not match a field in the table, the proxy skips that node. If the node name matches a field marked for encryption, then the proxy encrypts the value.

## Using an encoded query

```
function sampleJsonAction3() {
    var jsonContent = request.getAsJsonContent();
    var tableName = request.urlParam.table;
    // This first iterator will iterate over all record elements
    var jsonNodeIterator = jsonContent.getIterator('data');
    while (jsonNodeIterator.hasNext()) {
        var jsonNode = jsonNodeIterator.next();
        if (jsonNode.getName() == 'records')
            encryptRecors(jsonNodeIterator.next());
        else if (jsonNode.getName() == 'query')
            jsonNode.encodedQueryFor(tableName);
    }
}
function encryptRecords(jsonNode) {
    //we iterate over all fields in the node
    var recordIterator = jsonNode.iterator();
    while (recordIterator.hasNext()) {
        encryptFieldsInRecord(recordIterator.next());
    }
}
function encryptFieldsInRecord(jsonNode) {
    //this time we want to iterate over all nodes
    var fieldIterator = jsonNode.iterator();
    while (fieldIterator.hasNext()) {
            var field = fieldIterator.next();
            var fieldname = childElement.getName();
            field.valueFor(tableName, fieldName);
    }
}
```

In this example, the rule iterates over **data**. As it finds **records**, it performs the same logic as in the second example, iterating over fields in each node. When it finds the **query** node, it calls encodedQueryFor\(\) to encrypt values that should be encrypted in the query.

-   **[JsonNode](c_JsonNodeAPI.md#)**  
A global object that provides methods to iterate over the JSON content.
-   **[JsonNodeIterator](c_JsonNodeIteratorAPI.md#)**  
You get a JsonNodeIterator object by calling the getIterator\(\) or iterator\(\) methods of the JsonNode class.

**Parent Topic:**[Encryption rule objects and APIs](api-overview.md)

