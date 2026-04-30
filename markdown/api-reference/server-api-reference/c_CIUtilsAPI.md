---
title: CIUtils - Global
description: The CIUtils script include is a utility class that provides methods for working with configuration items \(CI\).Determines which business services are affected by the specific configuration item \(CI\).Determines which business services are affected by the specified task.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CIUtils- Global

The CIUtils script include is a utility class that provides methods for working with configuration items \(CI\).

By default, when traversing CI relationships the system uses a max depth of 10. You can override this value by modifying the glide.relationship.max\_depth property.

The maximum number of items returns is 1000. You can override this value by modifying the glide.relationship.threshold property.

The CIUtils class is available to server-side scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CIUtils - servicesAffectedByCI\(String CI\_sys\_id\)

Determines which business services are affected by the specific configuration item \(CI\).

|Name|Type|Description|
|----|----|-----------|
|CI\_sys\_id|String|The sys\_id of a configuration item \(cmdb\_ci\) to check.|

|Type|Description|
|----|-----------|
|Array|An array of sys\_id values for cmdb\_ci records downstream of \(or affected by\) the specified item.|

This example displays the names of the services affected by the CI items with the name = lnux100.

```
var CIUtil = new CIUtils();
 
//get a server record
var server = new GlideRecord("cmdb_ci_server");
server.addQuery("name", "lnux100");
server.query();
if (server.next()) {
  //get the affected services, array of ids
  var serviceIds = CIUtil.servicesAffectedByCI(server.getUniqueValue());
  for (var i=0; i < serviceIds.length; i++) {
    //get the service record
    var service = new GlideRecord("cmdb_ci_service");
    service.get(serviceIds[i]);
    gs.print(service.getDisplayValue());
  }
}
```

Output:

```
Client Services
IT Services
Bond Trading
```

## CIUtils - servicesAffectedByTask\(GlideRecord task\)

Determines which business services are affected by the specified task.

|Name|Type|Description|
|----|----|-----------|
|task|GlideRecord|Task GlideRecord, for example incident, change\_request, or problem.|

|Type|Description|
|----|-----------|
|Array|List of sys\_id values for CIs downstream of \(or affected by\) the configuration item referenced by the task's cmdb\_ci field.|

This example displays the names of the services affected by the incident INC00050.

```
var CIUtil = new CIUtils();
 
//get an incident record
var inc = new GlideRecord("incident");
inc.addQuery("number", "INC00050");
inc.query();
if (inc.next()) {
  //get the affected services, array of ids
  var serviceIds = CIUtil.servicesAffectedByTask(inc);
  for (var i=0; i < serviceIds.length; i++) {
    //get the service record
    var service = new GlideRecord("cmdb_ci_service");
    service.get(serviceIds[i]);
    gs.print(service.getDisplayValue());
  }
}
```

Output:

```
IT Services
Email
Windows Mobile
Electronic Messaging
Outlook Web Access (OWA)
Blackberry
```

