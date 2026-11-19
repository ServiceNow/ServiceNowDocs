---
title: NowPush API - iOS
description: The NowPush API is a top-level global API that enables users to instantiate a NowPush service instance.Creates an instance of NowChatService with the specified configuration.Creates an instance of NowPushService with the specified configuration, and once complete, calls the specified completion handler.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/cllent-mobile-api-reference/NowPushiOSAPI.html
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowPush API- iOS

The NowPush API is a top-level global API that enables users to instantiate a NowPush service instance.

**Parent Topic:**[Mobile SDK - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/MobileSDKiOSAPI.md)

## NowPush - makePushService\(instanceUrl: URL\)

Creates an instance of `NowChatService` with the specified configuration.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance providing push notification services.|

|Type|Description|
|----|-----------|
|AnyPublisher&lt;[Now​Push​Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowPushServiceiOSAPI.md), NowServiceError&gt;|If successful, returns an initialized [Now​Push​Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowPushServiceiOSAPI.md) object. If it fails, returns a NowServiceError object.|

This example shows how to create an instance of `NowChatService`.

```
func setup(with instanceURL: URL) -> AnyPublisher<NowService, ConfigurationError> {
  NowPush.makePushService(instanceUrl: instanceURL)
    .mapError { .sdkError($0) }
    .map { $0 as NowService }
    .eraseToAnyPublisher()
}
```

## NowPush - makePushService\(instanceUrl: URL, completion: @escaping \(\(Result&lt;NowPushService, NowServiceError&gt;\) -&gt; Void\)\)

Creates an instance of `NowPushService` with the specified configuration, and once complete, calls the specified completion handler.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance providing push notification services.|
|completion|@escaping \(\(Result&lt;[Now​Push​Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowPushServiceiOSAPI.md), Now​Service​Error&gt;\) -&gt; Void\)|Completion handler that is called containing either an initialized `NowPushService` instance or a `NowServiceError` indicating why the initialization failed.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to create an instance of `NowPushService`.

```
static func setup(with instanceURL: URL,completion: @escaping
  (Result<NowPushService, NowServiceError>) → Void) {
    NowPush.makePushService(instanceUrl: instanceURL} {result in
      switch result {
      case .success(letpushService):
        completion(.success(pushService))
      case .failure(let error):
        completion(.failure(eror))
      }
    }
  }
```

