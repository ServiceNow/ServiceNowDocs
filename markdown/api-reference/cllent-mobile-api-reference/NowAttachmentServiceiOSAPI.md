---
title: NowAttachmentService class - iOS
description: The NowAttachmentService class provides functions that enable you to upload and query attachments that are associated with records within a table on a ServiceNow instance.Retrieves the attachment with the specified sys\_id and validates the attachment by comparing the computed hash of the attachment to the expected SHA256 checksum.Retrieves the attachment with the specified sys\_id and validates the attachment by comparing the computed hash of the attachment to the expected SHA256 checksum. Once finished, it executes the passed completion handler.Retrieves the attachment with the specified sys\_id and validates the attachment by comparing the computed hash of the attachment to the expected hash.Retrieves the metadata for all the attachments that meet the specified criteria.Retrieves the metadata for all the attachments that meet the specified criteria.Retrieves the metadata for all the attachments that meet the specified criteria.Retrieves the metadata for the attachment associated with the specified sys\_id.Retrieves the metadata for the attachment associated with the specified sys\_id and then executes the completion handler after the metadata is retrieved.Retrieves the metadata for the attachment associated with the specified sys\_id.Retrieves the metadata for all the attachments that meet the specified criteria and returns a Paginator object for iterating through the pages of the returned metadata.Deletes the attachment with the specified sys\_id.Deletes the attachment with the specified sys\_id and then executes the passed completion handler after the attachment is deleted.Deletes the attachment with the specified sys\_id.Initializes a new NowAttachmentService instance.Uploads the attachment data and attaches it to a record in a table as specified in the upload configuration.Uploads the attachment data and attaches it to a record in a table as specified in the upload configuration.Uploads the attachment data and attaches it to a record in a table as specified in the upload configuration.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 32
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAttachmentService class - iOS

The NowAttachmentService class provides functions that enable you to upload and query attachments that are associated with records within a table on a ServiceNow instance.

You can upload or retrieve a single file with each request. NowAttachmentService respects any system limitations on uploaded files, such as maximum file size and allowed attachment types. You can control these settings using the instance properties com.glide.attachment.max\_size, 1024MB by default, and glide.attachment.extensions.

**Note:** NowAttachmentService accepts all Content-Type values \(/\). Specify the file content type when uploading an attachment. The content type is stored with the file metadata, enabling other tools to correctly identify and parse the file.

|Name|Type|Description|
|----|----|-----------|
|configuration|[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)|Configuration settings provided when the service was initialized.|

**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowAttachmentService - attachment\(for sysId: String, validateAttachment: Boolean\) async throws

Retrieves the attachment with the specified sys\_id and validates the attachment by comparing the computed hash of the attachment to the expected SHA256 checksum.

**Note:** Validation of an attachment can cause a performance impact. You can skip the validation step by setting the **validateAttachment** parameter to `false`. You can validate the attachment at a later stage if needed by calling the Attachment.validate\(\) function.

<table id="table_dqr_hmx_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

for sysId

</td><td>

String

</td><td>

Sys\_id of the attachment to retrieve.

</td></tr><tr><td>

validateAttachment

</td><td>

Boolean

</td><td>

Flag that indicates whether to validate the attachment.Valid values:

-   true: Validate the attachment.
-   false: Do not validate the attachment.

Default: true

</td></tr></tbody>
</table><table id="table_eqr_hmx_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NowAttachment

</td><td>

