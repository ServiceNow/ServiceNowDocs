---
title: SMSPreferenceHandlerSNC - Scoped, Global
description: The SMSPreferenceHandler script include provides methods to manage short message service \(SMS\) configurations.Instantiates the SMSPreferenceHandler script include object.Returns the preferences configuration record for the current telephony service provider.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SMSPreferenceHandlerSNC - Scoped, Global

The SMSPreferenceHandler script include provides methods to manage short message service \(SMS\) configurations.

This script include is implemented as the script include SMSPreferenceHandlerSNC and resides in the `sn_sms_pref` namespace. To use this API you must install the Notify plugin \(com.snc.notify\) which requires a separate subscription. You can activate this plugin if you have the admin role.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SMSPreferenceHandlerSNC - SMSPreferenceHandler\(String provider\)

Instantiates the SMSPreferenceHandler script include object.

|Name|Type|Description|
|----|----|-----------|
|provider|String|Name of the telephony service provider.|

```
var handler = new sn_sms_pref.SMSPreferenceHandler('TwilioDirect'); // Pass the provider name
var config = handler.getConfig();
```

## SMSPreferenceHandlerSNC - getConfig\(\)

Returns the preferences configuration record for the current telephony service provider.

The method queries all preference configuration records from the SMS Preference Configuration \[sn\_sms\_pref\_configuration\] table for the current telephony service provider, sorts the results by the Order field \(lowest to highest\), and then returns the first record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|Preference configuration record for the current telephony service provider. If no record exists, then null.|

```
var handler = new sn_sms_pref.SMSPreferenceHandler('TwilioDirect'); // Pass the provider name
var config = handler.getConfig();
```

