---
title: Paginate return results record sets
description: Within the Mobile SDK, when interacting with data from a ServiceNow instance through a REST endpoint using the NowTableService, you can create a Paginator object that enables you to iterate over the records in the return results.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Interact with table data in a ServiceNow instance, Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Paginate return results record sets

Within the Mobile SDK, when interacting with data from a ServiceNow instance through a REST endpoint using the NowTableService, you can create a Paginator object that enables you to iterate over the records in the return results.

You typically use paginated return results to provide infinite scroll capabilities for table records or to simplify page iteration of results in general.

The NowTableService class provides a method for creating a Paginator object that contains the return results from a REST endpoint call:

[NowTableService - paginator\(tableName: String, configuration: FetchConfiguration\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowTableService/concept/NowTableServiceAndroidInterface.md#)

This method creates a Paginator object that contains the specified records from the specified table in raw data format. If you do not include the FetchConfiguration object in the call, it contains all records and their associated fields in the return results.

The returned Paginator object provides the following methods that enable you to page through the returned records. You must first call the observe\(\) function to set the Paginator's callback.

-   first\(\)
-   hasNext\(\)
-   hasPrevious
-   isBusy
-   last\(\)
-   next\(\)
-   observe\(\)
-   previous\(\)
-   reset\(\)

**Note:** Some Paginator methods may throw an exception, such as when there are no more pages to fetch.

The following code example shows how to paginate through data.

```
// Configure what data to pass back
val fetchConfiguration = FetchConfiguration(Filter("active=true"), 10)

val paginator = getNowTableService()?.paginator(
  "sn_customerservice_case", fetchConfiguration)
  ?.observe(object : PaginatorCallBack<ByteArray> {
    override fun onSuccess(response: Response<List<ByteArray>>) {
      val byteArray = response.rawBody ?: throw Exception("Null Result")
      val responseString = String(byteArray)
    }

    override fun onFailure(e: NowDataError) {
      // Handle error
    }
  })

// Use paginator operators to navigate. Example
while (paginator.hasNext() && !paginator.isBusy()) {
  paginator.next()
}
```

