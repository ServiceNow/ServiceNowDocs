---
title: NotifyClient - Client
description: The NotifyClient API provides methods that enable you to use Notify telephony functionality, such as making and receiving calls from a web browser.Instantiates a new Notify WebRTC Client object.Registers an event handler to listen for changes in a Notify client.Calls the specified phone number or the phone number associated with a specified user.Kills the current Notify client, rendering it unusable.Forwards an ongoing incoming or outgoing phone call to either a different phone number or a different WebRTC client.Returns a list of clients available to accept calls.Returns the parent call identifier for a specified call identifier, if one exists.Returns the normalized status of the current call.End the current call.Initializes the client driver.Mute or unmute the current client.Answers and connects to an incoming call from a WebRTC client.Send one or more DTMF-valid digits over the current call.Sets the caller ID for the current client session.Sets the availability of an active WebRTC client agent.
locale: en-US
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# NotifyClient- Client

The NotifyClient API provides methods that enable you to use Notify telephony functionality, such as making and receiving calls from a web browser.

Several NotifyClient methods take a callback function as a parameter. Because NotifyClient method calls are made asynchronously, these methods can't return a value directly. Use the callback function to parse the returned data, such as by assigning variables or making other API calls.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## NotifyClient - Client\(Object notifyConfig, Boolean initializeVendorClientLazily\)

Instantiates a new Notify WebRTC Client object.

<table id="table_iv3_kht_tr" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

initializeVendorClientLazily

</td><td>

Boolean

</td><td>

Flag that indicates whether to use the autoSelectVendorCallback function passed in the setCallerId\(\) method to automatically set the caller's associated vendor \(**notifyConfig.vendor** does not need to be defined in the constructor\).-   false: Default. Do not use the autoSelectVendorCallback function to set the caller's vendor. The vendor must be set in the constructor.
-   true: Use the autoSelectVendorCallback function to define the vendor when the caller ID is set.

</td></tr><tr><td>

notifyConfig

</td><td>

Object

</td><td>

JSON object that contains the configuration settings for the Notify WebRTC Client.

</td></tr><tr><td>

notifyConfig.autoLoadScriptResources

</td><td>

Boolean

</td><td>

Flag that indicates how to load the core JS library needed by the vendor client.-   false: Default. Use vendor specific codes to load the required vendor JS library \(enables backwards compatibility\).
-   true: Use notifyClient.js to load the core JS library.

</td></tr><tr><td>

notifyConfig.callerId

</td><td>

Number

</td><td>

Registered Notify number to use. Do not directly set this value. Use the method notifyClient.setCallerID\(\) to set this value.

</td></tr><tr><td>

notifyConfig.forceRefreshToken

</td><td>

Boolean

</td><td>

Flag that indicates whether to auto-renew expired client tokens.-   false: Do not automatically renew client tokens when they expire.
-   true: Default. Automatically renew client tokens when they expire.

</td></tr><tr><td>

notifyConfig.skipParentId

</td><td>

Boolean

</td><td>

Flag that indicates whether to immediately invoke the onIncoming caller for incoming calls.-   false: Default. Do not immediately invoke the onIncoming event handler.
-   true: Immediately invoke the onIncoming event handler. By setting this flag, if there is another call, where the `<Dial><Client>` Twiml caused the incoming call, then setting this flag causes the system to auto poll the backend. This auto poll obtains the parent notify\_call reference.

</td></tr><tr><td>

notifyConfig.vendor

</td><td>

Constant

</td><td>

Vendor to which the caller belongs.-   SNC.Notify.Vendor.TWILIO\_DIRECT
-   SNC.Notify.Vendor.TWILIO \(older, deprecated Twilio driver\)

</td></tr></tbody>
</table>The following example shows how to create the NotifyClient constructor, register various event listeners, and initialize the client driver.

```
jQuery(function () {

  var notifyConfig = {
    autoLoadScriptResources: true // This will take care of auto loading the JS resources needed by the client (if any)
  };
  var client = new SNC.Notify.Client(notifyConfig, true); // The second argument ensures that the proper vendor for the given number is auto determined
  client.setCallerId('valid_notify_long_number', function () {
    // This is called after the vendor has been determined.

    if (!notifyConfig.vendor) // Means this number has no compatible vendor
      return;

    client.addEventListener(SNC.Notify.STD_EVENTS.ONLINE, function () {
      // Ability to call is available
    });
    client.addEventListener(SNC.Notify.STD_EVENTS.OFFLINE, function () {
      // Ability to call is _not_ available right now
    });
    client.addEventListener(SNC.Notify.STD_EVENTS.ERROR, function (msg, code) {
      // Some error happened
    });
      //... register other event handlers here
      //Show UI elements which can be used to invoke client.call() and other APIs
    client.init(); // This is important to call this.
    });
});
```

## NotifyClient - addEventListener\(String event, Function fn\)

Registers an event handler to listen for changes in a Notify client.

Using this method you can register multiple listeners. Each listener must be a separate method call.

<table id="table_f1j_llh_wfb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

event

</td><td>

String

</td><td>

