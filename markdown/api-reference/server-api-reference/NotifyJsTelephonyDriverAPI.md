---
title: NotifyJsTelephonyDriver - Global
description: The NotifyJsTelephonyDriver API provides methods that you can use to obtain information about the capabilities of the associated telephony driver.Calls a specified telephone number.Returns a list of the capabilities of the telephony driver.Returns the maximum number of telephone numbers to which the telephony driver associated with the passed in Notify telephone number can send an SMS message to at one time.Returns the Notify phone number record for the specified phone number.Returns a list of all Notify telephone numbers associated with the current telephony driver.Checks whether the current telephony driver is active.Removes the specified caller from the current Notify conference call.Mutes the specified caller in the current Notify conference call.Sends the specified Short Message Service \(SMS\) message to the specified list of telephone numbers.Sends a specified Short Message Service \(SMS\) message to a specified telephone number.Checks whether the specified Notify telephone number is capable of handling autonomous bulk Short Message Service \(SMS\) messages.Checks whether the current telephony driver is capable of handling telephone calls.Checks whether the specified Notify telephone number is capable of calls to a browser using WebRTC \(Real-Time Communications.\)Checks whether the current telephony driver is capable of handling Short Message Service \(SMS\) messages.Unmutes the specified caller in the current Notify conference call.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NotifyJsTelephonyDriver- Global

The NotifyJsTelephonyDriver API provides methods that you can use to obtain information about the capabilities of the associated telephony driver.

It is a scripted extension point that can only be used when its object is returned by another method, such as NotifyUtil - getTelephonyDriverFromNotifyNumber\(\). You cannot call this API directly. The calling method associates a specific driver to the interface, abstracting the details of determining the driver. Each of the available drivers implement the same interface, which is defined by the NotifyJsTelephonyDriver API.

In the following code example, the getTelephonyDriverFromNotifyNumber\(\) method returns an implementation of this API, with the driver interface being determined by the passed in telephone number, such as TwilioNotifyJsTelephonyDriver.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      return {
        driverName: driver.getName(),
        supportsCall: driver.supportsCall(),
        supportsSMS: driver.supportsSms()
      } 
    }
} 
```

To see which drivers are associated with the NotifyJsTelephonyDriver extension point, navigate to **System Extension Points**&gt;**global.NotifyJsTelephonyDriver**. All associated driver implementations appear in the **Implementations** tab.

For additional information on scripted extension points, see [Using extension points to extend application functionality point](../../../../../build/applications/concept/extension-points.md).

To use this API you must activate the Notify \(com.snc.notify\) plugin. To activate specific driver implementations, such as Twillo, you must activate their specific plugin.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## NotifyJsTelephonyDriver - call\(Object notifyPhoneNumber, String phoneNumber\)

Calls a specified telephone number.

<table id="table_xcn_24y_qmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

notifyPhoneNumber

</td><td>

[NotifyPhoneNumber - Global](../../NotifyPhoneNumber/concept/c_NotifyPhoneNumberAPI.md#)

</td><td>

NotifyPhoneNumber record that contains the Notify phone number from which to make the call. Located in the Notify Phone Number \[notify\_number\] table.

</td></tr><tr><td>

toPhoneNumber

</td><td>

String

</td><td>

Telephone number to call.Format: E.164

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {

    }
} 
```

## NotifyJsTelephonyDriver - getCapabilities\(\)

Returns a list of the capabilities of the telephony driver.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

This example returns the capabilities of the associated telephony driver.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      return {
       capabilities: driver.getCapabilities()
      } 
    }
} 
```

## NotifyJsTelephonyDriver - getMaxSizeForBulkSms\(String phoneNumber\)

Returns the maximum number of telephone numbers to which the telephony driver associated with the passed in Notify telephone number can send an SMS message to at one time.

|Name|Type|Description|
|----|----|-----------|
|phoneNumber|String|Notify telephone number to check for the maximum number of telephone numbers that the associated driver is able to send to in one bulk SMS message.|

|Type|Description|
|----|-----------|
|Number|Maximum number of telephone numbers that an SMS message can be sent to in a single bulk SMS delivery.|

This example returns the maximum number of telephone numbers that can be sent to in a single bulk SMS message for the associated telephony driver.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
       return {
       maxSmsNumbers: driver.getMaxSizeForBulkSMS(notifyNumber)
      }       
    }
} 
```

