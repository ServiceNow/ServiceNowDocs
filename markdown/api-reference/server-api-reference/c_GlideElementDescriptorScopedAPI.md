---
title: GlideElementDescriptor - Scoped, Global
description: The GlideElementDescriptor API provides information about individual fields in a glide record.Returns the encryption type used for attachments on the element's table.Returns the element's encryption type.Returns the element's internal data type.Returns the element's label.Returns the element's length.Returns the element's name.Returns the element's plural label.Returns true if an encrypted attachment has been added to the table.Returns true if the element is an automatically generated or system field.Returns true if the element is defined as a dropdown choice in its dictionary definition.Returns true if an element is encrypted.Returns whether the field represented by this descriptor is configured for field encryption.Determines whether the element is mandatory and must contain a value before the record can be saved.Returns true if the element is a virtual element.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideElementDescriptor - Scoped, Global

The GlideElementDescriptor API provides information about individual fields in a glide record.

There is no constructor for this class. Use the GlideElement or GlideRecord getED\(\) method to obtain a GlideElementDescriptor object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideElementDescriptor - getAttachmentEncryptionType\(\)

Returns the encryption type used for attachments on the element's table.

This method is for use with the Edge Encryption plugin.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The encryption type used on attachments. Returns null if attachments on the element's table are not being encrypted.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');

var field = grInc.getElement('priority');
var ed = field.getED();

var isEdge = ed.getAttachmentEncryptionType();
gs.info(isEdge);

```

Output:

```
null
```

## GlideElementDescriptor - getEncryptionType\(\)

Returns the element's encryption type.

This method is for use with the Edge Encryption plugin.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The element's encryption type. Returns null if the element is not encrypted.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');

var field = grInc.getElement('priority');
var ed = field.getED();

sEdge = ed.getEncryptionType();
gs.info(isEdge);
```

Output:

```
null
```

## GlideElementDescriptor - getInternalType\(\)

Returns the element's internal data type.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_scc_gv3_yr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The element's internal data type.Possible values:

-   boolean
-   char
-   collection
-   conditions
-   date
-   decimal
-   documentation\_field
-   domain\_id
-   due\_date
-   email
-   field\_name
-   file\_attachment
-   float
-   glide\_date
-   glide\_date\_time
-   glide\_duration
-   glide\_list
-   GUID
-   html
-   image
-   integer
-   long
-   longint
-   multi\_two\_lines
-   journal
-   journal\_input
-   numeric
-   order\_index
-   password
-   ph\_number
-   reference
-   script
-   script\_plain
-   string
-   sys\_class\_name
-   table\_name
-   template\_value
-   timer
-   translated\_field
-   url
-   user\_image
-   user\_input
-   user\_roles
-   video
-   workflow

</td></tr></tbody>
</table>```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');
 
var field = grInc.getElement('priority');
var ed = field.getED();
 
var isEdge = ed.getInternalType();
gs.info(isEdge);
```

Output:

```
integer
```

## GlideElementDescriptor - getLabel\(\)

Returns the element's label.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The element's label.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');
 
var field = grInc.getElement('priority');
var ed = field.getED();
 
var isEdge = ed.getLabel();
gs.info(isEdge);
```

Output:

```
Priority
```

## GlideElementDescriptor - getLength\(\)

Returns the element's length.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The element's size.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');
 
var field = grInc.getElement('priority');
var ed = field.getED();
 
var isEdge = ed.getLength();
gs.info(isEdge);
```

Output:

```
40
```

## GlideElementDescriptor - getName\(\)

Returns the element's name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The element's name.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');
 
var field = grInc.getElement('priority');
var ed = field.getED();
 
var isEdge = ed.getName();
gs.info(isEdge);
```

Output:

```
priority
```

## GlideElementDescriptor - getPlural\(\)

Returns the element's plural label.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The element's plural label.|

```
var now_GR = new GlideRecord('incident');
now_GR.query();
var ed = now_GR.getED();
gs.info(ed.getPlural());
```

Output:

```
Incidents
```

## GlideElementDescriptor - hasAttachmentsEncrypted\(\)

Returns true if an encrypted attachment has been added to the table.

This method is for use with the Edge Encryption plugin.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if an encrypted attachment has been added to the table.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');

var field = grInc.getElement('priority');
var ed = field.getED();

var isEdge = ed.hasAttachmentsEncrypted();
gs.info(isEdge);
```

