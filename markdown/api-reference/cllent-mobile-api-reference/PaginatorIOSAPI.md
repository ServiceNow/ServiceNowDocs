---
title: Paginator API - iOS
description: The Paginator class provides methods for iterating through a record set returned by a call to the ServiceNow Table API through the NowTableService. It is the object that is returned by the NowTableService paginator\(\) methods. Do not call this method outside of that environment.Fetches the first page of the return results.Fetches the last page of the return results.Fetches the next page of the return results.Fetches the previous page of the return results.Resets the Paginator back to the first page but doesn't return the first page of the return results.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# Paginator API- iOS

The Paginator class provides methods for iterating through a record set returned by a call to the ServiceNow Table API through the NowTableService. It is the object that is returned by the NowTableService paginator\(\) methods. Do not call this method outside of that environment.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

hasNext

</td><td>

Boolean

</td><td>

Flag that indicates whether there is a next page to fetch.Valid values:

-   true: Next page is available.
-   false: Next page is not available.

</td></tr><tr><td>

hasPrevious

</td><td>

Boolean

</td><td>

Flag that indicates whether there is a previous page to fetch.Valid values:

-   true: Previous page is available.
-   false: Previous page is not available.

</td></tr><tr><td>

isBusy

</td><td>

Boolean

</td><td>

Flag that indicates whether the Paginator object is busy fetching data.Valid values:

-   true: Publisher is busy.
-   false: Publisher is not busy.

</td></tr><tr><td>

isFinished

</td><td>

Boolean

</td><td>

Flag that indicates whether the Paginator object is finished. When the paginator is configured to finish, the Paginator object's publisher finishes when the last page has been fetched. A Paginator object cannot fetch any pages after it finishes. For additional information, see the description of the **publisherShouldFinish** parameter.Valid values:

-   true: Publisher is finished.
-   false: Publisher is not finished.

</td></tr><tr><td>

itemsPerPage

</td><td>

Integer

</td><td>

Number of items to fetch per page.Default: 20

</td></tr><tr><td>

numberOfPages

</td><td>

Integer

</td><td>

Total number of pages within the record set.When the Paginator object has not yet fetched any pages, this parameter is set to `Int.max`. After an initial request has been made to the ServiceNow instance, the number of pages is updated to the actual number of pages received from the ServiceNow instance.

</td></tr><tr><td>

page

</td><td>

Integer

</td><td>

Current page within the paginated record set.

</td></tr><tr><td>

publisher

</td><td>

String

</td><td>

Publisher that supplies the stream of paginated data to the subscribers.**Note:** By default, the publisher does not finish. To change this behaviour, set the **publisherShouldFinish** property to `true`.

</td></tr><tr><td>

publisherShouldFinish

</td><td>

Boolean

</td><td>

Flag that indicates whether to stop the Paginator object's publisher when the last page has been fetched. A Paginator object cannot fetch any pages after it finishes.Valid values:

-   true: Once the last page is fetched, the publisher is released from providing additional data. The reset\(\) method is no longer functional.
-   false: The publisher is never finished and all methods are fully operational regardless of navigation.

Default: false

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## Paginator - first\(\) throws

Fetches the first page of the return results.

If this method can't fetch the first page, it throws a `PaginationError`.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
class PaginatorTestViewModel<T: JSONRepresentable>: ObservableObject {
  @Published var result: Result<String, Error>?
  private let paginator: Paginator<T>
  private var subscriptions = Set<AnyCancellable>()

  init(paginator: Paginator<T>) {
    self.paginator = paginator
    subscribeToPaginator()
  }

  private func subscribeToPaginator() {
    paginator.publisher
      .receive(on: DispatchQueue.main)
      .sink { [weak self] comp in
        if case .failure(let error) = comp {
          self?.result = .failure(error)
        }
      } receiveValue: { [weak self] jsonRepresentable in
        self?.result = .success(jsonRepresentable.jsonDescription)
      }
      .store(in: &subscriptions)
  }

  func first() {
    result = nil
    do {
      try paginator.first()
    } catch {
      self.result = .failure(error)
    }
  }
}
```

## Paginator - last\(\) throws

Fetches the last page of the return results.

If this method can't fetch the last page, it throws a `PaginationError`.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
…
func last() {
  result = nil
  do {
    try paginator.last()
  } catch {
    self.result = .failure(error)
  }
}
…
```

## Paginator - next\(\) throws

Fetches the next page of the return results.

If there are no more pages to fetch, the method throws a `PaginationError`.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
…
func next() {
  result = nil
  do {
    try paginator.next()
  } catch {
    self.result = .failure(error)
  }
}
…
```

## Paginator - previous\(\) throws

Fetches the previous page of the return results.

If the method can't fetch the previous page, it throws a `PaginationError`.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
…
func previous() {
  result = nil
  do {
    try paginator.previous()
  } catch {
    self.result = .failure(error)
  }
}
…
```

## Paginator - reset\(\)

Resets the Paginator back to the first page but doesn't return the first page of the return results.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
…
func reset() {
  result = nil
  paginator.reset()
}
…
```

