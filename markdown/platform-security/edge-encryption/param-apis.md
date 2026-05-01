---
title: POST and URL parameter APIs
description: POST and URL parameters can be accessed as properties of the request object using request.postParams and request.urlParams.Converts the POST or URL parameter value to a string.Returns the request as an iterable object of type JsonNode.Returns the request content as an iterable object of type XMLContent.Specifies that the value of the element is an encoded query on the specified table.Specifies that the value of the element maps to the specified field in the specified table.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 6
breadcrumb: [Encryption rule objects and APIs, Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# POST and URL parameter APIs

POST and URL parameters can be accessed as properties of the request object using `request.postParams` and `request.urlParams`.

Any single parameter can be accessed as a property of the postParams and urlParams parent objects by calling `request.postParams.myParam`. Any parameter accessed this way is an object of the underlying class ParameterValue. Any APIs in this class can be called on any parameter.

After [inspecting the client request](../task/request-type.md), it may be necessary to access and encrypt parameter values from the request object. Depending on the data in the client request, you can encrypt values and map them to fields on the instance in multiple ways.

## Encrypt the value of a known table and field

If you know the name of the instance table and field that will hold the encrypted data, you can explicitly define them in the encryption rule. For example, you may know that the request will be processed on the instance to create an incident and you want to encrypt the **text** parameter in the description field. In this case, you can create the following action.

```
function SampleAction1() { 
    request.postParams.text.valueFor('incident', 'description');
}
```

## Encrypt the value of a dynamically defined table and field

If, conversely, you do not know the name of the field that the encrypted data will populate, you can dynamically define them using **tableName** and **fieldName**.

The below example processes a generic request that might store data in different task tables \(such as incident, problem, and change\_request\) on the instance.

```
function SampleAction2() {
    var tableName = request.urlParams.table;  
    for (var parameter in request.postParams) {   
        var currentParam = request.postParams[parameter];
        var fieldName = currentParam.toString();
        if (fieldName == 'text') {
            currentParam.valueFor(tableName, 'description') 
        } else {
            currentParam.valueFor(tableName, fieldName);
        }
    }
}
```

This action:

-   Gets the destination table from the URL parameters.
-   Iterates over the URL parameters.
-   Asks the Edge Encryption proxy server to encrypt any URL parameter with a name that matches a field marked for encryption.
-   Looks for a specific parameter called text and asks the Edge Encryption proxy to encrypt the value based on the encryption configuration for the description field on the incident table.

In this example, the [valueFor\(\)](c_XMLElementAPI.md#) method is not actually performing any encryption. Rather, the method asks the Edge Encryption proxy server to check whether the table/field pair in the request object is marked for encryption with an encryption configuration and, if applicable, encrypt it.

## Encrypt JSON or XML within a parameter

A POST or URL parameter might include JSON or XML content. In this case, you can process the content within the parameter, iterate over the values, and encrypt required fields. In this example, the **tableName** is still accessed from a POST parameter, but the value of the field is the JSON object **data**.

```
function SampleAction3() {
    var tableName = request.postParams.table;
    var data = request.postParams.data;
    var dataIterator = data.getAsJsonContent().iterator();
    while (dataIterator.hasNext()) {
        var jsonElement = dataIterator.next();
        var fieldName = jsonElement.getName();
        if (fieldName == 'text') {
            jsonElement.valueFor(tableName, 'description');
        } else {
            jsonElement.valueFor(tableName, fieldName);
        }   
    }
}
```

An example of an encryption rule action that processes XML within a POST parameter.

```
function SampleAction4() {
    var tableName = request.postParams.table;
    var data = request.postParams.data;
    var dataIterator = data.getAsXmlContent().getIteratorOverAllChildren();
    while (dataIterator.hasNext()) {
        var jsonElement = dataIterator.next();
        var fieldName = jsonElement.getName();
        if (fieldName == 'text') {
            jsonElement.valueFor(tableName, 'description');
        } else {
            jsonElement.valueFor(tableName, fieldName);
        }   
    }
}
```

## Encrypt a query

You might encounter an encoded query within a parameter in the client request that contains sensitive data. To match a field in a query to an encrypted value in the instance database, you must create an encryption rule that asks the proxy to check whether a field in the query is marked for encryption. The [encodedQueryFor\(\)](c_XMLElementAPI.md#) method parses an encoded query on a given table, and checks if any fields in the query have encryption configurations.

In this example, the rule iterates over the parameters looking for the **filter** parameter, which is expected to be a Glide encoded query.

```
function SampleAction5() {
    var tableName = request.urlParams.table;
    for (var parameter in request.postParams) {
        var currentParam = request.postParams[parameter];
        var fieldName = currentParam.toString();
        if (fieldName == 'filter') {
            currentParam.encodedQueryFor(tableName);
        } else {
            currentParam.valueFor(tableName, fieldName);
        }
    }
}
```

For example, if the value of **filter** is: `short_description=My sensitive information^number=INC000056^category=Outage`, the query would become `short_description=<Encrypted(My sensitive information)>^number=INC000056^category=Outage` on the instance.

**Parent Topic:**[Encryption rule objects and APIs](api-overview.md)

## ParameterValue - toString\(\)

Converts the POST or URL parameter value to a string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The parameter value as a string.|

## ParameterValue - getAsJsonContent\(\)

Returns the request as an iterable object of type JsonNode.

This method is available only in an Edge Encryption rule if the request body is a valid JSON payload. If you are not sure what format the request body includes, check the contentType field on the request object.

Once the request is returned as a JsonNode object, you can use the [JSON APIs](json-overview.md) to iterate over the object and encrypt fields.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|JsonNode|The request as an iterable JsonNode.|

## ParameterValue - getAsXmlContent\(\)

Returns the request content as an iterable object of type XMLContent.

This method is available only in an Edge Encryption rule. This method assumes that the request body is a valid XML payload. You can check the contentType to make sure.

Once the request is returned as an XMLContent object, you can use the [XML APIs](xml-overview.md) to iterate over the object and encrypt fields.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLContent|The request as an iterable object of type XMLContent.|

## ParameterValue - encodedQueryFor\(String tableName\)

Specifies that the value of the element is an encoded query on the specified table.

Calling this function on a parameter tells the proxy that the value of the parameter is an [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for the specified table. The proxy parses the encoded query and encrypts the fields in the encoded query that must be encrypted.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table that you expect the query to run on.|

|Type|Description|
|----|-----------|
|void| |

## ParameterValue - valueFor\(String tableName, String fieldName\)

Specifies that the value of the element maps to the specified field in the specified table.

Calling this method on an element value tells the proxy that the value for this element maps to the specified field in the specified table. The proxy then checks if the field must be encrypted.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table name.|
|fieldName|String|The field name.|

|Type|Description|
|----|-----------|
|void| |

