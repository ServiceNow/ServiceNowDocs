---
title: NowData framework - iOS
description: The NowData framework contains methods that enable the instantiation of NowData services, such as NowGraphQLService, NowTableService, NowAPIService \(for custom APIs\), and NowAttachmentService.Creates an instance of NowApiService, and once complete, calls the specified completion handler.Creates an instance of NowAttachmentService, and after completion, calls the specified completion handler.Creates an instance of NowGraphQLService, and once complete, calls the specified completion handler.Creates an instance of NowTableService, and after it completes, calls the specified completion handler.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowData framework- iOS

The NowData framework contains methods that enable the instantiation of NowData services, such as NowGraphQLService, NowTableService, NowAPIService \(for custom APIs\), andNowAttachmentService.

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowData - makeApiService\(instanceUrl: URL, path: String, completion: @escaping \(\(Result&lt;NowApiService, NowServiceError&gt;\) -&gt; Void\)\)

Creates an instance of NowApiService, and once complete, calls the specified completion handler.

<table id="table_ff3_4pw_kqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

instanceUrl

</td><td>

URL

</td><td>

URL of the ServiceNow instance whose REST APIs are to be accessed by the service.

</td></tr><tr><td>

path

</td><td>

String

</td><td>

API path. For example, if the API call is `https://xxx.service-now.com/api/now/sg/incident`, the path is `/api/now/sg/incident`.

</td></tr><tr><td>

completion

</td><td>

@escaping \(\(Result​&lt;[NowApiService](../../NowAPIService/concept/NowAPIServiceiOSAPI.md#), Now​Service​Error&gt;\) -&gt; Void\)

</td><td>

Completion handler that is called with a `Result<NowApiService, NowServiceError>` containing either an initialized `NowApiService` instance or a `NowServiceError` indicating why the initialization failed.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
let path = "api/now/sg"
let apiPublisher = apiService(for: path)

func apiService(for path: String) -> AnyPublisher<NowAPIService, ConfigurationError> {
  guard let instanceURL else {
    return Fail(error: ConfigurationError.invalidInstanceURL)
    .eraseToAnyPublisher()
  }
  return Future { promise in
    NowData.makeApiService(instanceUrl: instanceURL, path: path) { (result) in
      promise(result.mapError { .sdkError($0) })
    }
  }
  .eraseToAnyPublisher()
}
```

## NowData - makeAttachmentService\(instanceUrl: URL, completion: @escaping \(\(Result&lt;NowAttachmentService, NowServiceError&gt;\) -&gt; Void\)\)

Creates an instance of NowAttachmentService, and after completion, calls the specified completion handler.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance whose attachments are to be accessed by the service.|
|completion|@escaping \(\(Result​&lt;[NowAttachmentService](../../NowAttachmentService/concept/NowAttachmentServiceiOSAPI.md#), Now​Service​Error&gt;\) -&gt; Void\)|Completion handler that is called with a `Result<NowAttachmentService, NowServiceError>` containing either an initialized `NowAttachmentService` instance or a `NowServiceError` indicating why the initialization failed.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
….
guard 
  let jwtUrl = URL(string: "http://13.57.38.237:8080"),
  let instanceUrl = URL(string: "https://mobilecoresdk.service-now.com") else {
    return
  }

// AuthorizationProvider – struct conforming to NowSDKAuthorizationProviding protocol
let authorizationProvider = AuthorizationProvider(userEmail: "sdk@servicenow.com", jwtProviderUrl: jwtUrl, clientId: "deb8756b452d201039231ca568f26511")
        
// PermissionProvider – class conforming to DevicePermissionDelegate protocol
let permissionProvider = PermissionProvider()
let config = NowSDKConfiguration(authorizationProvider: authorizationProvider, permissionDelegate: permissionProvider, logLevel: .debug)
	
do {
  try NowSDK.configure(with: config)
  initializeAttachmentService (with: instanceURL)
} catch {
  // Return ConfigurationError.sdkError(error)
}
…..

func initializeAttachmentService(instanceUrl: instanceURL) { result in
  switch result {
    case .success(let service)
      self?.attachmentService = service
    case .failure(let error)
      debug.print(“Creating Attachment service failed with error: \(error.localizedDescription)”)
      self?.attachmentService = nil
  }
}

```

## NowData - makeGraphQLService\(instanceUrl: URL, completion: @escaping \(\(Result&lt;NowGraphQLService, NowServiceError&gt;\) -&gt; Void\)\)

Creates an instance of NowGraphQLService, and once complete, calls the specified completion handler.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance providing GraphQL services.|
|completion|@escaping \(\(Result​&lt;[NowGraphQLService](../../NowGraphQLService/concept/NowGraphQLServiceiOSAPI.md#), Now​Service​Error&gt;\) -&gt; Void\)|Completion handler that is called with a `Result<NowGraphQLService, NowServiceError>` containing either an initialized `NowGraphQLService` instance or a `NowServiceError` indicating why the initialization failed.|

|Type|Description|
|----|-----------|
|None| |

```
func initializeGraphQLService(instanceUrl: URL) {
  makeGraphQLService(instanceUrl: instanceUrl) { [weak self] result in
    switch result {
    case .success(let service):
      self?.graphQLService = service
    case .failure(let error):
      debugPrint("Creating GraphQL service failed with error: \(error.localizedDescription)")
      self?.graphQLService = nil
    }
  }
}
```

## NowData - makeTableService\(instanceUrl: URL, completion: @escaping \(\(Result&lt;NowTableService, NowServiceError&gt;\) -&gt; Void\)\)

Creates an instance of NowTableService, and after it completes, calls the specified completion handler.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance whose tables are to be accessed by the service.|
|completion|@escaping \(\(Result​&lt;[NowTableService](../../NowTableService/concept/NowTableServiceiOSAPI.md#), Now​Service​Error&gt;\) -&gt; Void\)|Completion handler that is called with a `Result<NowTableService, NowServiceError>` containing either an initialized `NowTableService` instance or a `NowServiceError` indicating why the initialization failed.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
func initializeTableService(for instanceUrl: URL) {
  makeTableService(instanceUrl: instanceUrl) { [weak self] result in
    guard let self = self else { return }
            
    switch result {
      case .success(let tableService):
        self.tableService = tableService
        // Create a Paginator that will iterate over pages of customer support cases. The Paginator's response type will be
        // inferred from the Paginator's type definition (e.g. `Paginator<[CustomerServiceCase]>`).
        self.paginator = tableService.paginator(from: Self.tableName, configuration: self.fetchConfiguration)
        // Subscribe to the Paginator's publisher so we will be able to receive paged results.
        self.subscribeToPaginatorPublisher()
        // As we are now ready to start fetching data, inform the view controller.
        self.onReady(self)
      case .failure(let error):
        debugPrint("Creating table service failed with error: \(error.localizedDescription)")
        self.tableService = nil
        self.paginator = nil
    }
  }
}
```

