---
title: Service Graph Connector for AWS properties
description: Service Graph Connector for AWS properties control the behavior of the connector.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-01"
reading_time_minutes: 11
breadcrumb: [Reference, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for AWS properties

Service Graph Connector for AWS properties control the behavior of the connector.

## Connection properties

These connection properties are available for the Service Graph Connector for AWS.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **AWS** &gt; **Connections**, and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_msd_jq3_c3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws\_lookback\_time\_in\_days

</td><td>

This property is used for record removal. Time in days in which the sys\_object\_source records are queried for the deletion of CIs. The value is automatically updated to 15 after the initial run.Set the value of this property to empty to include all the older records populated by SG-AWS as removal candidates.

**Note:** Do not modify this property if the value is empty.

-   Type: integer
-   Default value: empty

</td></tr><tr><td>

config\_aggregator\_name

</td><td>

Enter the name of the configuration aggregator.-   Type: string
-   Default value: empty

</td></tr><tr><td>

config\_aggregator\_account

</td><td>

Enter the AWS account where the configuration aggregator is configured.-   Type: string
-   Default value: empty

</td></tr><tr><td>

config\_aggregator\_region

</td><td>

Enter the AWS region in which the configuration aggregator is configured.-   Type: string
-   Default value: empty

</td></tr><tr><td>

sts\_role

</td><td>

Enter the AWS STS role name.-   Type: string
-   Default value: empty

</td></tr><tr><td>

aws\_rotate\_keys

</td><td>

Set the property to `true` to enable the AWS key rotation process.-   Type: true \| false
-   Default value: `false`

</td></tr><tr><td>

aws\_rotate\_keys\_status

</td><td>

The AWS key rotation status.-   Type: string
-   Default value: empty

</td></tr><tr><td>

aws\_rotate\_keys\_date

</td><td>

Enter the AWS key rotation date.-   Type: string
-   Default value: empty

</td></tr><tr><td>

aws\_rotate\_keys\_period

</td><td>

Enter the AWS key rotation period \(in days\).-   Type: integer
-   Default value: 90

</td></tr><tr><td>

aws\_rotate\_keys\_error\_notify\_user

</td><td>

Enter the comma-separated list of the email addresses of recipients to be sent notifications about AWS key rotation errors.-   Type: string
-   Default value: empty

</td></tr><tr><td>

aws\_rotate\_keys\_error\_notify\_group

</td><td>

Enter the comma-separated list of the ServiceNow email groups to be sent notifications about AWS key rotation errors.-   Type: string
-   Default value: empty

</td></tr><tr><td>

org\_name

</td><td>

Enter the name of the AWS organization.-   Type: string
-   Default value: &lt;ORG\_NAME&gt;

</td></tr><tr><td>

org\_description

</td><td>

Enter the description of AWS organization.-   Type: string
-   Default value: empty

</td></tr><tr><td>

org\_account\_id

</td><td>

Enter the AWS account ID that is used to identify the AWS organization.-   Type: string
-   Default value: &lt;ORG\_ID&gt;

</td></tr><tr><td>

management\_account\_id

</td><td>

Enter the AWS account ID that is used for the management account. This property is required only if the ServiceNow user is created in a designated account.-   Type: string
-   Default value: empty

</td></tr><tr><td>

u\_connection\_alias\_id

</td><td>

The ServiceNow sys\_id for the connection alias.-   Type: string
-   Default value: empty

</td></tr><tr><td>

standalone\_account\_id

</td><td>

Enter the AWS account ID for standalone setup. This property is required only if you set up AWS on a standalone account.-   Type: string
-   Default value: empty

</td></tr><tr><td>

gov\_cloud

</td><td>

Set the property to `true` to enable AWS GovCloud. -   Type: true \| false
-   Default value: empty

</td></tr><tr><td>

aws\_account\_partition\_size

</td><td>

Enter the partition size for AWS accounts if parallel loading is enabled. The value must be a numeric value greater than zero.-   Type: integer
-   Default value: empty

</td></tr><tr><td>

ssm\_sendcommand\_windows\_name

</td><td>

Enter the SSM document name for the SendCommand for Windows.-   Type: string
-   Default value: empty

</td></tr><tr><td>

ssm\_sendcommand\_linux\_name

</td><td>

Enter the SSM document name for the SendCommand for Linux.-   Type: string
-   Default value: empty

</td></tr><tr><td>

ssm\_eks\_names\_document

</td><td>

Enter the SSM document name for the EKS data source.-   Type: string
-   Default value: empty

</td></tr><tr><td>

ssm\_eks\_shell\_document

</td><td>

Enter the SSM document name for EKS-Full data source.-   Type: string
-   Default value: empty

</td></tr><tr><td>

regions

</td><td>

Enter the comma-separated list of AWS regions.-   Type: string
-   Default value: empty

</td></tr><tr><td>

s3\_account\_id

</td><td>

Enter the numeric identifier of the AWS account that hosts the Amazon Simple Storage Service \(Amazon S3\) bucket.-   Type: integer
-   Default value: empty

</td></tr><tr><td>

s3\_bucket\_name

</td><td>

Enter the name of the Amazon S3 bucket that collects the details from Amazon EC2 instances.-   Type: string
-   Default value: empty

</td></tr><tr><td>

s3\_region

</td><td>

Enter the region where the Amazon S3 bucket is set up.-   Type: string
-   Default value: empty

</td></tr></tbody>
</table>## Default system properties

These default system properties are available for the Service Graph Connector for AWS.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_tgy_zlj_c3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_aws\_integ.create\_server\_record\_even\_if\_SSM\_disabled

</td><td>

This property controls server creation with or without SSM enabled on the instance. Set the property to `true` to create server records when SSM is disabled on the instance.-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.eks\_document\_processing\_time

</td><td>

Enter the time \(in milliseconds\) required to process the EKS SendCommand document, during which time the data source thread waits.-   Type: integer
-   Default value: `100`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.enableOptimizedDeletion

</td><td>

Set the property to `true` to enable optimized deletion using the Integration Commons record removal API.During parallel data loading, delete jobs are created only for delta loads, not for full data loads.

-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.global\_generic\_resource\_region

</td><td>

Set the region that has the configuration recorder that can record global resources such as IAM user and IAM group.

 Global generic resources are imported only when the region is set.

 -   Type: string
-   Default value: empty
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.is\_software\_inventory\_enabled

</td><td>

**Important:** This property is not supported in Service Graph Connector for AWS version 2.10.0 and later.

Set the property to `true` if SG-AWS-Software-Inventory is enabled to improve the performance of SG-AWS-SendCommand.-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.load\_all\_images

</td><td>

Set the property to `true` to run the DescribeImages API for all images that are included in the SG-AWS-Image-Id data source. Set the property to `false` to run the DescribeImages API only for images without names.-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.save\_payload\_as\_attachment

</td><td>

Option to save the REST responses as attachments. Set this property to `true` if the payload size is greater than 10 MB.-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.sgaws\_config\_list\_discovered\_resource\_count

</td><td>

Set the number of resource IDs for the list discovered API. The default value is 20, and the maximum value is 769.-   Type: integer
-   Default value: `20`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.sgaws\_config\_list\_discovered\_retry\_count

</td><td>

Set the retry count after a failure of the list discovered API.-   Type: integer
-   Default value: `100`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.sgaws\_ssm\_list\_cmd\_retry\_count

</td><td>

Set the retry count after a failure of the SendCommand API.-   Type: integer
-   Default value: `200`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.use\_aggregator\_configured\_accounts

</td><td>

Set the property to `true` to import CIs only from the aggregator configured accounts, not from all the member accounts.-   Type: true \| false
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.u\_sgaws\_csv\_supported\_db

</td><td>

Enter the list of database applications \(such as MySQL and Postgres\) that are supported for detection using the SSM SendCommand.-   Type: string
-   Default value: \{"mysql":"mysql"\}
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.linux\_TCP\_Established\_Status

</td><td>

-   Type: string
-   Default value: ESTABLISHED \| TIME\_WAIT \| CLOSE\_WAIT
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.linux\_TCP\_Listener\_Status

</td><td>

-   Type: string
-   Default value: LISTEN
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.windows\_TCP\_Established\_Status

</td><td>

-   Type: string
-   Default value: ESTABLISHED\|HERGESTELLT
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_aws\_integ.windows\_TCP\_Listener\_Status

</td><td>

-   Type: string
-   Default value: LISTENING\|ABHÖREN
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Custom system properties

You can create these custom system properties for the Service Graph Connector for AWS. These properties must be created in the Service Graph Connector for AWS application scope. The custom properties that you create are listed in the System Properties \[sys\_properties\] table. For more information about creating custom system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

<table id="table_r43_g5k_c3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_aws\_integ.eks\_chunk\_size

</td><td>

Enter the number of EKS records per batch. The value of this property can be reduced if the import row size leads to transformation errors.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ssm\_managed\_instance\_inventory\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-Software-Inventory data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ssm\_managed\_instance\_inventory\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-Software-Inventory data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.generic\_resource\_\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-Generic-Resources data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.generic\_resource\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-Generic-Resources data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.eks\_cluster\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-EKS-Cluster data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.eks\_cluster\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-EKS-Cluster data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_subnet\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-Subnets data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_subnet\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-Subnets data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_network\_interface\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-Network-Interface data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_network\_interface\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-Network-Interface data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_volume\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-Storage-Volume data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_volume\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-Storage-Volume data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_instance\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-EC2 data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_instance\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-EC2 data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.rds\_db\_instance\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-RDS data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.rds\_db\_instance\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-RDS data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.s3\_bucket\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-S3 data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.s3\_bucket\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-S3 data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.api\_gateway\_v2\_api\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-API-Gateway data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.api\_gateway\_v2\_api\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-API-Gateway data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_security\_group\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-Security-Group data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_security\_group\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-Security-Group data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_vpc\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-VPC data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.ec2\_vpc\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-VPC data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.elastic\_load\_balancing\_load\_balancer\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-ELB-V1 data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.elastic\_load\_balancing\_load\_balancer\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-ELB-V1 data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.elastic\_load\_balancing\_v2\_load\_balancer\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-ELB-V2 data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.elastic\_load\_balancing\_v2\_load\_balancer\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-ELB-V2 data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.lambda\_function\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-Lambda data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.lambda\_function\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-Lambda data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.dynamo\_db\_table\_batch\_get\_aggregate\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_AGGREGATE\_RESOURCE\_CONFIG API response for the SG-AWS-DynamoDb data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.dynamo\_db\_table\_batch\_get\_resource\_config\_batch\_size

</td><td>

Set the batch size of the BATCH\_GET\_RESOURCE\_CONFIG API response for the SG-AWS-DynamoDb data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_aws\_integ.throttling\_min\_wait\_time\_in\_ms

</td><td>

Set the minimum wait time \(in milliseconds\) before retrying after an API failure due to throttling or rate limiting issues.-   Type: integer
-   Default value: `10,000`

</td></tr><tr><td>

sn\_aws\_integ.throttling\_max\_wait\_time\_in\_ms

</td><td>

Set the maximum waiting period \(in milliseconds\) after an API failure due to throttling or rate limiting issues.-   Type: integer
-   Default value: `160,000`

</td></tr><tr><td>

sn\_aws\_integ.config\_db\_load\_enabled

</td><td>

Enter the list of import set table names for which the DB Load is to be enabled to improve performance.-   Type: string
-   Default value: empty

</td></tr></tbody>
</table>## Related content

[Data mapping for Service Graph Connector for AWS](cmdb-data-mapping-aws.md)

[CMDB classes targeted in Service Graph Connector for AWS](cmdb-aws-classes.md)

**Parent Topic:**[Service Graph Connector for AWS reference](../concept/sgc-cmdb-aws-reference.md)