Output:

```
false
```

## GlideElementDescriptor - isAutoOrSysID\(\)

Returns true if the element is an automatically generated or system field.

Automatically generated and system fields cannot be encrypted. This method is for use with the Edge Encryption plugin.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the element is automatically generated or a system field.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');
var field = grInc.getElement('priority');
var ed = field.getED();

isEdge = ed.isAutoOrSysID();
gs.info(isEdge);

```

Output:

```
false
```

## GlideElementDescriptor - isChoiceTable\(\)

Returns true if the element is defined as a dropdown choice in its dictionary definition.

Choice fields cannnot be encrypted.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if the element is defined as a dropdown choice. Returns true even if there are no entries defined in the choice table. The last choice type, suggestion, does not return true.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');

var field = grInc.getElement('priority');
var ed = field.getED();

var isChoiceTable = ed.isChoiceTable();
gs.info(isChoiceTable);
```

Output:

```
true
```

## GlideElementDescriptor - isEdgeEncrypted\(\)

Returns true if an element is encrypted.

This method is for use with the Edge Encryption plugin.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if the element is encrypted, false otherwise.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');

var field = grInc.getElement('priority');
var ed = field.getED();

var isEdge = ed.isEdgeEncrypted();
gs.info(isEdge)
```

Output:

```
false
```

## GlideElementDescriptor - isEncrypted\(\)

Returns whether the field represented by this descriptor is configured for field encryption.

Use this method to programmatically detect encrypted fields before reading or writing sensitive data, or to enforce access policies based on a field's encryption status.

Required plugins: Field Encryption Starter \(com.glide.field.encryption.starter\). Without this plugin, isEncrypted\(\) returns false.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_kx1_tmp_z3c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the field is configured for field encryption.

 Valid values:

-   true: Field is configured for field encryption.
-   false: Field isn't encrypted, or the Field Encryption Starter \(com.glide.field.encryption.starter\) plugin isn't active.

</td></tr></tbody>
</table>The following server-side script uses isEncrypted\(\) to check whether the short\_description field on the Incident table is encrypted before logging its value. Copy this into a Background Script or Business Rule on your instance to test.

**Note:** Use the [GlideRecord - getED\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#) or [Scoped GlideElement - getED\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#) method to obtain a GlideElementDescriptor object.

```
// Retrieve a sample Incident record
var gr = new GlideRecord('incident');
gr.setLimit(1);
gr.query();

if (gr.next()) {
    // Get the GlideElement for the field you want to inspect
    var element = gr.getElement('short_description');

    // Retrieve the descriptor from the element
    var descriptor = element.getED();

    // Check whether the field is configured for Field Encryption
    if (descriptor.isEncrypted()) {
        gs.info('short_description is encrypted. Value: ' + element.getDisplayValue());
    } else {
        gs.info('short_description is NOT encrypted. Value: ' + gr.getValue('short_description'));
    }
}
```

Output \(unencrypted\):

```
short_description is NOT encrypted. Value: Unable to connect to network
```

Output \(encryption enabled on the field\):

```
short_description is encrypted. Value: Unable to connect to network
```

## GlideElementDescriptor - isMandatory\(\)

Determines whether the element is mandatory and must contain a value before the record can be saved.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_yxq_xwv_shb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the associated element is mandatory and must contain a value before the record containing the element can be saved.Possible values:

-   true: element must contain a value; mandatory field
-   false: element does not have to contain a value

</td></tr></tbody>
</table>This example shows how to check whether the name field is mandatory.

```
var isRecordValid;
var now_GR = new GlideRecord('my_table');
var field = now_GR.getElement('name');
var elementDescriptor = field.getED();
now_GR.query();
while (now_GR.next()) {
if (elementDescriptor.isMandatory() && !now_GR.name) {
       isRecordValid = false;
  }
}
```

## GlideElementDescriptor - isVirtual\(\)

Returns true if the element is a virtual element.

A virtual element is a calculated field as set by the dictionary definition of the field. Virtual fields cannot be encrypted.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if the element is a virtual element.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');

var field = grInc.getElement('priority');
var ed = field.getED();

var isVirtual = ed.isVirtual();
gs.info(isVirtual);
```

Output:

```
false
```

