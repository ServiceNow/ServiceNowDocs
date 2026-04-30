---
title: Mobile fetch types
description: Fetch type settings determine when data is loaded in your screens. Change your fetch type to optimize load time performance for your screens.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Mobile fetch types

Fetch type settings determine when data is loaded in your screens. Change your fetch type to optimize load time performance for your screens.

|Fetch type|Description|Usage|
|----------|-----------|-----|
|Prefetch|Prefetch is the default fetch type for new screens, except form and details. This option pre-loads record screen data while when your user accesses a list, calendar, or record screen. Lists may take longer to load, but form load time is faster.|This fetch type is the default for most screens. Use this fetch type when the form and form segments do not take much additional time to load.|
|Background|The app makes a background network request to load embedded screens or form segments. Embedded screens and form segments load instantly once the background request completes.|Use this fetch type when a screen is not the first loaded, but one your users are likely to navigate to. For example, a related list associated with a form.|
|On Demand|The app makes a network request to load the screen only when your users navigate to it.|Use this fetch type when a screen is not expected to be used often.|
|Dynamic|The screens for the first 10 rows load as described in the **prefetch** type. After 10 first rows, the app loads screens as defined in the**on demand** fetch type. This option is the default for form and details screens. You can change the number of rows loaded with **prefetch** by changing the value of the **Dynamic prefetch count** field.|Use this fetch type when large lists load too slowly using the **prefetch** fetch type.|

-   **[Change the fetch type for a screen](../task/change-fetch-type.md)**  
Change the fetch type of a screen to change when the app loads its data.

