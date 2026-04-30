---
title: NotifyPhoneNumber - Scoped
description: The NotifyPhoneNumber API allows you to query information about a Notify phone number.Returns the international dialing code for a Notify phone number.Returns the ID of this phone number as defined by the telephony provider.Returns the numerical phone number for the current Notify caller.Returns the telephony provider associated with this phone number.Returns the country associated with the phone number.Determines if the Notify phone number supports conference calls.Determines if the Notify phone number supports receiving phone calls.Determines if the Notify phone number supports receiving SMS messages.Determines if the Notify phone number supports initiating phone calls.Determines if the Notify phone number supports sending SMS messages.Determines if the Notify phone number supports recording phone calls.Determines if the Notify phone number supports calls to a browser, such as in a WebRTC implementation.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NotifyPhoneNumber- Scoped

The NotifyPhoneNumber API allows you to query information about a Notify phone number.

Execute the scoped NotifyPhoneNumber API and its associated methods in the `sn_notify` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped NotifyPhoneNumber - getDialCode\(\)

Returns the international dialing code for a Notify phone number.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|International phone code for a country.|

This example shows how to obtain the dial code for a phone number.

```
var numbers = sn_notify.NotifyScoped.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.getDialCode());
}
```

## Scoped NotifyPhoneNumber - getID\(\)

Returns the ID of this phone number as defined by the telephony provider.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Identifier of the number within the telephony provider.|

This example shows how to obtain the unique identifier for a phone number.

```
var numbers = sn_notify.NotifyScoped.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.getID());
}
```

## Scoped NotifyPhoneNumber - getNumber\(\)

Returns the numerical phone number for the current Notify caller.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|E.164-compliant phone number.|

This example shows how to obtain a Notify caller's phone number.

```
var numbers = sn_notify.NotifyScoped.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.getNumber());
}
```

## Scoped NotifyPhoneNumber - getOwner\(\)

Returns the telephony provider associated with this phone number.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Telephony provider associated with the number: Twilio.|

This example shows how to obtain the telephony provide that owns the specified phone number.

```
var numbers = sn_notify.NotifyScoped.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.getOwner());
}
```

## Scoped NotifyPhoneNumber - getTerritory\(\)

Returns the country associated with the phone number.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the country to which the phone number belongs.|

This example shows how to obtain the country of a Notify caller.

```
var numbers = sn_notify.NotifyScoped.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.getTerritory());
}
```

## Scoped NotifyPhoneNumber - supportsConferenceCall\(\)

Determines if the Notify phone number supports conference calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_sfg_jmv_bgb" class="returns"><thead><tr><th>

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
var numbers = sn_notify.NotifyScoped.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsConferenceCall());
}
```

## Scoped NotifyPhoneNumber - supportsIncomingPhoneCall\(\)

Determines if the Notify phone number supports receiving phone calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_xlt_lnv_bgb" class="returns"><thead><tr><th>

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
var numbers = sn_notify.NotifyScoped.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsIncomingPhoneCall());
}
```

## Scoped NotifyPhoneNumber - supportsIncomingSMS\(\)

Determines if the Notify phone number supports receiving SMS messages.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_mxf_x4v_bgb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Value that indicates whether the Notify phone number supports incoming SMS messages.-   true: phone number does support incoming SMS messages
-   false: phone number does not support incoming SMS messages

</td></tr></tbody>
</table>This example shows how to determine if a Notify caller can receive incoming SMS messages.

```
var numbers = sn_notify.NotifyScoped.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsIncomingSMS());
}
```

## Scoped NotifyPhoneNumber - supportsOutgoingPhoneCall\(\)

Determines if the Notify phone number supports initiating phone calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wkq_bqv_bgb" class="returns"><thead><tr><th>

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
var numbers = sn_notfy.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsOutgoingPhoneCall());
}
```

## Scoped NotifyPhoneNumber - supportsOutgoingSMS\(\)

Determines if the Notify phone number supports sending SMS messages.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qct_srv_bgb" class="returns"><thead><tr><th>

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
var numbers = sn_notify.NotifyScoped.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsOutgoingSMS());
}
```

## Scoped NotifyPhoneNumber - supportsRecording\(\)

Determines if the Notify phone number supports recording phone calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rxv_5sv_bgb" class="returns"><thead><tr><th>

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
var numbers = sn_notify.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsRecording());
}
```

## Scoped NotifyPhoneNumber - supportsWebRTC\(\)

Determines if the Notify phone number supports calls to a browser, such as in a WebRTC implementation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_lnk_vtv_bgb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Value that indicates whether the Notify phone number supports browser-to-browser \(WebRTC\) calls.-   true: phone number does support browser-to-browser \(WebRTC\) calls
-   false: phone number does not support browser-to-browser \(WebRTC\) calls

</td></tr></tbody>
</table>This example shows how to determine if a Notify caller can initiate/accept browser-to-browser calls.

```
var numbers = sn_notify.Notify.getPhoneNumbers();
 
// Here numbers is of type List
if (numbers.size() > 0) {
   var number = numbers.get(0);
 
   // Here number is of type NotifyPhoneNumber
  gs.info(number.supportsWebRTC());
}
```

