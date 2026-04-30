---
title: XML APIs
description: XML APIs can be used after calling getAsXmlContent\(\) on either the request object or a ParameterValue property.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Encryption rule objects and APIs, Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# XML APIs

XML APIs can be used after calling getAsXmlContent\(\) on either the request object or a ParameterValue property.

When using XML APIs to write your encryption rule, you can follow a general format:

1.  Call getAsXmlContent\(\) on the request object or ParameterValue property. This returns an iterable object of the XMLContent underlying class.
2.  Call getIterator\(\) or getIterator\(String xPath\) on the XMLContent object. This returns an XMLElementIterator object that can be used to iterate over XML elements.
3.  Call the hasNext\(\) method on the XMLElementIterator object to determine whether another element is available.
4.  Call next\(\) on the XMLElementIterator object to return the next XML element. You cannot call next\(\) without first calling hasNext\(\).
5.  Call valueFor\(String tableName, String fieldName\) on the XML element. This method tells the proxy that the value for this element maps to the specified field in the specified table. The proxy then checks if the field must be encrypted.

    **Note:** To determine if you want to call valueFor\(String tableName, String fieldName\) on an XML element, you can use the getName\(\) method to return the name of the element.


## Mapping to a known table-field on the instance

In this example, the XML payload will be processed on the instance to insert records in the incident table. The description field will populate short\_description on the incident.

```
<data>
    <record>
        <name>'Test Record 1'</name>
        <description>'Test Record 1 Description'</description>
        <tag>critical</tag>
    </record>
    <record>
        <name>'Test Record 2'</name>
        <description>'Test Record 2 Description'</description>
        <tag>security</tag>
    </record>
</data>
```

The following encryption rule action can apply:

```
function sampleXmlAction1() {
    var xmlContent = request.getAsXmlContent();
    // This loop iterates over all description tags that match the given path
    var xmlElementIterator = xmlContent.getIterator('data/record/description');    
    while (xmlElementIterator.hasNext()) {
        var xmlElement = xmlElementIterator.next();
        xmlElement.valueFor('incident', 'short_decription');
    }
}
```

This action iterates through the **description** tags and asks the proxy server to encrypt the values and insert them into incident.short\_description on the instance.

**Note:** This rule finds all **description** tags within all **record** tags in the XML payload. If there is only one occurrence of a tag to encrypt, the rule still uses the xPath and iterator structure. However, it iterates only once in the loop.

## Mapping to an unknown table-field on the instance

In this example, the rule iterates over the **record** tags, but does not know what tags to expect within the **record** tag. The only known is that the tags within the **record** tags match the names of the columns specified in the table URL parameter.

The rule also specifies that, if the table is incident, then the data in the **description** tag should be encrypted and stored in the short\_description field on the instance.

```
function sampleXmlAction2() {
    var xmlContent = request.getAsXmlContent();
    var tableName = request.urlParam.table;
    // This first iterator will iterate over all record elements
    var xmlElementIterator = xmlContent.getIterator('data/record');
    while (xmlElementIterator.hasNext()) {
        encryptFieldsInRecord(xmlElementIterator.next());
    }
}
function encryptFieldsInRecord(xmlElement) {
    //Then, iterate over all tags representing fields in the table
    var fieldIterator = xmlElement.getIteratorOverAllChildren();
    while (fieldIterator.hasNext()) {
        var field = fieldIterator.next();
        var fieldName = childElement.getName();
        //if table is incident, then description is encrypted for the short_description field
        if (tableName == 'incident' && fieldName == 'description') {
            field.valueFor(tableName, 'short_description');
        } else {
            //if table is not incident, ask the proxy to check if the given field is encrypted for the given table
            field.valueFor(tableName, fieldName);
        }
    }
}
```

In the encryptFieldsInRecord\(\) function, the valueFor\(\) method is called on a table and a field that are dynamically assigned based on the request. Even though the table and field names can change, the rule asks the proxy to check whether the field in the table must be encrypted based on the encryption configurations defined.

If the field is not configured for encryption, or if the tag does not match a field in the table, the proxy skips that tag. If the tag matches a field marked for encryption, then the Edge Encryption proxy server encrypts the value.

## Using an encoded query

In this example, all tags have the **filter** attribute, which indicates whether the tag contains an encoded query.

```
<data>
    <record>
        <name filter="false">'Test Record 1'</name>
        <description filter="false">'Test Record 1 Description'</description>
        <query filter="true">category=1^name=edge</query>
    </record>
    <record>
        <name filter="false">'Test Record 2'</name>
        <description filter="false">'Test Record 2 Description'</description>
        <query filter="true">category=2^severity=3</query>
   </record>
</data>
```

The following encryption rule action can apply:

```
function sampleXmlAction3() {
   var xmlContent = request.getAsXmlContent();
   var tableName = request.urlParam.table;
   // This first iterator will iterate over all record elements
   var xmlElementIterator = xmlContent.getIterator('data/record');
   while (xmlElementIterator.hasNext()) {
       encryptFieldsInRecord(xmlElementIterator.next());
   }
}
function encryptFieldsInRecord(xmlElement) {
   //this time we want to iterate over all tags representing fields in the table
   var fieldIterator = xmlElement.getIteratorOverAllChildren();
   while (fieldIterator.hasNext()) {
       var field = fieldIterator.next();
       var fieldname = childElement.getName();
       //let's look at the filter attribute, if true, then encrypt as encoded query
       if (field.getAttributeValue('filter') == 'true') {
           field.encodedQueryFor(tableName);
       } else {
           //if it is false then check if the field should be encrypted
           field.valueFor(tableName, fieldName);
       }
   }
}
```

If the **filter** attribute value is true, the rule asks the proxy server to encrypt the values in the encoded query. If false, the rule asks the proxy to check whether the field should be encrypted.

-   **[XMLContent](c_XMLContentAPI.md#)**  
A global object that provides methods to iterate over the XML content.
-   **[XMLElementIterator](c_XMLElementIteratorAPI.md#)**  
Provides methods for iterating over XML elements.
-   **[XMLElement](c_XMLElementAPI.md#)**  
Provides methods for iterating through XML elements and mapping values to fields in a table.

**Parent Topic:**[Encryption rule objects and APIs](api-overview.md)

