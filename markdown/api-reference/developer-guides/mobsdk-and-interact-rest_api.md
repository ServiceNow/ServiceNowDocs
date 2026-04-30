---
title: Interact with the public REST API on a ServiceNow instance
description: The Mobile SDK provides functionality that enables Android applications to call the public REST API on a ServiceNow instance.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Interact with the public REST API on a ServiceNow instance

The Mobile SDK provides functionality that enables Android applications to call the public REST API on a ServiceNow instance.

Using the [NowAPIService](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowAPIService/concept/NowAPIServiceAndroidInterface.md#) API you can interact with any of the base ServiceNow public [REST APIs](../../../../../build/applications/concept/api-rest.md), or create custom REST APIs within the instance and call those from your Android application.

Before making a call to a ServiceNow REST API, you must call the[makeNowAPIService\(\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowDataSDK/concept/NowDataSDKAndroidAPI.md#) method to create an instance of the service. The service instance is returned in the callback if successful otherwise, an error is thrown.

The following shows how to initialize a NowAPIService object:

```
/**
 * Helper class used to handle different Now service instances. It has an application scope or is Singleton
 */
@Singleton
class SdkManager @Inject constructor() {

    private var nowApiService: NowAPIService? = null

    /**
     * Create the NowAPIService once in the lifetime of the application inside the Application class or another manager class
     * that will be injected into other classes via dagger/hilt.
     * NowAPIService should be created after initializing the NowSDK
     */
    suspend fun getNowApiService(): NowAPIService? {
        if (nowApiService != null) return nowApiService

        return NowDataSDK.makeAPIService(URL("https://instance-name.service-now.com")).getOrThrow()
            .also { this.nowApiService = it }
    }

}
```

Once the NowAPIService object is initialized, use the NowAPIService [data\(\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowAPIService/concept/NowAPIServiceAndroidInterface.md#) method to specify the REST endpoint to call and all of its associated parameters:

```
 suspend fun makeNowApiCall() {
  val apiService = sdkManager.getNowApiService()

  val apiPath = "api/now/table/sn_customerservice_case"
  val endpoint = NowAPIService.Endpoint(HttpMethod.GET, apiPath, true)
  val fieldNames = "sys_id,number,short_description,number,priority,state," +
    "opened_at,account.name,account.number,contact.name,contact.email," +
    "contact_type,assignment_group.name,assigned_to.name"

  val queryParamsMap = mapOf("sysparm_fields" to fieldNames, "sysparm_limit" to "10")

  val queryParams = QueryParams.Builder().addAll(queryParamsMap).build()

  val response = runCatching {
    apiService?.data(endpoint = endpoint, queryParams = queryParams)?.execute()
  }

  if (response.isSuccess) {
    val resultString = response.getOrNull()?.body?.let { String(it) }
  } else {
    // Handle error
  }
}
```

