---
title: NotifyPhoneNumber - Global
description: The NotifyPhoneNumber API allows you to query information about a Notify phone number.Returns the international dialing code for a Notify phone number.Returns the ID of this phone number as defined by the telephony provider.Returns the numerical phone number for the current Notify caller.Returns the telephony provider associated with this phone number.Returns the country associated with the phone number.Determines whether the current Notify phone number is a short code.Determines if the Notify phone number supports conference calling.Determines if the Notify phone number supports receiving phone calls.Determines if the Notify phone number supports receiving SMS messages.Determines if the Notify phone number supports initiating phone calls.Determines if the Notify phone number supports sending SMS messages.Determines if the Notify phone number supports recording phone calls.Determines if the Notify phone number supports calls to a browser, such as in a WebRTC implementation.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NotifyPhoneNumber- Global

The NotifyPhoneNumber API allows you to query information about a Notify phone number.

Access the global NotifyPhoneNumber class and its associated methods in the `SNC` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## NotifyPhoneNumber - getDialCode\(\)

Returns the international dialing code for a Notify phone number.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|International phone code for a country.|

This example shows how to obtain the dial code for a phone number.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.getDialCode());
}
```

### Scoped equivalent

To use the getDialCode\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - getDialCode\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - getID\(\)

Returns the ID of this phone number as defined by the telephony provider.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Identifier of the number within the telephony provider.|

This example shows how to obtain the unique identifier for a phone number.

```
var numbers = SNC.NotifyScoped.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.getID());
}
```

### Scoped equivalent

To use the getID\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - getID\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - getNumber\(\)

Returns the numerical phone number for the current Notify caller.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|E.164-compliant phone number.|

This example shows how to obtain a Notify caller's phone number.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.getNumber());
}
```

### Scoped equivalent

To use the getNumber\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - getNumber\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - getOwner\(\)

Returns the telephony provider associated with this phone number.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Telephony provider associated with the number: Twilio.|

This example shows how to obtain the telephony provide that owns the specified phone number.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.getOwner());
}
```

### Scoped equivalent

To use the getOwner\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - getOwner\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - getTerritory\(\)

Returns the country associated with the phone number.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the country to which the phone number belongs.|

This example shows how to obtain the country of a Notify caller.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.getTerritory());
}
```

### Scoped equivalent

To use the getTerritory\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - getTerritory\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - isShortCode\(\)

Determines whether the current Notify phone number is a short code.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_mgj_csx_zfb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current Notify phone number is a short code.-   true: phone number is a short code.
-   false: phone number is not a short code.

</td></tr></tbody>
</table>This example shows how to check if the current Notify phone number is a short code.

```
GlideRecord notifyNumber = new GlideRecord(TABLE_NOTIFY_NUMBER);
notifyNumber.query(COL_NUMBER, notifyPhoneNumber.getNumber());

if (!notifyNumber.next()) {
  notifyNumber.initialize();
  notifyNumber.setValue(COL_OWNER, notifyPhoneNumber.getOwner());
  if (notifyPhoneNumber.isShortCode()) {
    notifyNumber.setValue(COL_SHORT_CODE, notifyPhoneNumber.getNumber());
  } else {
    notifyNumber.setValue(COL_PHONE_NUMBER, notifyPhoneNumber.getNumber());
  }
```

## NotifyPhoneNumber - supportsConferenceCall\(\)

Determines if the Notify phone number supports conference calling.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_dcj_qp4_wr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Value that indicates whether the Notify phone number supports conference calling.-   true: phone number does support conference calling
-   false: phone number does not support conference calling

</td></tr></tbody>
</table>This example shows how to determine if a Notify caller supports conference calls.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsConferenceCall());
}
```

### Scoped equivalent

To use the supportsConferenceCall\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - supportsConferenceCall\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - supportsIncomingPhoneCall\(\)

Determines if the Notify phone number supports receiving phone calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ull_np4_wr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Value that indicates whether the Notify phone number supports incoming phone calls.-   true: phone number does support incoming phone calls
-   false: phone number does not support incoming phone calls

</td></tr></tbody>
</table>This example shows how to determine if a Notify caller can receive incoming phone calls.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsIncomingPhoneCall());
}
```

### Scoped equivalent

To use the supportsIncomingPhoneCall\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - supportsIncomingPhoneCall\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - supportsIncomingSMS\(\)

Determines if the Notify phone number supports receiving SMS messages.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_x1k_rp4_wr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Value that indicates whether the Notify phone number supports receiving incoming MMS messages. -   true: phone number does support receiving incoming MMS messages
-   false: phone number does not support receiving incoming MMS messages

</td></tr></tbody>
</table>This example shows how to determine if a Notify caller can receive incoming SMS messages.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsIncomingSMS());
}
```

### Scoped equivalent

To use the supportsIncomingSMS\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - supportsIncomingSMS\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - supportsOutgoingPhoneCall\(\)

Determines if the Notify phone number supports initiating phone calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_n5l_4p4_wr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Value that indicates whether the Notify phone number supports initiating outgoing phone calls.-   true: phone number does support initiating outgoing phone calls
-   false: phone number does not support initiating outgoing phone calls

</td></tr></tbody>
</table>This example shows how to determine if a Notify caller can make outgoing phone calls.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsOutgoingPhoneCall());
}
```

### Scoped equivalent

To use the supportsOutgoingPhoneCall\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - supportsOutgoingPhoneCall\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - supportsOutgoingSMS\(\)

Determines if the Notify phone number supports sending SMS messages.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_hv1_tp4_wr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Value that indicates whether the Notify phone number supports sending SMS messages.-   true: phone number does support sending SMS messages
-   false: phone number does not support sending SMS messages

</td></tr></tbody>
</table>This example shows how to determine if a Notify caller can initiate outgoing SMS messages.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsOutgoingSMS());
}
```

### Scoped equivalent

To use the supportsOutgoingSMS\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - supportsOutgoingSMS\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - supportsRecording\(\)

Determines if the Notify phone number supports recording phone calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_gzm_wp4_wr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Value that indicates whether the Notify phone number supports recording phone calls.-   true: phone number does support recording phone calls
-   false: phone number does not support recording phone calls

</td></tr></tbody>
</table>This example shows how to determine if a Notify caller can record calls.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsRecording());
}
```

### Scoped equivalent

To use the supportsRecording\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - supportsRecording\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

## NotifyPhoneNumber - supportsWebRTC\(\)

Determines if the Notify phone number supports calls to a browser, such as in a WebRTC implementation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_lfq_vp4_wr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Value that indicates whether the Notify phone number supports calls to a browser.-   true: phone number does support calls to a browser
-   false: phone number does not support calls to a browser

</td></tr></tbody>
</table>This example shows how to determine if a Notify caller can initiate/accept browser-to-browser calls.

```
var numbers = SNC.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsWebRTC());
}
```

### Scoped equivalent

To use the supportsWebRTC\(\) method in a scoped application, use the corresponding scoped method: [Scoped NotifyPhoneNumber - supportsWebRTC\(\)](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#).