Name of the event to listen for. Instead of passing strings, use the constants defined in `SNC.Notify.STD_EVENTS`.

 -   CALL\_START: call has started and is in progress.
-   CALL\_CANCEL: caller canceled the call.
-   CALL\_INIT: WebRTC connected to a call \(incoming or outgoing\).
-   CALL\_DISCONNECT: current call has been disconnected.
-   ERROR: Error occurred. Parameters: `message(string), errCode(string)`
    -   `message`: error message to display.
    -   `errCode`: Optional. Associated error code.
-   INCOMING\_CALL: Call is coming in. Parameters: `from(string), to(string), callId(string), parentId(string), sysId(string), isFromClient(boolean)`
    -   `from`: caller's phone number.
    -   `to`: called phone number.
    -   `callId`: SID of the call.
    -   `parentId`: parent notify\_call reference. If skipParentId is set to true, this parameter should not be passed.
    -   `sysId`: WebRTC-to-WebRTC calls only. Unique identifier \(sys\_id\) of the caller.
    -   `isFromClient`: WebRTC-to-WebRTC calls only. Flag that indicates whether the call is from another WebRTC client.
-   CALL\_MUTE: client is muted.
-   CALL\_UNMUTE: client is unmuted.
-   OFFLINE: WebRTC session is not active.
-   ONLINE: WebRTC session is ready. Must be set after calling the init\(\) method.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Function|Function to use to de-register a listener.|

This example shows how to register multiple listeners.

```
jQuery(function () {

  var notifyConfig = {
    autoLoadScriptResources: true // This will take care of auto loading the JS resources needed by the client (if any)
  };
  var client = new SNC.Notify.Client(notifyConfig, true); // The second argument ensures that the proper client for the given number is auto determined
  client.setCallerId('valid_notify_long_number', function () {
    // This is called after the client has been determined.

    if (!notifyConfig.vendor) // Means this number has no compatible client
      return;

    client.addEventListener(SNC.Notify.STD_EVENTS.ONLINE, function () {
      // Ability to call is available
    });
    client.addEventListener(SNC.Notify.STD_EVENTS.OFFLINE, function () {
      // Ability to call is _not_ available right now
    });
    client.addEventListener(SNC.Notify.STD_EVENTS.ERROR, function (msg, code) {
      // Some error happened
    });
      //... register other event handlers here
     
    client.init(); // This is important to call this.
    });
});
```

This example shows how to de-register a listener.

```
var dereg = notifyClient.addEventListener(SNC.Notify.STD_EVENTS.ONLINE, function () {
 ... 
 }); 
 dereg(); 
  // The event listener function is no longer triggered.
```

## NotifyClient - call\(Object identifier\)

Calls the specified phone number or the phone number associated with a specified user.

**Note:** When checking the status of a call/connection, always compare against the constants provided by `SNC.Notify.Status`.

<table id="table_bbw_s3t_tr" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

identifier

</td><td>

Object

</td><td>

JSON object that contains either a phone number to call or the sys\_id of a WebRTC user. Passing a user sys\_id causes the call to be made through browser-to-browser communication.You can obtain the user sys\_id from the Notify WebRTC Session table.

 **Note:** If you provide both a phone number and user sys\_id, the method only uses the phone number.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example demonstrates passing a phone number as the function parameter.

```
notifyClient.call({
    phoneNumber: "+18001112223"
});
```

This example demonstrates passing a user record sys\_id as the function parameter.

```
notifyClient.call({
    userId: "6816f79cc0a8016401c5a33be04be441"
});
```

This example shows a button click handler.

```
$j("#pickupCallBtn").on("click", function() {
	notifyClient.hangupCall();
});
```

This example shows an event handler.

```
onConnect: function(status) {  
  // webRTC receives a call connection event (incoming or outgoing).
  if (status == SNC.Notify.Status.OPEN) {
    setStatus(getTimeStamp() + " -- Successfully established call");
    showHangupButton();
  }
},
```

## NotifyClient - destroy\(\)

Kills the current Notify client, rendering it unusable.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## NotifyClient - forwardCall\(Object argument\)

Forwards an ongoing incoming or outgoing phone call to either a different phone number or a different WebRTC client.

|Name|Type|Description|
|----|----|-----------|
|argument|Object|JSON object that contains the necessary information for forwarding the call to either a phone number or a WebRTC client \(user sys\_id\). You can obtain this sys\_id from the Notify WebRTC Session table.|

|Type|Description|
|----|-----------|
|void| |

This example demonstrates forwarding a call to a different phone number. The dtmf attribute allows you to send DTMF dial tones to the receiving number.

```
var arg = {
    type: "number",
    id: "+17012345678",
    dtmf: "1234"
}
client.forwardCall(arg);
```

This example demonstrates forwarding a call to a different Notify client.

```
var arg = {
    type: "userId",
    id: "6816f79cc0a8016401c5a33be04be441"
}
client.forwardCall(arg);
```

## NotifyClient - getAvailableClients\(Function callback\)

Returns a list of clients available to accept calls.

