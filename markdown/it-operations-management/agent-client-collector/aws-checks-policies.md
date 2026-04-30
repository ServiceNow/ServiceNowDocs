---
title: AWS Health Monitoring default checks and policies
description: Agent Client Collector provides the following default checks and policies for AWS monitoring.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [ACC-M default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# AWS Health Monitoring default checks and policies

Agent Client Collector provides the following default checks and policies for AWS monitoring.

<table id="table_rgw_psy_vrb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Usage example

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

aws.metrics-ec2

</td><td>

Returns metrics of all EC2 instances in a AWS Datacenter.

</td><td>

metrics-ec2.rb \(options\)

 -F, --filter FILTER String representation of the filter to filter EC2 instances by tags.

 -b, --batch\_size BATCH\_SIZE Batch size. Number of instances to fetch metrics in parallel. \(Default value: 10\)

</td><td>

`./metrics-ec2.rb -F "{name:tag:environment,values:[ENV1,ENV2]} {name:tag:Name,values:[Instance1,Instance2]}"`

 Provide the filter string along with double quotes \(""\) around the filter parameter.

 Set the **batch\_size** parameter according to the agent environment.

</td></tr><tr><td>

Metric

</td><td>

aws.metrics-ebs

</td><td>

Returns metrics of all EBS volumes in an AWS datacenter.

</td><td>

metrics-ebs.rb \(options\)

 -F, --filter FILTER String representation of the filter to filter EBS Volumes by Tags.

 -b, --batch\_size BATCH\_SIZE Batch size. Number of volumes to fetch metrics parallelly. \(Default value: 10\)

</td><td>

`./metrics-ebs.rb -F "{name:tag:environment,values:[ENV1,ENV2]} {name:tag:Name,values:[Volume1,Volume2]}"`

 Provide filter string along with double quotes \(""\) for the filter parameter.

 Set the **batch\_size** parameter according to the agent environment.

</td></tr><tr><td>

Metric

</td><td>

aws.metrics-s3

</td><td>

Returns metrics of all S3 buckets in an AWS datacenter.

</td><td>

metrics-s3.rb \(options\)

 -b, --batch\_size BATCH\_SIZE Batch size. Number of S3 buckets to fetch metrics in parallel. \(Default value: 10\)

</td><td>

`./metrics-s3.rb -b 5`

 Set the **batch\_size** parameter according to the agent environment.

</td></tr><tr><td>

Metric

</td><td>

aws.metrics-rds

</td><td>

Returns metrics of all RDS buckets in an AWS datacenter.

</td><td>

metrics-rds.rb \(options\)

 -F, --filter FILTER String representation of the filter to filter RDS Instances by tags.

 -b, --batch\_size BATCH\_SIZE Batch size. Number of databases to fetch metrics in parallel. \(Default value: 10\)

</td><td>

`./metrics-rds.rb -F "{name:tag:environment,values:[ENV1,ENV2]} {name:tag:engine,values:[MariaDB]}"` Provide the filter string with double quotes \(""\) around the filter parameter.

 Set the **batch\_size** parameter according to the agent environment.

</td></tr><tr><td>

Metric

</td><td>

aws.metrics-classic-elb

</td><td>

Returns metrics of all classic elastic load balancers in an AWS datacenter.

</td><td>

metrics-elb.rb \(options\)

 -e, --exclude\_lb EXCLUDE\_LB Exclude metrics from load balancers whose name contains one of the comma separated strings.

 -b, --batch\_size BATCH\_SIZE Batch size. Number of databases to fetch metrics in parallel. \(Default value: 10\)

</td><td>

`./metrics-elb.rb -t classic -e "classic,itom,ip" -b 10`

 Provide comma separated strings in double quotes \(""\) for the **exclude\_lb** parameter.

 Set the **batch\_size** parameter according to the agent environment.

</td></tr><tr><td>

Metric

</td><td>

aws.metrics-network-elb

</td><td>

Returns metrics of all network elastic load balancers in an AWS datacenter.

</td><td>

metrics-elb.rb \(options\)

 -e, --exclude\_lb EXCLUDE\_LB Exclude metrics from load balancers whose name contains any of the comma separated strings.

 -b, --batch\_size BATCH\_SIZE Batch size. Number of databases to fetch metrics in parallel. \(Default value: 10\)

</td><td>

`./metrics-elb.rb -t network -e "vpc,itom,ip" -b 10`

 Provide comma separated strings in double quotes \(""\) for the **exclude\_lb** parameter.

 Set the **batch\_size** parameter according to the agent environment.

 Do not change the command prefix.

</td></tr><tr><td>

Metric

</td><td>

aws.metrics-application-elb

</td><td>

Returns metrics of all application elastic load balancers in an AWS datacenter.

</td><td>

metrics-elb.rb \(options\)

 -e, --exclude\_lb EXCLUDE\_LB Exclude metrics from load balancers whose name contains any one of the string from comma separated strings.

 -b, --batch\_size BATCH\_SIZE Batch size. Number of databases to fetch metrics in parallel. \(Default value: 10\)

</td><td>

`./metrics-elb.rb -t application -e "classic,app,ip" -b 10`

 Provide comma separated strings in double quotes \(""\) for the **exclude\_lb** parameter.

 Set the **batch\_size** parameter according to the agent environment.

 Do not change the command prefix.

</td></tr><tr><td>

Metric

</td><td>

aws.metrics-ec2-count

</td><td>

Returns count of EC2 instances by instance\_type or status in an AWS datacenter.

</td><td>

metrics-ec2-count.rb \(options\)

 -s, --scheme SCHEME Metric naming scheme, text to prepend to metric. Default: aws.ec2

 -t, --type METRIC type Count by type: status, instance. Default: instance

</td><td>

`./metrics-ec2-count.rb -t status`

 `./metrics-ec2-count.rb -t status -s metric.aws.ec2`

</td></tr></tbody>
</table><table id="table_jtd_13s_2sb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

aws.metrics-dynamodb

</td><td>

Monitors the health of DynamoDB tables in an AWS datacenter.Binds to the DynamoDB table \(cmdb\_ci\_dynamodb\_table\)

</td><td>

e, --exclude\_tb EXCLUDE\_TB

Exclude metrics from tables whose name contains a string from comma separated strings. b, --batch\_size BATCH\_SIZE

Batch size. Number of tables to fetch metrics in parallel. \(Default value: 10\)

</td><td>

`metrics-dynamodb.rb -r {{.labels.params_ci_region}} {{.labels.params_exclude_tb}} -f {{.labels.params_exclude_tb}} {{end}} {{.labels.params_batch_size}} -b {{.labels.params_filter}} {{end}}`

</td></tr></tbody>
</table><table id="table_dj3_g3s_2sb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

aws.metrics-ecs-cluster

</td><td>

Monitors ECS clusters in an AWS datacenter.Binds to the AWS ECS Cluster CI type \(cmdb\_ci\_cloud\_ecs\_cluster\)

</td><td>

-F, --filter FILTER

String representation of the filter to filter ECS clusters by tags.b, --batch\_size BATCH\_SIZE

Batch size. Number of clusters to fetch metrics in parallel. \(Default value: 10\)

</td><td>

`metrics-ecs-cluster.rb -r {{.labels.params_ci_region}} {{.labels.params_filter}} -f {{.labels.params_filter}} {{end}} {{.labels.params_batch_size}} -b {{.labels.params_filter}} {{end}}`

</td></tr><tr><td>

Metric

</td><td>

aws.metrics-ecs-service

</td><td>

Monitors ECS services in an AWS datacenter.Binds to the AWS ECS Service CI type \(cmdb\_ci\_cloud\_ecs\_service\)

</td><td>

-F, --filter FILTER

String representation of the filter to filter ECS clusters by tags.b, --batch\_size BATCH\_SIZE

Batch size. Number of clusters to fetch metrics in parallel. \(Default value: 10\)

</td><td>

`metrics-ecs-service.rb -r {{.labels.params_ci_region}} {{.labels.params_filter}} -f {{.labels.params_filter}} {{end}} {{.labels.params_batch_size}} -b {{.labels.params_filter}} {{end}}`

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

**Related topics**  


[AWS metrics](aws-metrics.md)

