---
title: CMDB APIs \(CMDB SDK\)
description: Use CMDB APIs to create, update, and read operations on the CMDB. Domain separation is supported in CMDB APIs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB APIs \(CMDB SDK\)

Use CMDB APIs to create, update, and read operations on the CMDB. Domain separation is supported in CMDB APIs.

## CMDB APIs \(CMDB SDK\)

Use the following CMDB APIs to create, update, and read operations on the CMDB:

-   [CMDBGroupAPI - Scoped](https://www.servicenow.com/docs/access?context=c_CMDBGroupAPIScoped&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [CMDBTransformUtil - Global](https://www.servicenow.com/docs/access?context=c_CMDBTransformUtilAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [CMDBUtil - Global](https://www.servicenow.com/docs/access?context=c_CMDBUtilAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [IdentificationEngineScriptableApi](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [IdentificationEngine - Scoped](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

## Domain separation in CMDB APIs

Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.



CMDB APIs are used for accessing the CMDB from a script. CMDB stores the CI and relation information; CMDB is domain separated.

CMDB APIs support the following operations:

-   Create a new CI:

    This operation goes through the Identification and Reconciliation Engine which supports domain separation when creating a CI. The domain of the caller is used for this operation.

-   Update an existing CI:

    This operation goes through the Identification and Reconciliation Engine which supports domain separation when creating a CI. The domain of the caller is used for this operation.

-   Create/Delete relations:

    The cmdb\_rel\_ci table is not domain separated.

-   Query CMDB CI/Query CMDB table:

    Results are filtered by the domain\(s\) visible to the caller.

-   Query CMDB metadata table:

    Metadata information is not domain separated.


## Setting up domain separation for CMDB APIs

If domain separation is enabled for CMDB, then it is also available for CMDB APIs.

## Data separation

Data is stored and domain separated in CMDB. There is no additional work needed from the CMDB API perspective.

## Configuring a domain-separated environment

The configuration is done at the CMDB level.

## If a domain column is present for base system application tables

See the [Domain separation in CMDB Health](cmdb-health-domain-separation.md) topic.

## Tenant domains and application data

There is no application-specific data to manage with CMDB.

**Related topics**  


[Domain separation and Configuration Management Database \(CMDB\)](domain-separation-cmdb.md)

