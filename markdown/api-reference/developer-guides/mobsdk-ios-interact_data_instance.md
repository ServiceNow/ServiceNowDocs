---
title: Interact with table data in a ServiceNow instance
description: The Mobile SDK enables you to interact with data in tables that reside on your ServiceNow instance. You can interact with this data through the ServiceNow REST Table API using the NowTableService\(\) API that directly calls the REST interface, or through the NowGraphQLService\(\) API that executes a specified GraphQL query against the REST GraphQL API.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Interact with table data in a ServiceNow instance

The Mobile SDK enables you to interact with data in tables that reside on your ServiceNow instance. You can interact with this data through the ServiceNow REST Table API using theNowTableService\(\) API that directly calls the REST interface, or through the NowGraphQLService\(\) API that executes a specified GraphQL query against the REST GraphQL API.

If you want to return data from multiple tables within a single call, you will need to use the NowGraphQLService\(\) API. If you need to interact with other ServiceNow REST APIs, see [Interact with the public REST API on a ServiceNow instance](mobsdk-ios-interact-rest_api.md).

## Using NowGraphQLService to interact with ServiceNow tables

The [NowGraphQLService](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowGraphQLService/concept/NowGraphQLServiceiOSAPI.md#) class provides methods that enable you to construct and execute GraphQL queries on a specified table within your ServiceNow instance if the logged in user has the proper authorization. You can define all CRUD operations within your GraphQL query.

NowGraphQLService supports fetching results for a query by returning a completion handler:

```
func execute(_ query: GraphQLQuery, completion: @escaping (Result<Data, NowDataError>) → Void)
```

Through async/await:

```
func execute(_ query: GraphQLQuery) async throws -> Data
```

Or, a [Combine](https://developer.apple.com/documentation/combine) publisher \(which is currently deprecated\):

```
func publisher(for query: GraphQlQuery) → AnyPublisher<Data, NowDataError>

```

The following example shows how to import the NowData framework and then initialize a NowGraphQLService object that you can then use to interact with tables in your ServiceNow instance.

```
// Import the NowData framework
import NowData

// Initialize a NowGraphQLService
// The makeGraphQLService completion handler returns a result that wraps 
// the NowGraphQLService upon success or error. 

private func initializeGraphQLService(instanceUrl: URL) {
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

This example shows how to create an async function that fetches and publishes the most recently published KB articles.

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

## Using NowTableService to interact with ServiceNow tables

The [NowTableService](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowTableService/concept/NowTableServiceiOSAPI.md#) class provides methods to perform CRUD operations on the records in tables that reside on your ServiceNow instance. Through this interface you can directly access any of the records within any ServiceNow table for which the logged in user is authorized. NowTableService supports dot-walking for reference fields. For example, if a table contains a reference to the User table, the dot-walked value `user.name` returns the name of the user.

When returning the requested data, all applicable Access Control Lists \(ACLs\) are applied to the data, which may result in fewer results than expected, or authorization errors if the authenticated user does not have access rights to the specified table.

Most NowTableService methods provide three implementations for returning results data. One that uses async/await, one that calls a completion handler with a **Result** enumeration, and one that returns a [Combine](https://developer.apple.com/documentation/combine) publisher, which is currently deprecated.

For example, all createRecord\(\) methods insert a constructed record into a specified table, however, the

`[NowTableService - createRecord\(with fields: \[FieldName: FieldValue\], in tableName: String, writeOptions: FieldWriteOptions, configuration: FieldReadConfiguration, completion: @escaping \(Result&lt;Data, NowDataError&gt;\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowTableService/concept/NowTableServiceiOSAPI.md#)`

method calls a completion handler with a **Result** enumeration \(the `.success` case contains the results as its associated value\).

The

`[NowTableService - createRecord\(with fields: \[FieldName: FieldValue\], in tableName: String, writeOptions: FieldWriteOptions? = nil, configuration: FieldReadConfiguration? = nil\) async throws](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowTableService/concept/NowTableServiceiOSAPI.md#)`

method performs an async/await function. While the

`[NowTableService - createRecord\(with fields: \[FieldName: FieldValue\], in tableName: String, writeOptions: FieldWriteOptions? = nil, configuration: FieldReadConfiguration? = nil\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowTableService/concept/NowTableServiceiOSAPI.md#)`

method returns a Combine publisher, but is currently deprecated.

In addition, NowTableService provides two different implementations of CRUD methods, one that returns raw data, and one that returns Codable models. For example, both the update\(\) and updateRecord\(\) methods update a specified record in a specified table, but the update\(\) methods return a Codable model and the updateRecord\(\) methods return raw data. In some cases, Codable methods might be preferable, as a strongly typed Codable structure provides more flexibility than a collection of raw data fields.

The following example shows how to import the NowData framework and then initialize a NowTableService object that you can then use to interact with ServiceNow instance tables.

```
// Import the NowData framework
import NowData

// Initialize a NowTableService
// The makeTableService completion handler returns a result that wraps 
// the NowTableService upon success or error. 

makeTableService(instanceUrl: instanceUrl) { [weak self] result in
  guard let self = self else { return }
  
  switch result {
  case .success(let tableService):
    debugPrint("Successfully created a table service \(tableService)")
    self.tableService = tableService
  case .failure(let error):
    debugPrint("Creating table service failed with error: \(error.localizedDescription)")
  }
}
```

For additional code examples using the available NowTableService methods, refer to the `[NowTableService class - iOS](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowTableService/concept/NowTableServiceiOSAPI.md#)`API documentation.

