---
title: PADomainUtils - Global
description: The PADomainUtils API enables you to copy Performance Analytics records between different domains on the same instance.Instantiates a new PADomainUtils object to move or copy Performance Analytics records from the global domain.Instantiates a new PADomainUtils object to move or copy Performance Analytics records from the specified domain.Copies Performance Analytics records to a different domain.Copy a dashboard to another domain.Copies a Performance Analytics scheduled data collection job record to another domain.Evaluate if you can write to a specific record identified by table and sys\_id.Moves Performance Analytics records to a different domain.Use this method to move or copy only foundational records in a hybrid domain configuration.Use this method before copying records to set the sys\_override value of the new record to the original parent record.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PADomainUtils- Global

The PADomainUtils API enables you to copy Performance Analytics records between different domains on the same instance.

Use this API in server scripts to copy Performance Analytics records such as indicators, breakdowns, and dashboards, to different domains. This API enables you to create a Performance Analytics record in one domain and copy that record to any number of additional domains.

**Note:** This API cannot copy records into the Global domain.

**Warning:** When configuration records are moved to another domain, scores will not be accessible.

To use PADomainUtils, you must satisfy these requirements:

-   Performance Analytics must be enabled.
-   The user running the script must have the admin role.
-   The instance must use domain separation.
-   The script must be run from the global domain.
-   When moving or copying records, the source and target domains must be different.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PADomainUtils - PADomainUtils\(\)

Instantiates a new PADomainUtils object to move or copy Performance Analytics records from the global domain.

Use the PADomainUtils\(String domainFrom\) constructor instead when moving or copying records from a domain other than the global domain.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
// PADomainUtils initialized with the global domain
var globalUtils = new SNC.PADomainUtils();
```

## PADomainUtils - PADomainUtils\(String domainFrom\)

Instantiates a new PADomainUtils object to move or copy Performance Analytics records from the specified domain.

Use the PADomainUtils\(\) constructor instead when moving or copying from the global domain.

|Name|Type|Description|
|----|----|-----------|
|domainFrom|String|The domain to copy records from.|

```
// c90d4b084a362312013398f051272c0d is the sys id of the ACME domain
var acmeUtils = new SNC.PADomainUtils('c90d4b084a362312013398f051272c0d');
```

## PADomainUtils - copy\(String runAs\)

Copies Performance Analytics records to a different domain.

To copy dashboards or scheduled jobs, see [copyDashboard](c_PADomainUtils.md#) and [copyJob](c_PADomainUtils.md#).

|Name|Type|Description|
|----|----|-----------|
|runAs|String|User whose domain you want to copy records to.|

|Type|Description|
|----|-----------|
|void| |

```
// copy all the Performance Analytics records from global to user's domain
var pa = new SNC.PADomainUtils();
pa.copy('09ff3d105f231000b12e3572f2b4775d');
```

## PADomainUtils - copyDashboard\(String dashboardId, String runAs\)

Copy a dashboard to another domain.

|Name|Type|Description|
|----|----|-----------|
|dashboardId|String|Sys\_id of the dashboard to copy.|
|runAs|String|User whose domain you want to copy the dashboard to.|

|Type|Description|
|----|-----------|
|void| |

```
//Copy Incident Management dashboard from global to user's domain
var pa = new SNC.PADomainUtils();
pa.copyDashboard('a64b7031d7201100b96d45a3ce610335','09ff3d105f231000b12e3572f2b4775d');
```

## PADomainUtils - copyJob\(String paJob, String runAs\)

Copies a Performance Analytics scheduled data collection job record to another domain.

|Name|Type|Description|
|----|----|-----------|
|paJob|String|Sys\_id of a Performance Analytics scheduled data collection job \[sysauto\_pa\] record.|
|runAs|String|User whose domain you want to copy the job to.|

|Type|Description|
|----|-----------|
|String|Error message if an error occurs, or an empty string if there is no error.|

```
// No source domain needs to be set
var pa = new SNC.PADomainUtils();
// copy the '[PA Incident] Daily Data Collection job'
// set the 'run as' of the new record to be the 'acme.itil' user
// first argument is the sys_id of the sysauto_pa record
// the second is the sys_id of the acme.itil user record
pa.copyJob('82ba2023d7101100b96d45a3ce6103cd','797d14341f1310005a3637b8ec8b7010');
```

## PADomainUtils - isWriteable\(String table, String id\)

Evaluate if you can write to a specific record identified by table and sys\_id.

|Name|Type|Description|
|----|----|-----------|
|table|String|The name of the table containing the record to query, such as pa\_indicators.|
|id|String|The sys\_id of the record to query.|

|Type|Description|
|----|-----------|
|Boolean|Indicates that you can write to the specified record. Returns true if the record exists within the domain of the current user. Returns false if the record does not exist, or is in a different domain.|

```
var pa = new SNC.PADomainUtils();
pa.isWriteable('pa_incidents','cd8125b5140012007665a83e633b028d');
```

## PADomainUtils - move\(String runAs\)

Moves Performance Analytics records to a different domain.

|Name|Type|Description|
|----|----|-----------|
|runAs|String|The user whose domain you want to copy records to.|

|Type|Description|
|----|-----------|
|void| |

```
// move all the Performance Analytics records from the global to the customers domain
var pa = new SNC.PADomainUtils();
pa.move('774190f01f1310005a3637b8ec8b70ef')
```

## PADomainUtils - setFoundation\(Boolean foundation\)

Use this method to move or copy only foundational records in a hybrid domain configuration.

You can implement a hybrid approach by maintaining some types of record in a parent domain and some types in child domains. Generally, the parent domain contains foundational records and the child domain contains higher-level records, such as widgets. The following types of record are considered foundational records.

-   Bucket groups
-   Buckets
-   Scripts
-   Breakdown sources
-   Indicator sources
-   Filters
-   Breakdowns
-   Managed sources
-   Manual breakdowns
-   Breakdown mappings
-   Breakdown relations

Other Performance Analytics records such as widgets and indicators are not foundational records. Set this method to false to move or copy these additional records as well.

|Name|Type|Description|
|----|----|-----------|
|foundation|Boolean|Indicates if only foundational records should be copied or moved by this PADomainUtils object.|

|Type|Description|
|----|-----------|
|PADomainUtils|The object calling this function.|

```
var pa = new SNC.PADomainUtils().setFoundation(true);
pa.copy('bb6b58b01f1310005a3637b8ec8b70dd');
```

## PADomainUtils - setOverrides\(Boolean overrides\)

Use this method before copying records to set the sys\_override value of the new record to the original parent record.

Using this method enables you to automatically override records in a parent domain. By overriding the parent records, the parent records do not impact the child domain. If the source domain is not the parent of the target domain when copying records, setting the sys\_override value will not have any impact on behavior. You can specify an override only when copying records, not when moving records.

|Name|Type|Description|
|----|----|-----------|
|overrides|Boolean|Indicates that copied records in a child domain should override the source record in the parent domain. This value is true by default.|

|Type|Description|
|----|-----------|
|PADomainUtils|The object calling this function.|

```
var pa = new SNC.PADomainUtils('c90d4b084a362312013398f051272c0d');
pa.setOverrides(false);
pa.copy('bb6b58b01f1310005a3637b8ec8b70dd');
```

