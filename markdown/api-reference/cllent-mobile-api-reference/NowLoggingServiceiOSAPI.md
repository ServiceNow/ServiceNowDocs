---
title: NowLoggingService class - iOS
description: The NowLoggingService class provides functions that provide logging capabilities to feature services with the NowSDK.Returns a logger for the specified feature service.Sets the desired logging level.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowLoggingService class- iOS

The NowLoggingService class provides functions that provide logging capabilities to feature services with the NowSDK.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

logLevel

</td><td>

NowLogLevel

</td><td>

Level of log messages for the associated logger to store.Valid values:

-   debug
-   error
-   fatal
-   log
-   info
-   none

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowLoggingService - logger\(for category: NowLogCategory\)

Returns a logger for the specified feature service.

<table id="table_rby_zpq_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

for category

</td><td>

NowLogCategory

</td><td>

Feature service whose logger you want returned.Valid values:

-   analytics
-   chat
-   coresdk
-   data
-   sdk
-   web

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|NowLogging|Logger to use to save all log messages for the associated service.|

The following code example shows how to call this function.

```
let logging = NowLoggingService.logger(for: .chat)
…
logger.error(message: "Could not create service - service configuration invalid")
…
logger.debug(message: "Verifying settings…")
```

## NowLoggingService - setLogLevel\(\_ logLevel: NowLogLevel\)

Sets the desired logging level.

**Note:** Incoming log messages with types that don’t meet the set log level threshold are discarded.

<table id="table_b5x_drq_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

logLevel

</td><td>

NowLogLevel

</td><td>

Level of log messages for the associated logger to store.Valid values:

-   debug
-   error
-   fatal
-   info
-   none

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
NowLoggingService.setLogLevel(.info)
```

