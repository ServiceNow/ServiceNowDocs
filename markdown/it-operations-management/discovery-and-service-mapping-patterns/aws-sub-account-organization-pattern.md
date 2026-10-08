---
title: AWS sub account Organizations pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS sub-accounts in your organization on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/aws-sub-account-organization-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [Amazon AWS Sub Account, AWS sub-account, AWS Organizations, AWS discovery, AWS patterns, Sub Account pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS sub account Organizations pattern-based discovery

Discovery and Service Mapping Patterns finds AWS sub-accounts in your organization on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Sub Account \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Account Id \[account\_id\]|Unique identifier \(ID\) of the account.|
|Object ID \[object\_id\]|Unique ID of the account.|
|Datacenter Type \[datacenter\_type\]|Type of datacenter. The value is set to **AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]**.|
|Name \[name\]|User-friendly name of the account.|
|Is management account \[is\_master\_account\]|Indicates if this account is the management account of the organization.|
|Account Email \[account\_email\]|Email address of the AWS service account.|
|Datacenter URL \[datacenter\_url\]|URL of the datacenter used for discovery.|
|Install Status \[install\_status\]|Install status of the account, derived from the account state.|
|Operational status \[operational\_status\]|Operational status of the account, derived from the account state.|
|Parent account \[parent\_account\]|References the management Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] record.|

## CI relationships and references

The Amazon AWS - Sub Account \(LP\) pattern creates the following relationships and references to support AWS sub account discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Members::Member of|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Parent account \[parent\_account\]|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## AWS Tag discovery

The Amazon AWS - Sub Account \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

