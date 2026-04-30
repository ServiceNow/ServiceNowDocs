---
title: Interact with table data in a ServiceNow instance
description: The Mobile SDK enables you to interact with data in tables that reside on your ServiceNow instance. You can interact with this data through the ServiceNow REST Table API using the NowTableService\(\) API that directly calls the REST interface, or through the NowGraphQLService\(\) API that executes a specified GraphQL query against the REST GraphQL API.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Interact with table data in a ServiceNow instance

The Mobile SDK enables you to interact with data in tables that reside on your ServiceNow instance. You can interact with this data through the ServiceNow REST Table API using the NowTableService\(\) API that directly calls the REST interface, or through the NowGraphQLService\(\) API that executes a specified GraphQL query against the REST GraphQL API.

If you want to return data from multiple tables within a single call, you will need to use the NowGraphQLService\(\) API. If you need to interact with ServiceNow REST APIs other than the Table API, see [Interact with the public REST API on a ServiceNow instance](mobsdk-and-interact-rest_api.md).

## Using NowGraphQLService to interact with ServiceNow tables

The [NowGraphQLService](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowGraphQLService/concept/NowGQLServiceAndroidInterface.md#) class provides methods that enable you to construct and execute GraphQL queries on a specified table within your ServiceNow instance if the logged in user has the proper authorization. You can define all CRUD operations within your GraphQL query.

The following example shows how to import the NowData framework and then initialize a NowGraphQLService object that you can then use to interact with tables in your ServiceNow instance.

```
/**
 * Helper class used to handle different Now service instances.
 */
@Singleton
class SdkManager @Inject constructor() {

    private var nowGraphQLService: NowGraphQLService? = null

    /**
     * Create the NowGraphQLService once in the lifetime of the application inside the Application class or another manager class
     * that will be injected into other classes via dagger/hilt.
     * NowGraphQLService should be created after initializing the NowSDK
     */
    suspend fun getNowGraphQLService(): NowGraphQLService? {
        if (nowGraphQLService != null) return nowGraphQLService

        return NowDataSDK.makeGraphQLService(URL("https://instance-name.service-now.com")).getOrThrow()
            .also { this.nowGraphQLService = it }
    }
}
```

This example shows how to obtains published KB articles using a GraphQL query.

```
suspend fun loadList() = withContext(Dispatchers.IO) {
    val kbArticlesQuery = """
    { 
        GlideRecord_Query {
            kb_knowledge(queryConditions: "active=true^ORDERBYpublishedDESC"
            pagination:{ limit: 10, offset: 0 }) {
                _results {
                    sys_id { value },
                    number { displayValue },
                    short_description { displayValue },
                    author { displayValue }
                    published { displayValue }
                }
            }
        }
     }
 """
    val graphQLService = sdkManager.getNowGraphQLService()

    //graphQLService?.graphQLRequest(kbArticlesQuery)?.execute() can also be used
    graphQLService?.graphQLRequest(kbArticlesQuery)?.enqueue(
        { response ->
            response.body?.let {
                val resultString = String(it)
            }

        }, { nowDataError ->
            //handle error
        })
}
```

## Using NowTableService to interact with ServiceNow tables

The [NowTableService](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowTableService/concept/NowTableServiceAndroidInterface.md#) class provides methods to perform CRUD operations on the records in tables that reside on your ServiceNow instance. Through this interface you can directly access any of the records within any ServiceNow table for which the logged in user is authorized. NowTableService supports dot-walking for reference fields. For example, if a table contains a reference to the User table, the dot-walked value `user.name` returns the name of the user.

When returning the requested data, all applicable Access Control Lists \(ACLs\) are applied to the data, which may result in fewer results than expected, or authorization errors if the authenticated user does not have access rights to the specified table.

The following example shows how to import the NowData framework and then initialize a NowTableServce object that you can then use to interact with ServiceNow instance tables.

```
/**
 * Helper class used to handle different Now service instances. It has an application scope or is Singleton
 */
@Singleton
class SdkManager @Inject constructor() {

    private var nowTableService: NowTableService? = null

    /**
     * Create the NowTableService once in the lifetime of the application inside the Application class or another manager class
     * that will be injected into other classes via dagger/hilt.
     * NowTableService should be created after initializing the NowSDK
     */
    suspend fun getNowTableService(): NowTableService? {
        if (nowTableService != null) return nowTableService

        return NowDataSDK.makeTableService(URL("https://instance-name.service-now.com")).getOrThrow()
            .also { this.nowTableService = it }
    }
 }    


suspend fun loadCases() = withContext(Dispatchers.IO) {
    val tableService = sdkManager.getNowTableService()

    //configure what data to pass back
    val fetchConfiguration =  FetchConfiguration(Filter("active=true"), 10)

    val response = runCatching {
        tableService?.records(
            "sn_customerservice_case",
            fetchConfiguration
        )?.execute()
    }

    if (response.isSuccess) {
        val resultString = response.getOrNull()?.body?.let { String(it) }
    } else {
        //handle unsuccessful result
    }
}
```

For additional code examples using the available NowTableService methods, refer to the [NowTableService](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowTableService/concept/NowTableServiceAndroidInterface.md#) API documentation.