## NotifyJsTelephonyDriver - getPhoneNumber\(String phoneNumber\)

Returns the Notify phone number record for the specified phone number.

Returns null if the specified phone number is not found in the Notify Phone Number \[notify\_number\] table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|NotifyPhoneNumberAPI|Notify phone number record associated with the specified telephone number.|

This example obtains the telephony driver and returns the associated Notify phone number record for a specified phone number.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      return {
       phoneNumberRecord: driver.getPhoneNumber(notifyNumber)
      } 
    }
} 
```

## NotifyJsTelephonyDriver - getPhoneNumbers\(\)

Returns a list of all Notify telephone numbers associated with the current telephony driver.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Comma-separated list of all Notify telephone numbers associated with the current driver.|

This example obtains the telephony driver and returns the list of Notify phone numbers associated with the current telephony driver.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      return {
       phoneNumbers: driver.getPhoneNumbers()
      } 
    }
} 
```

## NotifyJsTelephonyDriver - isActive\(\)

Checks whether the current telephony driver is active.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_iry_t5p_qmb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current telephony driver is active.

 Valid values:

-   true: Driver is active.
-   false: Driver is inactive.

</td></tr></tbody>
</table>This example obtains the telephony driver and returns whether the current telephony driver is active.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      return {
        active: driver.isActive()
      } 
    }
} 
```

## NotifyJsTelephonyDriver - kick\(GlideRecord participantRecord\)

Removes the specified caller from the current Notify conference call.

|Name|Type|Description|
|----|----|-----------|
|participantRecord|[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)|GlideRecord object containing the Notify Participant \[notify\_participant\] record of the caller to remove from the conference call.|

|Type|Description|
|----|-----------|
|String|Only returned if error. Error message that describes why the caller was not removed from the call.|

This example mutes the associated caller in the current conference call.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      var notifyParticipantGr = new GlideRecord('notify_participant');
      notifyParticipantGr.get('active participant sys id');
    
      if (notifyParticipantGr.isValid) {
        driver.kick(notifyParticipantGr)
    }
} 
```

## NotifyJsTelephonyDriver - mute\(GlideRecord participantRecord\)

Mutes the specified caller in the current Notify conference call.

|Name|Type|Description|
|----|----|-----------|
|participantRecord|[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)|GlideRecord object containing the Notify Participant \[notify\_participant\] record of the caller to mute in the conference call.|

|Type|Description|
|----|-----------|
|String|Only returned if error. Error message that describes why the caller was not muted.|

This example mutes the associated caller in the current conference call.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      var notifyParticipantGr = new GlideRecord('notify_participant');
      notifyParticipantGr.get('active participant sys id');
    
      if (notifyParticipantGr.isValid) {
        driver.mute(notifyParticipantGr)
    }
} 
```

## NotifyJsTelephonyDriver - sendAutonomousBulkSms\(Object notifyPhoneNumber, Array toPhoneNumber, String message, GlideRecord source\)

Sends the specified Short Message Service \(SMS\) message to the specified list of telephone numbers.

In addition, you can optionally associate the Incident record that caused the SMS message to be generated with the SMS message.

<table id="table_rwk_xvx_qmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

String

</td><td>

Message to send.

</td></tr><tr><td>

notifyPhoneNumber

</td><td>

[NotifyPhoneNumber - Global](../../NotifyPhoneNumber/concept/c_NotifyPhoneNumberAPI.md#)

</td><td>

Record that contains the phone number that is sending the bulk SMS message.

</td></tr><tr><td>

source

</td><td>

[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)

</td><td>

Optional. Incident GlideRecord to store in the Source field of the associated SMS message record in the Notify Message \[notify message\] table. This links the Incident record that caused the SMS message to be generated to that SMS message.Default: None. If this parameter is not passed in, this information is not tracked.

</td></tr><tr><td>

toPhoneNumbers

</td><td>

Array

</td><td>

List of telephone numbers of the devices to receive the SMS message.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to send an autonomous bulk SMS.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {

    }
} 
```

