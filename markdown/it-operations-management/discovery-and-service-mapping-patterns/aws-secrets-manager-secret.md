---
title: AWS Secrets Manager Secret pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Secrets Manager Secrets on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-secrets-manager-secret.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 4
keywords: [AWS Secrets Manager Secret, AWS Secrets Manager Secret discovery, AWS patterns, Secrets Manager pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Secrets Manager Secret pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Secrets Manager Secrets on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns]().

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [AWS Resource Inventory discovery with Patterns]().

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern]().


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - Secrets Manager Secret - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The Amazon Resource Name \(ARN\) of the secret.|
|Name \[name\]|Name of the secret.|
|Primary Region \[primary\_region\]|The primary Region for the secret, for multi-Region secrets.|
|Owning Service \[owning\_service\]|The name of the service that created the secret.|
|Rotation Enabled \[rotation\_enabled\]|Indicates whether automatic rotation is enabled for the secret.|
|Kms Key ID \[kms\_key\_id\]|The ARN or alias of the KMS key used to encrypt the secret.|
|Description \[description\]|Description of the secret.|
|Rotation Lambda Arn \[rotation\_lambda\_arn\]|The ARN of the Lambda function used to rotate the secret.|
|Rotation Days \[rotation\_days\]|The number of days between automatic scheduled rotations of the secret.|
|Schedule Expression \[schedule\_expression\]|A cron or rate expression that defines the schedule for rotating the secret.|
|Duration \[duration\]|The length of the rotation window during which Secrets Manager rotates the secret.|
|Secret Version To Stages \[secret\_version\_to\_stages\]|A map of the secret versions and their staging labels.|
|Created Date \[created\_date\]|Date and time when the secret was created.|
|Last Changed Date \[last\_changed\_date\]|Date and time when the secret was last changed.|
|Last Accessed Date \[last\_accessed\_date\]|Date and time when the secret was last accessed.|
|Last Rotated Date \[last\_rotated\_date\]|Date and time when the secret was last rotated.|
|Configuration Item \[configuration\_item\]|References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.|

## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - Secrets Manager Secret - Extended Inventory \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the secret.|
|Object ID \[object\_id\]|The ARN of the secret.|
|Resource type \[resource\_type\]|Type of resource. The value is set to **AWS::SecretsManager::Secret**.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

## CI relationships

The Amazon AWS - Secrets Manager Secret - Extended Inventory \(LP\) pattern creates the following relationships and references to support AWS Secrets Manager Secret discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|AWS Secrets Manager Secret \[cmdb\_aws\_secrets\_manager\_secret\]|Configuration Item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|

## AWS Tag discovery

The Amazon AWS - Secrets Manager Secret - Extended Inventory \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

