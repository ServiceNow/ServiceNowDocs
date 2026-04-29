---
title: NowGraphQLService class - iOS
description: The NowGraphQLService class provides functions that enable you to make requests using GraphQL queries against data on your ServiceNow instance through its GraphQL REST API.Executes the specified GraphQL query.Executes the specified GraphQL query.Creates a NowGraphQLService based on the specified parameters.Creates a publisher to request GraphQL data.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowGraphQLService class- iOS

The NowGraphQLService class provides functions that enable you to make requests using GraphQL queries against data on your ServiceNow instance through itsGraphQL REST API.

|Name|Type|Description|
|----|----|-----------|
|configuration|[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)|Configuration settings provided when the service was initialized.|

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowGraphQLService - execute\(query: GraphQLQuery\) async throws

Executes the specified GraphQL query.

|Name|Type|Description|
|----|----|-----------|
|query|String|GraphQL query to execute.|

<table id="table_tfm_c4h_ppb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data

</td><td>

Returned when the method is successful. Query data generated from the specified query.

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
</table>The following code example shows how to call this method.

```
private func fetchArticles() async throws -> [Article] { 
    guard let graphQLService = graphQLService else { 
        throw ArticleListError.invalidGraphQLService 
    }         

    do {
        let data = try await graphQLService.execute(GraphQLQuery(query: recentlyPublishedQuery))
        let articles = try dataToArticleList(data)
    } catch let error as NowDataError {
        throw ArticleListError.fetchError(error)
    } catch {
        throw error
    }
} 
  
private let recentlyPublishedQuery = 
""" 

{
  GlideRecord_Query {
    kb_knowledge(queryConditions: "active=true^ORDERBYpublishedDESC" pagination: { limit: 10, offset: 0 }) {
      _results { 
        sys_id {
          value
        },
        number {
          displayValue
        },
        short_description {
          displayValue
        },
        author {
          displayValue
        }
        published {
          displayValue
        }
      }
    }
  }
}
"""
```

## NowGraphQLService - execute\(query: GraphQLQuery, completion: @escaping \(Result&lt;Data, NowDataError&gt;\)\)

Executes the specified GraphQL query.

<table id="table_sfm_c4h_ppb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

query

</td><td>

String

</td><td>

GraphQL query to execute.

</td></tr><tr><td>

completion

</td><td>

@escaping \(Result&lt;Data, NowDataError&gt;\)

</td><td>

Completion handler to execute after the query is complete. Return values:

-   Success: Returns query data.
-   Error: NowDataError

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
gqlService.execute(GraphQLQuery(query: myQuery)) { result in 
  switch result { 
  case .success(let data): 
    // use data 
  case .failure(let error): 
    // handle error 
  } 
}
```

## NowGraphQLService - init\(configuration: NowServiceConfiguration, coreServiceProvider: NowCoreServiceProviding\)

Creates a NowGraphQLService based on the specified parameters.

<table id="table_k4t_mnh_ppb" class="parameters"><thead><tr><th>

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

Configuration parameters to use when initializing the service, such as the bundle ID of the application integrating with the service and the URL of the ServiceNow instance that the NowGraphQLService wants to access.

</td></tr><tr><td>

coreServiceProvider

</td><td>

NowCoreServiceProviding

</td><td>

Optional. Core service provider.**Note:** Currently this parameter is required even though it is shown as optional.

Default: nil

</td></tr></tbody>
</table>```

```

## NowGraphQLService - publisher\(for query: GraphQLQuery\)

Creates a publisher to request GraphQL data.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

|Name|Type|Description|
|----|----|-----------|
|for query|GraphQLQuery|GraphQL query string to execute.|

<table id="table_ksv_5wh_ppb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher&lt;Data, NowDataError&gt;

</td><td>

Success: GraphQL data set.Failure: NowDataError

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
private func fetchArticles() -> AnyPublisher<[Article], ArticleListError> {
  guard let graphQLService = graphQLService else {
    return Fail(error: .invalidGraphQLService).eraseToAnyPublisher()
  }
        
  return graphQLService.publisher(for: GraphQLQuery(query: recentlyPublishedQuery))
    .mapError({ dataError -> ArticleListError in
      .fetchError(dataError)
    })
    .flatMap(dataToArticleList)
    .eraseToAnyPublisher()
}
```