## NotifyJsTelephonyDriver - sendSMS\(NotifyPhoneNumber notifyPhoneNumber, String toPhoneNumber, String messageBody\)

Sends a specified Short Message Service \(SMS\) message to a specified telephone number.

<table id="table_ohm_jdr_qmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

notifyPhoneNumber

</td><td>

[NotifyPhoneNumber - Global](../../NotifyPhoneNumber/concept/c_NotifyPhoneNumberAPI.md#)

</td><td>

Notify phone number record that contains the telephone number that is sending the SMS message. Located in the Notify Phone Number \[notify\_number\] table.

</td></tr><tr><td>

toPhoneNumber

</td><td>

String

</td><td>

Phone number to send the SMS message to. Format: E.164 compliant

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Text to send in the SMS message.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example sends an SMS message to a specified telephone number.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
        
    }
} 
```

## NotifyJsTelephonyDriver - supportsAutonomousBulkSms\(String phoneNumber\)

Checks whether the specified Notify telephone number is capable of handling autonomous bulk Short Message Service \(SMS\) messages.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_vlw_3nq_qmb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified Notify telephone number supports autonomous bulk SMS.

 Valid values:

-   true: Supports autonomous bulk SMS.
-   false: Does not support autonomous bulk SMS.

</td></tr></tbody>
</table>This example obtains the telephony driver and returns whether the driver supports autonomous bulk SMS.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      return {
        supportsBulkSMS: driver.supportsAutonomousBulkSms(notifyNumber)
      } 
    }
} 
```

## NotifyJsTelephonyDriver - supportsCall\(\)

Checks whether the current telephony driver is capable of handling telephone calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_acf_3lq_qmb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current telephony driver supports telephone calls.

 Valid values:

-   true: Driver supports telephone calls.
-   false: Driver does not support telephone calls.

</td></tr></tbody>
</table>This example obtains the telephony driver and returns whether the driver supports telephone calls.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      return {
        supportsCall: driver.supportsCall()
      } 
    }
} 
```

## NotifyJsTelephonyDriver - supportsCallOverWebRtc\(\)

Checks whether the specified Notify telephone number is capable of calls to a browser using WebRTC \(Real-Time Communications.\)

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wgy_kcs_qmb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified Notify telephone number supports browser calls using WebRTC.

 Valid values:

-   true: Supports WebRTC.
-   false: Does not support WebRTC.

</td></tr></tbody>
</table>This example obtains the telephony driver and returns whether the driver supports browser calls using WebRTC.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      return {
        supportsWebRTC: driver.supportsCallOverWebRtc(notifyNumber)
      } 
    }
} 
```

## NotifyJsTelephonyDriver - supportsSMS\(\)

Checks whether the current telephony driver is capable of handling Short Message Service \(SMS\) messages.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wnl_cmq_qmb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current telephony driver supports SMS.

 Valid values:

-   true: Driver supports SMS.
-   false: Driver does not support SMS.

</td></tr></tbody>
</table>This example obtains the telephony driver and returns whether the driver supports SMS.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      return {
        supportsSMS: driver.supportsSMS()
      } 
    }
} 
```

## NotifyJsTelephonyDriver - unmute\(GlideRecord participantRecord\)

Unmutes the specified caller in the current Notify conference call.

|Name|Type|Description|
|----|----|-----------|
|participantRecord|[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)|GlideRecord object containing the Notify Participant \[notify\_participant\] record of the caller to mute in the conference call.|

|Type|Description|
|----|-----------|
|String|Only returned if error. Error message that describes why the caller was not muted.|

This example mutes the associated caller in the current conference call.

```
getDriverDetails('<notify_number>'); 

function getDriverDetails(notifyNumber) {
  var nUtil = new NotifyUtil();
  if (!notifyNumber || !nUtil.validateOutboundNotifyNumber(notifyNumber))
    return;
  var driver = nUtil.getTelephonyDriverFromNotifyNumber(notifyNumber);
    if (driver) {
      var notifyParticipantGr = new GlideRecord('notify_participant');
      notifyParticipantGr.get('active participant sys id');
    
      if (notifyParticipantGr.isValid) {
        driver.unmute(notifyParticipantGr)
    }
} 
```