Returned when the method is successful. Specified attachment.

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
func downloadAttachment(sysId: String) async throws -> NowAttachment {
    do {
        let nowAttachment = try await attachmentService.attachment(for: sysId, validateAttachment: false)
        return nowAttachment
    } catch {
        // Handle NowDataError
        throw error
    }
}
```

## NowAttachmentService - attachment\(for sysId: String, validateAttachment: Boolean, completion: @escaping \(Result&lt;NowAttachment, NowDataError&gt;\)\)

Retrieves the attachment with the specified sys\_id and validates the attachment by comparing the computed hash of the attachment to the expected SHA256 checksum. Once finished, it executes the passed completion handler.

**Note:** Validation of an attachment can cause a performance impact. You can skip the validation step by setting the **validateAttachment** parameter to `false`. You can validate the attachment at a later stage if needed by calling the Attachment.validate\(\) function.

<table id="table_dqr_hmx_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

for sysId

</td><td>

String

</td><td>

Sys\_id of the attachment to retrieve.

</td></tr><tr><td>

validateAttachment

</td><td>

Boolean

</td><td>

Flag that indicates whether to validate the attachment.Valid values:

-   true: Validate the attachment.
-   false: Do not validate the attachment.

Default: true

</td></tr><tr id="mobilesdkiOS-completion_data_dataerror-row"><td>

completion

</td><td>

@escaping \(Result​&lt;[NowAttachment](../../NowAttachment/concept/NowAttachmentiOSStructure.md#), NowDataError&gt;\)

</td><td>

Completion handler to execute after the attachment is retrieved. Return values for the completion handler:

-   Success: [NowAttachment](../../NowAttachment/concept/NowAttachmentiOSStructure.md#) - Requested attachment
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
let sysId = UUID().uuidString  // UUID for the attachment
private func downloadAttachment(sysId: String) {
  attachmentService.attachment(for: sysId, validateAttachment: false) { (result) in
    switch result {
      case .success(let attachment):
        // Attachment retrieved successful, return attachment
      case .failure(let error):
        // Attachment retrieved failed, return NowDataError
    }
  }
}
```

## NowAttachmentService - attachment\(for sysId: String, validateAttachment: Boolean\)

Retrieves the attachment with the specified sys\_id and validates the attachment by comparing the computed hash of the attachment to the expected hash.

**Note:** Validation of an attachment can cause a performance impact. You can skip the validation step by setting the **validateAttachment** parameter to `false`. If needed, you can validate the attachment at a later stage by calling the Attachment.validate\(\) function.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

<table id="table_w4s_d3s_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

for sysId

</td><td>

String

</td><td>

Sys\_id of the attachment to retrieve.

</td></tr><tr><td>

validateAttachment

</td><td>

Boolean

</td><td>

Flag that indicates whether to validate the attachment.Valid values:

-   true: Validate the attachment.
-   false: Don’t validate the attachment.

Default: true

</td></tr></tbody>
</table><table id="table_x4s_d3s_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher​&lt;[NowAttachment](../../NowAttachment/concept/NowAttachmentiOSStructure.md#), NowDataError&gt;

</td><td>

