---
title: Paginate return results record sets
description: Within the Mobile SDK, when interacting with data from a ServiceNow instance through a REST endpoint using the NowTableService, you can create a Paginator object that enables you to iterate over the records in the return results.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Interact with table data in a ServiceNow instance, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Paginate return results record sets

Within the Mobile SDK, when interacting with data from a ServiceNow instance through a REST endpoint using the NowTableService, you can create a Paginator object that enables you to iterate over the records in the return results.

You typically use paginated return results to provide infinite scroll capabilities for table records presented inside a UITableView, a UICollectionView \(UIKit\), or a List \(SwiftUI\), or to simplify page iteration of results in general.

The NowTableService class provides two methods for creating a Paginator object that contains the return results from a REST endpoint call:

-   [NowTableService - paginator\(from tableName: String, configuration: FetchConfiguration? = nil\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowTableService/concept/NowTableServiceiOSAPI.md#)

    This method creates a Paginator object that contains the specified records from the specified table. If you do not include the FetchConfiguration object, it contains all records and their associated fields in the return results. This method returns raw data.

-   [NowTableService - paginator&lt;Model: Decodable&gt;\(from tableName: String, path: String = Constants.resultPath, coder: Coder = .default, configuration: FetchConfiguration? = nil\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowTableService/concept/NowTableServiceiOSAPI.md#)

    This method creates a Paginator object that contains the specified records from the specified table. If you do not include the FetchConfiguration object, it contains all records and their associated fields in the return results. This method returns Codable models and enables you to define a custom `Coder` for Codable models that require custom decoding. You can supply a custom `JSONDecoder` by supplying a `NowData.Coder.custom` enumeration value that contains the custom `JSONDecoder` and `JSONEncoder`.


The paginator type is determined by the [Generics](https://docs.swift.org/swift-book/LanguageGuide/Generics.html) and the compiler [type inference](https://www.swiftbysundell.com/basics/type-inference/).

In the following example, the compiler infers that `service.paginator(…)` returns a paginator of type `Paginator<[User]>`, a paginator that publishes a collection of users, such as, [Codable](https://developer.apple.com/documentation/swift/codable) User structures, through its [Combine](https://developer.apple.com/documentation/combine) publisher.

```
let paginator: Paginator<[User]> = service.paginator(from: "sys_user", path: "result")
```

After obtaining a Paginator object, subscribe to its publisher to start receiving data.

```
paginator.publisher
  .subscribe(on: DispatchQueue.global())
  .receive(on: DispatchQueue.main)
  .sink { ... }
  .store(in: &subscriptions)
```

The returned Paginator object provides the following methods that enable you to page through the returned records:

-   first\(\)
-   last\(\)
-   next\(\)
-   previous\(\)
-   reset\(\)

**Note:** Some Paginator methods may throw an exception, such as when there are no more pages to fetch.

In addition, the Paginator object provides properties that enable you to obtain insights into the paginated data. For additional details on these properties and the available methods, see `[Paginator API - iOS](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/Paginator/concept/PaginatorIOSAPI.md#)`.