This method excludes the current client from the list. The equivalent [Notify-getAvailableClients\(\)](../../Notify/concept/c_NotifyAPI.md#) method does not filter any user.

<table id="table_xc5_skr_ls" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

callback

</td><td>

Function

</td><td>

Function to use to parse the list of clients. This function accepts a single parameter, an array of JSON objects with the following format:```
[{
    sys_id: "...",  // user's sys_id
    name: "..." // user's name
}]
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## NotifyClient - getParentId\(String callId, Function callback\)

Returns the parent call identifier for a specified call identifier, if one exists.

Depending on the telephony provider, there may be a delay before the parent call identifier is returned; therefore you must provide a callback function.

|Name|Type|Description|
|----|----|-----------|
|callId|String|Unique identifier of the call for which to return the parent call identifier.|
|callback|Function|Function that obtains the JSON object that contains either the parent call identifier or an error message if the identifier could not be obtained after several tries.|

|Type|Description|
|----|-----------|
|String|Parent call identifier.|

This example shows how to use this method to obtain the parent call identifier.

```
notifyClient.getParentId( callId, function(jsonObj) {} );
```

This example shows the contents of the jsonObj parameter.

```
{
	parentId: "xyz",
	error: "msg"
}
```

## NotifyClient - getStatus\(\)

Returns the normalized status of the current call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current status of the call. The values returned by the telephony provider API are normalized by replacing the returned driver value with its equivalent value as defined in SNC.Notify.Status.|

This example shows how to obtain the status of the current Notify client.

```
clientStatus = notifyClient.getStatus();
```

## NotifyClient - hangupCall\(\)

End the current call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example how to hang up a call.

```
$j("#pickupCallBtn").on("click", function() {
    notifyClient.hangupCall();
});
```

## NotifyClient - init\(\)

Initializes the client driver.

For example, when using the Twilio client, it invokes the method Twilio.Device.setup\(\). Call this method after the user has interacted with the page. This initialization process is asynchronous, therefore, you must provide an ONLINE event handler. This handler is called when the setup process is complete and the system is ready to take or make calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how to initialize the Notify client.

```
$j(function() {
  notifyClient = new SNC.Notify.Client( notifyConfig );
  notifyClient.setCallerId( '+31858889170' );
  notifyClient.init();
});
```

## NotifyClient - mute\(Boolean muted\)

Mute or unmute the current client.

<table id="table_mln_23t_tr" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

muted

</td><td>

Boolean

</td><td>

Mutes or unmutes the current call.-   false: \(or any non-true value\) unmutes the current call.
-   true: mutes the current call.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to send mute the current call.

```
notifyClient.mute( "true" );
```

## NotifyClient - pickupCall\(\)

Answers and connects to an incoming call from a WebRTC client.

Call this method when there is a notification of an incoming call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how to pickup a call.

```
$j("#pickupCallBtn").on("click", function() {
    notifyClient.pickupCall();
});
```

## NotifyClient - sendDtmf\(String digits\)

Send one or more DTMF-valid digits over the current call.

|Name|Type|Description|
|----|----|-----------|
|digits|String|One or more DTMF-valid digits.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to send DTMF signals to the current call.

```
notifyClient.SendDtmf( "1246AF" ) {} );
```

## NotifyClient - setCallerId\(String value, Function autoSelectVendorCallback\)

Sets the caller ID for the current client session.

You can change or update the caller ID at any time however, the caller ID must belong to the same vendor.

<table id="table_i54_w31_wfb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

value

</td><td>

String

</td><td>

Phone number to use to make and receive calls.

</td></tr><tr><td>

autoSelectVendorCallback

</td><td>

Function

</td><td>

**Optional.** **initializeVendorClientLazily** must be set to "true" in the constructor to use this function, otherwise an error is thrown. Name of the callback function to call once the vendor is automatically set for the specified phone number. With this option, the vendor does not need to be specified in the constructor \(**notifyConfig.vendor**\). Auto vendor selection is an asynchronous operation. Therefore, this callback is required to indicate when it is safe to call notifyConfig.init\(\), as this method requires that the vendor be set before it is called. In addition, you must also check if **notifyConfig.vendor** has been set in the callback to ensure that a vendor has been specified.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to set the caller ID. This example assumes that the vendor is set in the constructor.

```
$j(function() {
  notifyClient = new SNC.Notify.Client( notifyConfig );
  notifyClient.setCallerId( '+31858889170' );
  notifyClient.init();
});
```

## NotifyClient - setClientAvailable\(Boolean available\)

Sets the availability of an active WebRTC client agent.

This type of availability is different than an agent being in a call. In this case, an active WebRTC client may be connected and not on a call, but may not want to receive calls.

Calling this method updates the **Available** field value on the Notify Client Connected Session \[notify\_client\_session\] record associated with this client session. You can get a list of available clients using the getAvailableClients\(\) method.

<table id="table_ukv_kkr_ls" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

available

</td><td>

boolean

</td><td>

Flag that indicates whether an active WebRTC client wants to receive calls.-   false: client does not want to receive calls.
-   true: client does want to receive calls.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