Success: [NowAttachment](../../NowAttachment/concept/NowAttachmentiOSStructure.md#) - Contains the specified attachment.Failure: NowDataError

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
let sysId = UUID().uuidString  // UUID for the attachment
private func downloadAttachment(sysId: String) {
  let publisher = self.attachmentService.attachment(for: sysId, validateAttachment: false)
  publisher
    .receive(on: DispatchQueue.main)
    .sink { [weak self] completion in
      if case let .failure(error) = completion {
        // Attachment retrieved failed, return NowDataError
      }
    } receiveValue: { [weak self] (attachment) in
      // Attachment retrieved successful, return attachment
    }
    .store(in: &subscriptions)
}
```

## NowAttachmentService - attachmentMetadata\(filter: Filter, limit: Int\) async throws

Retrieves the metadata for all the attachments that meet the specified criteria.

<table id="table_tcn_cfs_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

[Filter](../../Filter/concept/FilteriOSStructure.md#)

</td><td>

Optional. Query string to use to filter the attachments whose metadata to return.Default: nil - Returns metadata for all available attachments. Takes into consideration the **limit** parameter.

</td></tr><tr><td>

limit

</td><td>

Integer

</td><td>

Optional. Maximum number of attachment file's metadata to return.Default: nil - Returns all metadata that meets the **filter** parameter specifications.

</td></tr></tbody>
</table><table id="table_ucn_cfs_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[NowAttachmentMetadata\]

</td><td>

Returned when the method is successful. Array that contains the metadata for the matching attachments.

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
let filter = Filter(criteria: [], sortBy: [.desc("created")],
             queryCategory: nil)
do {
    let metadata = try await attachmentService.attachmentMetadata(filter: filter, limit: 10)
    // Metadata retrieval successful
} catch {
    // Metadata retrieval failed, NowDataError thrown
}
```

## NowAttachmentService - attachmentMetadata\(filter: Filter, limit: Int, completion: @escaping \(Result&lt;\[NowAttachmentMetadata\], NowDataError&gt;\)\)

Retrieves the metadata for all the attachments that meet the specified criteria.

<table id="table_tcn_cfs_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

[Filter](../../Filter/concept/FilteriOSStructure.md#)

</td><td>

Optional. Query string to use to filter the attachments whose metadata to return.Default: nil - Returns metadata for all available attachments. Takes into consideration the **limit** parameter.

</td></tr><tr><td>

limit

</td><td>

Integer

</td><td>

Optional. Maximum number of attachment file's metadata to return.Default: nil - Returns all metadata that meets the **filter** parameter specifications.

</td></tr><tr><td>

completion

</td><td>

@escaping \(Result​&lt;\[[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#)\], NowDataError&gt;\)

</td><td>

Completion handler to execute after the metadata is retrieved. Return values for the completion handler:

-   Success: NowAttachmentMetadata - Objects containing the requested metadata.
-   Error: NowDataError
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
let query = "active=true^short_descriptionLIKEbroken"
let filter = Filter(query: query)
attachmentService.attachmentMetadata(filter: filter, limit: limit) { (result) in
  DispatchQueue.main.async { [weak self] in
    switch result {
    case .success(let response):
      do {
        let data = try JSONEncoder().encode(response)
        // Retrieve metadata successfully, return data
      } catch {
        // Retrieve metadata failed, return error 
      }
    case .failure(let error):
      // Retrieve metadata failed, return NowDataError
    }	
  }
}
```

## NowAttachmentService - attachmentMetadata\(filter: Filter, limit: Int\)

Retrieves the metadata for all the attachments that meet the specified criteria.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

<table id="table_ahv_32s_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

[Filter](../../Filter/concept/FilteriOSStructure.md#)

</td><td>

Optional. Query string to use to filter the attachments whose metadata to return.Default: nil - Returns metadata for all available attachments. Takes into consideration the **limit** parameter.

</td></tr><tr><td>

limit

</td><td>

Integer

</td><td>

Optional. Maximum number of attachment file's metadata to return.Default: nil - Returns all metadata that meets the **filter** parameter specifications.

</td></tr></tbody>
</table><table id="table_bhv_32s_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher​&lt;\[[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#)\], NowDataError&gt;

</td><td>

Success: NowAttachmentMetadata - Objects that contain the metadata for the matching attachments.Failure: NowDataError

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
let query = "active=true^short_descriptionLIKEbroken"
let filter = Filter(query: query)
let publisher = self.attachmentService.attachmentMetadata(filter: filter)
publisher
  .receive(on: DispatchQueue.main)
  .encode(encoder: JSONEncoder())
  .sink { [weak self] completion in
    if case let .failure(error) = completion {
      // Retrieve metadata failed, return NowDataError
  } receiveValue: { [weak self] (data) in
     // Retrieve metadata successfully, return data
  }
.store(in: &subscriptions
```

## NowAttachmentService - attachmentMetadata\(for sysId: String\) async throws

Retrieves the metadata for the attachment associated with the specified sys\_id.

|Name|Type|Description|
|----|----|-----------|
|for sysId|String|Sys\_id of the attachment whose metadata to retrieve.|

<table id="table_mdt_3hs_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NowAttachmentMetadata

</td><td>

Returned when the method is successful. Metadata for the requested attachment.

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
    let metadata = try await attachmentService.attachmentMetadata(for: sysId)
    // Metadata retrieval successful
} catch {
    // Metadata retrieval failed, NowDataError thrown
}
```

## NowAttachmentService - attachmentMetadata\(for sysId: String, completion: @escaping \(Result&lt;NowAttachmentMetadata, NowDataError&gt;\)\)

Retrieves the metadata for the attachment associated with the specified sys\_id and then executes the completion handler after the metadata is retrieved.

<table id="table_ldt_3hs_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

for sysId

</td><td>

String

</td><td>

Sys\_id of the attachment whose metadata to retrieve.

</td></tr><tr id="mobilesdkiOS-completion_data_dataerror-row"><td>

completion

</td><td>

@escaping \(Result​&lt;[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#), NowDataError&gt;\)

</td><td>

Completion handler to execute after the metadata is retrieved. Return values for the completion handler:

-   Success: [NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#) - Requested metadata
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
let sysId = UUID().uuidString  // UUID for the attachment
attachmentService.attachmentMetadata(for: sysId) { (result) in
  DispatchQueue.main.async { [weak self] in
    switch result {
      case .success(let response):
        do {
          let data = try JSONEncoder().encode(response)
          // Retrieve metadata successfully, return data
        } catch {
          // Retrieve metadata failed, return error      
        }
      case .failure(let error):
        // Retrieve metadata failed, return NowDataError
    }	
  }
}
```

## NowAttachmentService - attachmentMetadata\(for sysId: String\)

Retrieves the metadata for the attachment associated with the specified sys\_id.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

|Name|Type|Description|
|----|----|-----------|
|for sysId|String|Sys\_id of the attachment whose metadata to retrieve.|

<table id="table_thc_ngs_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher​&lt;\[[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#)\], NowDataError&gt;

</td><td>

Success: NowAttachmentMetadata - Object that contains the metadata for the requested attachment.Failure: NowDataError

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
let sysId = UUID().uuidString  // UUID for the attachment
let publisher = self.attachmentService.attachmentMetadata(for: sysId)
publisher
  .receive(on: DispatchQueue.main)
  .encode(encoder: JSONEncoder())
  .sink { [weak self] completion in
    if case let .failure(error) = completion {
      // Retrieve metadata failed, return NowDataError
    }
  } receiveValue: { [weak self] (data) in
     // Retrieve metadata successfully, return data
  }
.store(in: &subscriptions)
```

## NowAttachmentService - attachmentMetadataPaginator\(filter: Filter, limit: Int\)

Retrieves the metadata for all the attachments that meet the specified criteria and returns a Paginator object for iterating through the pages of the returned metadata.

<table id="table_tqh_dcs_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

[Filter](../../Filter/concept/FilteriOSStructure.md#)

</td><td>

Optional. Query string to use to filter the attachments whose metadata to return.Default: nil - Returns metadata for all available attachments. Takes into consideration the **limit** parameter.

</td></tr><tr><td>

limit

</td><td>

Integer

</td><td>

Optional. Maximum number of attachment file's metadata to return.Default: nil - Returns all metadata that meets the **filter** parameter specifications.

</td></tr></tbody>
</table><table id="table_uqh_dcs_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Paginator](../../Paginator/concept/PaginatorIOSAPI.md#)​&lt;\[[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#)\]&gt;

</td><td>

Success: Array of NowAttachmentMetadata objects. Failure: NowDataError object.

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
let paginator: Paginator<T> = makePaginator(query: query, fetchLimit: 1)

func makePaginator(query: String, fetchLimit: Int?) -> Paginator<[NowAttachmentMetadata]> {
  attachmentsService.attachmentMetadataPaginator(filter: Filter(query: query), limit: fetchLimit)
}
```

## NowAttachmentService - delete\(sysId: String\) async throws

Deletes the attachment with the specified sys\_id.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|Sys\_id of the attachment to delete.|

<table id="table_f5b_zqx_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

Nothing is returned if the method was successful.

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
    try await attachmentService.delete(sysId: sysId)
    // Deletion successful
} catch {
    // Deletion failed, NowDataError thrown
}
```

## NowAttachmentService - delete\(sysId: String, completion: @escaping \(Result&lt;Void, NowDataError&gt;\)\)

Deletes the attachment with the specified sys\_id and then executes the passed completion handler after the attachment is deleted.

<table id="table_e5b_zqx_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysId

</td><td>

String

</td><td>

Sys\_id of the attachment to delete.

</td></tr><tr><td>

completion

</td><td>

@escaping \(Result&lt;Void, NowDataError&gt;\)

</td><td>

Completion handler to execute after the attachment is deleted. Return values for the completion handler:

-   Success: Void
-   Error: NowDataError
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
let sysId = UUID().uuidString  // UUID for the attachment
attachmentService.delete(sysId: sysId) { (result) in
  DispatchQueue.main.async { [weak self] in
    switch result {
      case .success:
        // Attachment with sysId is deleted
      case .failure(let error):
        // Failed to delete, with NowDataError
    }
  }
}
```

## NowAttachmentService - delete\(sysId: String\)

Deletes the attachment with the specified sys\_id.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|Sys\_id of the attachment to delete.|

<table id="table_tvp_2qx_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher&lt;Void, NowDataError&gt;

</td><td>

Success: Nothing returnedFailure: NowDataError

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
let publisher = attachmentService.delete(sysId: sysId)
publisher
  .receive(on: DispatchQueue.main)
  .sink { [weak self] completion in
    switch completion {
      case .finished:
        // Attachment with sysId is deleted
      case .failure(let error):
       // Failed to delete, with NowDataError
   }
 } receiveValue: {
 }
 .store(in: &subscriptions)
```

## NowAttachmentService - init\(configuration: NowServiceConfiguration, coreServiceProvider: NowCoreServiceProviding\)

Initializes a new NowAttachmentService instance.

<table id="table_hfm_ry2_tpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)

</td><td>

Configuration information needed to properly initialize the service.

</td></tr><tr><td>

coreServiceProvider

</td><td>

NowCoreServiceProviding

</td><td>

Optional. Object implementing the NowCoreServiceProviding protocol.Default: nil

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
guard let coreService = NowSDK.core() else {
  // Error with NowServiceError.sdkNotConfigured
  return
}
guard 
  let instanceUrl = URL(string: "http://sample.service-now.com"), 
  let serviceConfig = NowSDK.makeServiceConfiguration(for: instanceUrl) else {
    // Could not create service – 
    // NowServiceError.serviceConfigurationInvalid
    return
}
let attachmentService = NowAttachmentService(configuration: serviceConfig, coreServiceProvider: coreService)
```

## NowAttachmentService - upload\(data: Data, configuration: NowAttachmentUploadConfiguration, progressUpdate: @escaping ProgressUpdate\) async throws

Uploads the attachment data and attaches it to a record in a table as specified in the upload configuration.

The ProgressUpdate callback provides upload progress information that you can then use to provide UI feedback.

<table id="table_n5z_mpx_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Data

</td><td>

Attachment to upload.

</td></tr><tr><td>

configuration

</td><td>

[NowAttachmentUpload Configuration](../../NowAttachmentUploadConfiguration/concept/NowAttachUploadConfigiOSStruct.md#)

</td><td>

Configuration information that defines the upload parameters for the attachment, such as: -   Table and record to attach the file to
-   Attachment file name
-   Type of attachment
-   Whether the file is encrypted

</td></tr><tr><td>

progressUpdate

</td><td>

@escaping ProgressUpdate

</td><td>

Completion handler to execute after the attachment is retrieved. This is called multiple times until the upload process is complete.Return values for the completion handler:

ProgressUpdate - Returns the current progress of the upload.

`ProgressUpdate = (_bytesWritten: Int64, _totalBytesWritten: Int64, _totalBytesExpectedToWrite: Int64) -> Void`

</td></tr></tbody>
</table><table id="table_o5z_mpx_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NowAttachmentMetadata

</td><td>

Returned when the method is successful. Object that contains the uploaded metadata.

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
func uploadFile(for tableName: String, sysId: String, mimeType: String, encryptionContext: String?, data: Data, filename: String) async throws -> NowAttachmentMetadata { 

    let mimeType = MediaUtilities.mimeType(forFileName: filename)
    let uploadConfig = NowAttachmentUploadConfiguration(tableName: tableName, 
                                                        recordSysId: sysId,
                                                        fileName: filename,
                                                        contentType: mimeType,
                                                        encryptionContext: encryptionContext) 

    do {
        let attachmentMetadata = try await attachmentService.upload(data: data, configuration: uploadConfig) { (_, _, _) in }
        return attachmentMetadata
    } catch {
        // Handle NowDataError
        throw error
    }
}
```

## NowAttachmentService - upload\(data: Data, configuration: NowAttachmentUploadConfiguration, progressUpdate: @escaping ProgressUpdate, completion: @escaping \(Result&lt;NowAttachmentMetadata, NowDataError&gt;\)\)

Uploads the attachment data and attaches it to a record in a table as specified in the upload configuration.

The ProgressUpdate callback provides upload progress information that you can then use to provide UI feedback.

<table id="table_n5z_mpx_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Data

</td><td>

Attachment to upload.

</td></tr><tr><td>

configuration

</td><td>

[NowAttachmentUpload Configuration](../../NowAttachmentUploadConfiguration/concept/NowAttachUploadConfigiOSStruct.md#)

</td><td>

Configuration information that defines the upload parameters for the attachment, such as: -   Table and record to attach the file to
-   Attachment file name
-   Type of attachment
-   Whether the file is encrypted

</td></tr><tr><td>

progressUpdate

</td><td>

@escaping ProgressUpdate

</td><td>

Completion handler to execute after the attachment is retrieved. This is called multiple times until the upload process is complete.Return values for the completion handler:

ProgressUpdate - Returns the current progress of the upload.

`ProgressUpdate = (_bytesWritten: Int64, _totalBytesWritten: Int64, _totalBytesExpectedToWrite: Int64) -> Void`

</td></tr><tr><td>

completion

</td><td>

@escaping \(Result&lt;[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#), NowDataError&gt;\)

</td><td>

Completion handler to execute after the metadata is uploaded. Return values for the completion handler:

-   Success: [NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#) - Object containing the metadata for the uploaded attachment.
-   Error: NowDataError
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
typealias ProgressUpdate = (_ bytesWritten: Int64, _ totalBytesWritten: Int64, _ totalBytesExpectedToWrite: Int64) -> Void

let image = UIImage(named: "photo.png") 
let data = image.pngData() 
let recordSysId = "" // Sys_id of the record on the SN instance

let config = NowAttachmentUploadConfiguration(
  tableName: "tableName", 
  recordSysId: recordSysId, 
  fileName: "photo.png",
  contentType: "image/png",
  encryptionContext: nil)

private func uploadFile(
  data: Data,
  config: NowAttachmentUploadConfiguration,
  progress: @escaping ProgressUpdate) {
    attachmentService.upload(data: data, configuration: config, progressUpdate: progress) { (result) in
      DispatchQueue.main.async { [weak self] in
        switch result {
          case .success(let response)
            do {
              let data = try JSONEncoder().encode(response)
                // Upload file successfully, return data
            } catch
                // Upload file decode failed, return error
            }
          case .failure(let error):
                // Upload file failed, return NowDataError
      }
    }
  }

```

## NowAttachmentService - upload\(data: Data, configuration: NowAttachmentUploadConfiguration, progressUpdate: @escaping ProgressUpdate\)

Uploads the attachment data and attaches it to a record in a table as specified in the upload configuration.

The ProgressUpdate callback provides upload progress information that you can then use to provide UI feedback.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

<table id="table_ptn_lnx_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Data

</td><td>

Attachment to upload. The data size and type of attachment that you can upload are controlled by your ServiceNow instance.

</td></tr><tr><td>

configuration

</td><td>

[NowAttachmentUploadConfiguration](../../NowAttachmentUploadConfiguration/concept/NowAttachUploadConfigiOSStruct.md#)

</td><td>

Configuration information that defines the upload parameters for the attachment, such as:-   Table and record to attach the file to
-   Attachment file name
-   Type of attachment
-   Whether the file is encrypted

</td></tr><tr><td>

progressUpdate

</td><td>

@escaping ProgressUpdate

</td><td>

Completion handler to execute after the attachment is retrieved. Return values for the completion handler:

ProgressUpdate - Returns the current progress of the upload. This is called multiple times until the upload process is complete.

`ProgressUpdate = (_bytesWritten: Int64, _totalBytesWritten: Int64, _totalBytesExpectedToWrite: Int64) -> Void`

</td></tr></tbody>
</table><table id="table_qtn_lnx_spb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher​&lt;[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#), NowDataError&gt;

</td><td>

Success: [NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#) - Object that contains the metadata for the requested attachment.Failure: NowDataError

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
typealias ProgressUpdate = (_ bytesWritten: Int64, _ totalBytesWritten: Int64, _ totalBytesExpectedToWrite: Int64) -> Void

let image = UIImage(named: "photo.png") 
let data = image.pngData() 
let recordSysId = "" // Sys_id of the record on the SN instance
let config = NowAttachmentUploadConfiguration(
  tableName: "tableName", 
  recordSysId: recordSysId, 
  fileName: "photo.png",
  contentType: "image/png", 
  encryptionContext: nil)

private func uploadFile(data: Data,
  config: NowAttachmentUploadConfiguration,
  progress: @escaping ProgressUpdate) {
    let publisher = attachmentService.upload(data: data, configuration: config, progressUpdate: progress)

    publisher
      .receive(on: DispatchQueue.main)
      .encode(encoder: JSONEncoder())
      .sink { [weak self] completion in
        if case let .failure(error) = completion {
          // Upload file failed, return NowDataError
        }
      } receiveValue: { [weak self] (data) in
        // Upload file successfully, return data
      }
      .store(in: &subscriptions)
  }

```

