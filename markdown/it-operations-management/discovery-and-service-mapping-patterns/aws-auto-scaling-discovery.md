---
title: AWS Auto Scaling groups discovery with Patterns
description: The Discovery application uses the Amazon AWS - AutoScaling Groups \(LP\) pattern and Auto Scaling extensions to find AWS Auto Scaling groups. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-11-09"
reading_time_minutes: 4
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Auto Scaling groups discovery with Patterns

The ® Discovery application uses the Amazon AWS - AutoScaling Groups \(LP\) pattern and Auto Scaling extensions to find AWS Auto Scaling groups. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Starting with Discovery and Service Mapping Patterns version 1.0.95, the pattern extension is automatically displayed and collects the Auto Scaling tags.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Configure AWS Credentials**

    On your instance, configure credentials of type **AWS Credentials** and set them to **Active**. For more information, see [Access setup for AWS service accounts](../../it-operations-management/concept/access-aws-accounts.md).

-   **Configure a Cloud service account**

    Configure the AWS service account valid in the ServiceNow instance. For more information, see [Set up AWS service accounts.](../../it-operations-management/concept/setup-aws-service-accounts.md)

-   **Configure user permissions to execute the list AWS Auto Scaling groups API call**

    Provide the user permission to run the following API: https://autoscaling.amazonaws.com/?Action=DescribeAutoScalingGroups&amp;Version=2011-01-01

    For more information, see [Amazon AWS Cloud components discovery using patterns.](../../discovery/reference/data-discovered-aws-patterns.md)

-   **Configure Cloud Discovery schedule**

    Create a cloud application schedule for discovering AWS Auto Scaling groups and configure the attributes. Set **Discovery** to **Cloud application**. For more information, see [Create schedules for discovering cloud resources in Cloud Discovery Workspace](../../discovery/task/cloud-operations-disco-create-schedule.md)

-   **Configure AWS Auto Scaling groups**

    Navigate to the Instance Scale Set table and verify that the configurations are set as follows:

    |Element Name|Type|Label|Max Length|
    |------------|----|-----|----------|
    |desired\_capacity|integer|Desired Capacity|32|
    |min\_size|integer|Minimum Size|32|
    |max\_size|integer|Maximum Size|32|
    |health\_check\_type|string|Health Check Type|128|


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - AutoScaling Groups \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Amazon Resource Name \(ARN\) of the Auto Scaling group.|
|Object ID \[object\_id\]|The ARN of the Auto Scaling group.|
|Install Status \[install\_status\]|The install status of Auto Scaling group. Default value is Installed.|
|Operational status \[operational\_status\]|The operational status of Auto Scaling group. Default value is Operational.|
|Desired Capacity \[desired\_capacity\]|The desired size of the group.|
|Maximum Size \[max\_size\]|The maximum size of the group.|
|Minimum Size \[min\_size\]|The minimum size of the group.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The Instance ID of the Virtual Machine.|

![cmdb ci instance scale set and cmdb ci vm instance hosted on cmdb ci aws datacenter which is hosted on cmdb ci cloud service account](../image/aws-auto-scaling-gruop-discovery.png "AWS EC2 Auto Scaling– Class model")

## Relationships

Discovery creates these relationships to support the AWS Auto Scaling groups discovery.

<table id="table_nxq_dcc_x5b"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]

</td><td>

Hosted on::Hosts

</td><td>

Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td></tr><tr><td>

Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]

</td><td>

Hosted on::Hosts

</td><td>

AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]

</td></tr><tr><td>

Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]

</td><td>

\*Managed by::Manages

</td><td>

VM Instance \[cmdb\_ci\_vm\_instance\]**Note:** EC2 VM

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

References

</td><td>

Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]

</td></tr></tbody>
</table>\*Starting with Discovery and Service Mapping Patterns version 1.29.0, the relationship between Instance Scale Set and VM Instance has changed from **Members::Member of** to **Managed by::Manages**.

## Tag discovery

The Amazon AWS - AutoScaling Groups \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|The key of the resource tag.|
|Value \[value\]|The value of the resource tag.|
|Configuration item \[configuration\_item\]|References the Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\] table.|

**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

**Related topics**  


[Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md)

[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

