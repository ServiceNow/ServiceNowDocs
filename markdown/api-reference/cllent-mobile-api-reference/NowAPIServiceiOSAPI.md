---
title: NowAPIService class - iOS
description: The NowAPIService class provides functions that enable you to perform requests to a specified ServiceNow REST API.Requests data from the specified ServiceNow REST API and then executes the completion handler.Requests data from the specified ServiceNow REST API.Requests data from the specified ServiceNow REST API.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAPIService class- iOS

The NowAPIService class provides functions that enable you to perform requests to a specified ServiceNow REST API.

|Name|Type|Description|
|----|----|-----------|
|configuration|[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)|Service configuration to associate with the protocol.|

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowAPIService - data\(for endpoint: NowAPIEndpoint, queryItems: \[String: String\], httpHeaders: \[String: String\], body: Data, completion: @escaping \(Result&lt;DataResponse, NowDataError&gt;\)

Requests data from the specified ServiceNow REST API and then executes the completion handler.

<table id="table_jck_kyp_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

for endpoint

</td><td>

[NowAPIEndpoint](../../NowAPIEndpoint/concept/NowAPIEndpointiOSProtocol.md#)

</td><td>

Object containing the ServiceNow REST API endpoint to access, including the HTTP method, relative path to the endpoint, path parameters, and whether authentication is required.

</td></tr><tr><td>

queryItems

</td><td>

Array

</td><td>

Optional. Query parameters for the endpoint as key/value pairs.Default: nil

</td></tr><tr><td>

httpHeaders

</td><td>

Array

</td><td>

Optional. Request HTTP headers required by the endpoint as key/value pairs. Default: nil

</td></tr><tr><td>

body

</td><td>

String

</td><td>

Optional. Request body parameters.Default: nil

</td></tr><tr id="mobilesdkiOS-completion_data_dataerror-row"><td>

completion

</td><td>

@escaping \(Result&lt;DataResponse, NowDataError&gt;\)

</td><td>

Completion handler to execute after the REST API call completes. Return values for the completion handler:

-   Success: DataResponse that contains the returned data from the REST API call.
-   Failure: NowDataError
    -   `accessToken(AccessTokenProviderError)`

        -   **AccessTokenProviderError**: The access token provider's error code or message.
            -   accessTokenRetrievalFailed
            -   userSessionError\(\_ error: Error\)
Thrown when there is an error in the access token.

    -   `attachmentValidation`

Thrown when an attachment fails validation.

    -   `badResponse(statusCode: HTTPStatusCode)`

        -   **HTTPStatusCode**: Status code received from the instance.
Thrown when a request returns an unexpected response

    -   `cannotDecodeModel(DecodingError)`

        -   **DecodingError**: Decoding error detected.
Thrown when a Codable model cannot be decoded from JSON.

    -   `cannotDecodeProperty(type: Any, from: String)`

        -   **type**: Wrapped type to decode from a string.
        -   **from**: String to decode to the specified type.
Thrown when a string-wrapped value cannot be decoded from JSON.

    -   `cannotEncodeModel(EncodingError)`

        -   **EncodingError**: Encoding error detected.
Thrown when a Codable model cannot be encoded to JSON.

    -   `cannotParseResponse`

Thrown when a response from the instance cannot be parsed into its expected format.

    -   `invalidURL`

Thrown when a URL cannot be formed. For example, if the string contains characters that are illegal in a URL or is an empty string.

    -   `missingAttachmentMetadata`

Thrown when the attachment metadata header is missing.

    -   `missingServiceConfiguration`

Thrown when an expected service configuration is missing.

    -   `missingSysID`

Thrown when an expected sys\_id parameter is missing.

    -   `network(NetworkServiceError)`

        -   genericError\(String\)
        -   operationCanceled
        -   service​Disabled
        -   serverError\(Error\)
        -   systemError\(Error\)
Thrown when a network service encountered an error.


</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
struct Endpoint: NowAPIEndpoint {
  let httpMethod: HTTPMethod
  let relativePath: String
  let requiresAuthentication: Bool
}

/// HTTP request method
public enum HTTPMethod: CaseIterable {
    case options, get, head, post, put, patch, delete, trace, connect
}
let relativePath = “/api/now/account”
let endPoint = Endpoint(httpMethod: HTTPMethod.get, relativePath: relativePath, requiresAuthentication: true)

apiService.data(for: endPoint, queryItems: [“name”: “abel”], httpHeaders: httpHeaders, body: body.data(using: .utf8)) { [weak self] (result) in
  switch result {
    case .success(let response):
    // Data request successful
    case .failure(let error):
    // Data request failed, return NowDataError
    // .failure(error)
  }
}

```

## NowAPIService - data\(for endpoint: NowAPIEndpoint, queryItems: \[String: String\], httpHeaders: \[String: String\], body: Data\) async throws

Requests data from the specified ServiceNow REST API.

<table id="table_jck_kyp_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

for endpoint

</td><td>

[NowAPIEndpoint](../../NowAPIEndpoint/concept/NowAPIEndpointiOSProtocol.md#)

</td><td>

Object containing the ServiceNow REST API endpoint to access, including the HTTP method, relative path to the endpoint, path parameters, and whether authentication is required.

</td></tr><tr><td>

queryItems

</td><td>

Array

</td><td>

Optional. Query parameters for the endpoint as key/value pairs.Default: nil

</td></tr><tr><td>

httpHeaders

</td><td>

Array

</td><td>

Optional. Request HTTP headers required by the endpoint as key/value pairs. Default: nil

</td></tr><tr><td>

body

</td><td>

String

</td><td>

Optional. Request body parameters.Default: nil

</td></tr></tbody>
</table><table id="table_kck_kyp_5pb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DataResponse

</td><td>

Returned when the method is successful. Data from the REST API call.

</td></tr><tr><td>

NowDataError

</td><td>

Thrown when the method fails. -   `accessToken(AccessTokenProviderError)`

    -   **AccessTokenProviderError**: The access token provider's error code or message.
        -   accessTokenRetrievalFailed
        -   userSessionError\(\_ error: Error\)
Thrown when there is an error in the access token.

-   `attachmentValidation`

Thrown when an attachment fails validation.

-   `badResponse(statusCode: HTTPStatusCode)`

    -   **HTTPStatusCode**: Status code received from the instance.
Thrown when a request returns an unexpected response

-   `cannotDecodeModel(DecodingError)`

    -   **DecodingError**: Decoding error detected.
Thrown when a Codable model cannot be decoded from JSON.

-   `cannotDecodeProperty(type: Any, from: String)`

    -   **type**: Wrapped type to decode from a string.
    -   **from**: String to decode to the specified type.
Thrown when a string-wrapped value cannot be decoded from JSON.

-   `cannotEncodeModel(EncodingError)`

    -   **EncodingError**: Encoding error detected.
Thrown when a Codable model cannot be encoded to JSON.

-   `cannotParseResponse`

Thrown when a response from the instance cannot be parsed into its expected format.

-   `invalidURL`

Thrown when a URL cannot be formed. For example, if the string contains characters that are illegal in a URL or is an empty string.

-   `missingAttachmentMetadata`

Thrown when the attachment metadata header is missing.

-   `missingServiceConfiguration`

Thrown when an expected service configuration is missing.

-   `missingSysID`

Thrown when an expected sys\_id parameter is missing.

-   `network(NetworkServiceError)`

    -   genericError\(String\)
    -   operationCanceled
    -   service​Disabled
    -   serverError\(Error\)
    -   systemError\(Error\)
Thrown when a network service encountered an error.


</td></tr></tbody>
</table>The following code examples shows how to call this method.

```
do {
    let dataResponse = try await apiService.data(for: endpoint, queryItems: queryItems, httpHeaders: httpHeaders, body: body)
    // Data request successful
} catch {
    // Data request failed, NowDataError thrown
}
```

## NowAPIService - data\(for endpoint: NowAPIEndpoint, queryItems: \[String: String\]? = nil, httpHeaders: \[String: String\]? = nil, body: Data? = nil\)

Requests data from the specified ServiceNow REST API.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

<table id="table_sfb_5tp_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

for endpoint

</td><td>

[NowAPIEndpoint](../../NowAPIEndpoint/concept/NowAPIEndpointiOSProtocol.md#)

</td><td>

Object containing the ServiceNow REST API endpoint to access, including the HTTP method, relative path to the endpoint, path parameters, and whether authentication is required.

</td></tr><tr><td>

queryItems

</td><td>

Array

</td><td>

Optional. Query parameters for the endpoint as key/value pairs.Default: nil

</td></tr><tr><td>

httpHeaders

</td><td>

Array

</td><td>

Optional. Request HTTP headers required by the endpoint as key/value pairs.Default: nil

</td></tr><tr><td>

body

</td><td>

Data

</td><td>

Optional. Request body parameters. Default: nil

</td></tr></tbody>
</table><table id="table_tfb_5tp_5pb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher&lt;DataResponse, NowDataError&gt;

</td><td>

Success: Data returned by the REST API.Failure: NowDataError

-   `accessToken(AccessTokenProviderError)`

    -   **AccessTokenProviderError**: The access token provider's error code or message.
        -   accessTokenRetrievalFailed
        -   userSessionError\(\_ error: Error\)
Thrown when there is an error in the access token.

-   `attachmentValidation`

Thrown when an attachment fails validation.

-   `badResponse(statusCode: HTTPStatusCode)`

    -   **HTTPStatusCode**: Status code received from the instance.
Thrown when a request returns an unexpected response

-   `cannotDecodeModel(DecodingError)`

    -   **DecodingError**: Decoding error detected.
Thrown when a Codable model cannot be decoded from JSON.

-   `cannotDecodeProperty(type: Any, from: String)`

    -   **type**: Wrapped type to decode from a string.
    -   **from**: String to decode to the specified type.
Thrown when a string-wrapped value cannot be decoded from JSON.

-   `cannotEncodeModel(EncodingError)`

    -   **EncodingError**: Encoding error detected.
Thrown when a Codable model cannot be encoded to JSON.

-   `cannotParseResponse`

Thrown when a response from the instance cannot be parsed into its expected format.

-   `invalidURL`

Thrown when a URL cannot be formed. For example, if the string contains characters that are illegal in a URL or is an empty string.

-   `missingAttachmentMetadata`

Thrown when the attachment metadata header is missing.

-   `missingServiceConfiguration`

Thrown when an expected service configuration is missing.

-   `missingSysID`

Thrown when an expected sys\_id parameter is missing.

-   `network(NetworkServiceError)`

    -   genericError\(String\)
    -   operationCanceled
    -   service​Disabled
    -   serverError\(Error\)
    -   systemError\(Error\)
Thrown when a network service encountered an error.


</td></tr></tbody>
</table>The following code example shows how to call this function.

```
struct Endpoint: NowAPIEndpoint {
    let httpMethod: HTTPMethod
    let relativePath: String
    let requiresAuthentication: Bool
}

/// HTTP request method
public enum HTTPMethod: CaseIterable {
    case options, get, head, post, put, patch, delete, trace, connect
}
let relativePath = "/api/now/account"
let endPoint = Endpoint(httpMethod: HTTPMethod.get, relativePath: relativePath, requiresAuthentication: true)

// Using Combine
apiService.data(for: Endpoint(httpMethod: httpMethod, relativePath: endpointPath, requiresAuthentication: requiresAuthentication), queryItems: queryItems, httpHeaders: httpHeaders, body: body.data(using: .utf8))
  .receive(on: DispatchQueue.main)
  .sink { [weak self] (comp) in
    if case let .failure(error) = comp {
      // Data request failed, return NowDataError
    }
  } receiveValue: { [weak self] (response) in
    // Data request successful
    self?.publish(data: response.data)
  }
  .store(in: &self.subscriptions)
}
```

