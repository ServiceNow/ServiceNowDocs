---
title: AWS metrics
description: The following tables list and describe the metrics that are gathered as output from the specified AWS checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 18
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# AWS metrics

The following tables list and describe the metrics that are gathered as output from the specified AWS checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

<table id="table_wj4_qr1_wrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws.ec2.CPUCreditBalance.Average

</td><td>

Number of earned CPU credits that an instance has accrued since it was launched or started.

</td></tr><tr><td>

aws.ec2.CPUUtilization.Average

</td><td>

Average percentage of allocated EC2 compute units that are currently in use on the instance.

</td></tr><tr><td>

aws.ec2.DiskReadOps.Average\(Featured metric\)

</td><td>

Average of completed read operations from all instance store volumes available to the instance in a specified time period.

</td></tr><tr><td>

aws.ec2.DiskWriteOps.Average\(Featured metric\)

</td><td>

Completed write operations to all instance store volumes available to the instance in a specified time period.

</td></tr><tr><td>

aws.ec2.DiskReadBytes.Average\(Featured metric\)

</td><td>

Average number of bytes read from all instance store volumes available to the instance.

</td></tr><tr><td>

aws.ec2.DiskWriteBytes.Average\(Featured metric\)

</td><td>

Average number of bytes written to all instance store volumes available to the instance.

</td></tr><tr><td>

aws.ec2.NetworkIn.Average\(Featured metric\)

</td><td>

Average number of bytes received by the instance on all network interfaces. This metric identifies the volume of incoming network traffic to a single instance.

</td></tr><tr><td>

aws.ec2.NetworkOut.Average\(Featured metric\)

</td><td>

Average number of bytes sent out by the instance on all network interfaces. This metric identifies the volume of outgoing network traffic from a single instance.

</td></tr><tr><td>

aws.ec2.NetworkPacketsIn.Average

</td><td>

Average number of packets received by the instance on all network interfaces. This metric identifies the volume of incoming traffic in terms of the number of packets on a single instance.

</td></tr><tr><td>

aws.ec2.NetworkPacketsOut.Average

</td><td>

Average number of packets sent out by the instance on all network interfaces. This metric identifies the volume of outgoing traffic in terms of the number of packets on a single instance.

</td></tr><tr><td>

aws.ec2.MetadataNoToken.Average

</td><td>

Average number of times the instance metadata service was successfully accessed using a method that does not use a token.

</td></tr><tr><td>

aws.ec2.CPUCreditUsage.Average

</td><td>

Average number of CPU credits spent by the instance for CPU utilization.

</td></tr><tr><td>

aws.ec2.CPUSurplusCreditBalance.Average

</td><td>

Average number of surplus credits that have been spent by an unlimited instance when its **CPUCreditBalance** value is zero.

</td></tr><tr><td>

aws.ec2.CPUSurplusCreditsCharged.Average

</td><td>

Average number of spent surplus credits that are not paid down by earned CPU credits, and which thus incur an additional charge.

</td></tr><tr><td>

aws.ec2.StatusCheckFailed\_Instance.Average

</td><td>

Reports whether the instance has passed the instance status check in the last minute.

</td></tr><tr><td>

aws.ec2.StatusCheckFailed\_System.Average

</td><td>

Reports whether the instance has passed the system status check in the last minute.

</td></tr><tr><td>

aws.ec2.StatusCheckFailed.Average

</td><td>

Reports whether the instance has passed both the instance status check and the system status check in the last minute.

</td></tr></tbody>
</table><table id="table_sl3_xr1_wrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws.ebs.VolumeReadBytes.Average\(Featured metric\)

</td><td>

Average total number of bytes transferred during the period while reading.

</td></tr><tr><td>

aws.ebs.VolumeWriteBytes.Average\(Featured metric\)

</td><td>

Average total number of bytes transferred during the period while writing.

</td></tr><tr><td>

aws.ebs.VolumeReadOps.Average\(Featured metric\)

</td><td>

Average total number of read operations in a specified time period.

</td></tr><tr><td>

aws.ebs.VolumeWriteOps.Average\(Featured metric\)

</td><td>

Average total number of write operations in a specified time period.

</td></tr><tr><td>

aws.ebs.VolumeTotalReadTime.Average\(Featured metric\)

</td><td>

Average total number of seconds spent by all read operations completed in a specified time period.

</td></tr><tr><td>

aws.ebs.VolumeTotalWriteTime.Average\(Featured metric\)

</td><td>

Average of total number of seconds spent by all write operations completed in a specified time period.

</td></tr><tr><td>

aws.ebs.VolumeIdleTime.Average

</td><td>

Average of total number of seconds in a specified time period when no read or write operations were submitted.

</td></tr><tr><td>

aws.ebs.VolumeQueueLength.Average

</td><td>

Average number of read and write operation requests waiting to be completed in a specified time period.

</td></tr><tr><td>

aws.ebs.VolumeThroughputPercentage.Average

</td><td>

Average percentage of I/O operations per second \(IOPS\) delivered of the total IOPS provisioned for an Amazon EBS volume.

</td></tr><tr><td>

aws.ebs.VolumeConsumedReadWriteOps.Average

</td><td>

Average total amount of read and write operations \(normalized to 256K capacity units\) consumed in a specified time period.

</td></tr><tr><td>

aws.ebs.BurstBalance.Average

</td><td>

Average percentage of I/O credits \(for gp2\) or throughput credits \(for st1 and sc1\) remaining in the burst bucket.

</td></tr></tbody>
</table><table id="table_ac1_5tv_wrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws.s3.NumberOfObjects.Average\(Featured metric\)

</td><td>

Average total number of objects stored in a bucket for all storage classes.Collected every 12 hours.

</td></tr><tr><td>

aws.s3.BucketSizeBytes.Average\(Featured metric\)

</td><td>

Average amount of data in bytes stored in a bucket in the STANDARD storage class.Collected every 12 hours.

</td></tr></tbody>
</table><table id="table_mg1_q5v_wrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws.rds.BinLogDiskUsage.Average

</td><td>

Average amount of disk space occupied by binary logs on the primary. Applies to MySQL read replicas.

</td></tr><tr><td>

aws.rds.BurstBalance.Average

</td><td>

Average percent of General Purpose SSD \(gp2\) burst-bucket I/O credits available.

</td></tr><tr><td>

aws.rds.CPUUtilization.Average\(Featured metric\)

</td><td>

Average percentage of CPU utilization.

</td></tr><tr><td>

aws.rds.CPUCreditUsage.Average

</td><td>

Average number of CPU credits spent by the instance for CPU utilization.

</td></tr><tr><td>

aws.rds.CPUCreditBalance.Average

</td><td>

Average number of surplus credits that have been spent by an unlimited instance when its **CPUCreditBalance** value is zero.

</td></tr><tr><td>

aws.rds.DatabaseConnections.Average\(Featured metric\)

</td><td>

Average number of database connections in use.

</td></tr><tr><td>

aws.rds.DiskQueueDepth.Average\(Featured metric\)

</td><td>

Average number of outstanding I/Os \(read/write requests\) waiting to access the disk.

</td></tr><tr><td>

aws.rds.EBSByteBalance%.Average

</td><td>

Average percentage of throughput credits remaining in the burst bucket of your RDS database.

</td></tr><tr><td>

aws.rds.EBSIOBalance%.Average

</td><td>

Average percentage of I/O credits remaining in the burst bucket of your RDS database.

</td></tr><tr><td>

aws.rds.FailedSQLServerAgentJobsCount.Average\(Featured metric\)

</td><td>

Average number of failed Microsoft SQL Server Agent jobs during the last minute.

</td></tr><tr><td>

aws.rds.FreeableMemory.Average\(Featured metric\)

</td><td>

Average amount of available random access memory.

</td></tr><tr><td>

aws.rds.FreeStorageSpace.Average

</td><td>

Average amount of available storage space.

</td></tr><tr><td>

aws.rds.MaximumUsedTransactionIDs.Average

</td><td>

Average amount of maximum transaction IDs that have been used. Applies to PostgreSQL.

</td></tr><tr><td>

aws.rds.NetworkReceiveThroughput.Average\(Featured metric\)

</td><td>

Average incoming \(receive\) network traffic on the DB instance, including both customer database traffic and Amazon RDS traffic used for monitoring and replication.

</td></tr><tr><td>

aws.rds.NetworkTransmitThroughput.Average\(Featured metric\)

</td><td>

Average outgoing \(transmit\) network traffic on the DB instance, including both customer database traffic and Amazon RDS traffic used for monitoring and replication.

</td></tr><tr><td>

aws.rds.OldestReplicationSlotLag.Average

</td><td>

Average lagging size of the replica lagging the most in terms of write-ahead log \(WAL\) data received. Applies to PostgreSQL.

</td></tr><tr><td>

aws.rds.ReadIOPS.Average

</td><td>

Average number of disk read I/O operations per second.

</td></tr><tr><td>

aws.rds.ReadLatency.Average\(Featured metric\)

</td><td>

Average amount of time taken per disk I/O operation.

</td></tr><tr><td>

aws.rds.ReadThroughput.Average

</td><td>

Average number of bytes read from disk per second.

</td></tr><tr><td>

aws.rds.ReplicaLag.Average

</td><td>

Average amount of time a read replica DB instance lags behind the source DB instance. Applies to MySQL, MariaDB, Oracle, PostgreSQL, and SQL Server read replicas.

</td></tr><tr><td>

aws.rds.ReplicationSlotDiskUsage.Average

</td><td>

Average amount of disk space used by replication slot files. Applies to PostgreSQL.

</td></tr><tr><td>

aws.rds.SwapUsage.Average

</td><td>

Average amount of swap space used on the DB instance. This metric is not available for SQL Server.

</td></tr><tr><td>

aws.rds.TransactionLogsDiskUsage.Average

</td><td>

Average disk space used by transaction logs. Applies to PostgreSQL.

</td></tr><tr><td>

aws.rds.TransactionLogsGeneration.Average

</td><td>

Average size of transaction logs generated per second. Applies to PostgreSQL.

</td></tr><tr><td>

aws.rds.WriteIOPS.Average

</td><td>

Average number of disk write I/O operations per second.

</td></tr><tr><td>

aws.rds.WriteLatency.Average\(Featured metric\)

</td><td>

Average amount of time taken per disk I/O operation.

</td></tr><tr><td>

aws.rds.WriteThroughput.Average

</td><td>

Average number of bytes written to disk per second.

</td></tr><tr><td>

aws.rds.CPUSurplusCreditBalance.Average

</td><td>

Average number of surplus credits that have been spent by an unlimited instance when its **CPUCreditBalance** value is zero.

</td></tr><tr><td>

aws.rds.CPUSurplusCreditsCharged.Average

</td><td>

Average number of spent surplus credits that are not paid down by earned CPU credits, and which therefore incur an additional charge.

</td></tr></tbody>
</table><table id="table_ybj_bcw_wrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws.classicElb.EstimatedALBActiveConnectionCount.Average\(Featured metric\)

</td><td>

Average estimated number of concurrent TCP connections active from clients to the load balancer and from the load balancer to targets.

</td></tr><tr><td>

aws.classicElb.EstimatedALBConsumedLCUs.Average

</td><td>

Average estimated number of load balancer capacity units \(LCU\) used by an Application Load Balancer. You pay for the number of LCUs that you use per hour.

</td></tr><tr><td>

aws.classicElb.EstimatedALBNewConnectionCount.Average\(Featured metric\)

</td><td>

Average estimated number of new TCP connections established from clients to the load balancer and from the load balancer to targets.

</td></tr><tr><td>

aws.classicElb.EstimatedProcessedBytes.Average

</td><td>

Estimated number of bytes processed by an Application Load Balancer.

</td></tr><tr><td>

aws.classicElb.DesyncMitigationMode\_NonCompliant\_Request\_Count.Sum

</td><td>

Number of requests that do not comply with RFC 7230.

</td></tr><tr><td>

aws.classicElb.HTTPCode\_ELB\_5XX.Sum\(Featured metric\)

</td><td>

Number of HTTP 4XX client error codes generated by the load balancer.

</td></tr><tr><td>

aws.classicElb.HTTPCode\_ELB\_4XX.Sum\(Featured metric\)

</td><td>

Number of HTTP 5XX server error codes generated by the load balancer.

</td></tr><tr><td>

aws.classicElb.SurgeQueueLength.Maximum

</td><td>

Maximum total number of requests \(HTTP listener\) or connections \(TCP listener\) that are pending routing to a healthy instance. The maximum size of the queue is 1,024. Additional requests or connections are rejected when the queue is full.

</td></tr><tr><td>

aws.classicElb.SpilloverCount.Sum\(Featured metric\)

</td><td>

Total number of requests rejected because the surge queue is full.

</td></tr><tr><td>

aws.classicElb.RequestCount.Sum

</td><td>

Total number of requests completed or connections made during the specified interval.

</td></tr><tr><td>

aws.classicElb.Latency.Average\(Featured metric\)

</td><td>

Average total time elapsed, in seconds, from the time the load balancer sent the request to a registered instance until the instance started to send the response headers.

</td></tr><tr><td>

aws.classicElb.BackendConnectionErrors.Sum\(Featured metric\)

</td><td>

Total number of connections that were not successfully established between the load balancer and the registered instances.

</td></tr><tr><td>

aws.classicElb.HealthyHostCount.Average

</td><td>

Average number of healthy instances registered with your load balancer. A newly registered instance is considered healthy after it passes the first health check.

</td></tr><tr><td>

aws.classicElb.UnHealthyHostCount.Average

</td><td>

Average of number of unhealthy instances registered with your load balancer. An instance is considered unhealthy after it exceeds the unhealthy threshold configured for health checks.

</td></tr></tbody>
</table><table id="table_l1c_5gw_wrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws.networkElb.ActiveFlowCount.Average\(Featured metric\)

</td><td>

Average total number of concurrent flows \(or connections\) from clients to targets. This metric includes connections in the SYN\_SENT and ESTABLISHED states.

</td></tr><tr><td>

aws.networkElb.ActiveFlowCount\_TCP.Average\(Featured metric\)

</td><td>

Average total number of concurrent TCP flows \(or connections\) from clients to targets. This metric includes only connections in the ESTABLISHED state.

</td></tr><tr><td>

aws.networkElb.ActiveFlowCount\_TLS.Average\(Featured metric\)

</td><td>

Average total number of concurrent TLS flows \(or connections\) from clients to targets. This metric includes only connections in the ESTABLISHED state.

</td></tr><tr><td>

aws.networkElb.ActiveFlowCount\_UDP.Average\(Featured metric\)

</td><td>

Average total number of concurrent UDP flows \(or connections\) from clients to targets.

</td></tr><tr><td>

aws.networkElb.ClientTLSNegotiationErrorCount.Sum\(Featured metric\)

</td><td>

Average total number of TLS handshakes that failed during negotiation between a client and a TLS listener.

</td></tr><tr><td>

aws.networkElb.ConsumedLCUs.Average

</td><td>

Average number of load balancer capacity units \(LCU\) used by your load balancer.

</td></tr><tr><td>

aws.networkElb.ConsumedLCUs\_TCP.Average

</td><td>

Average number of load balancer capacity units \(LCU\) used by your load balancer for TCP.

</td></tr><tr><td>

aws.networkElb.ConsumedLCUs\_TLS.Average

</td><td>

Average number of load balancer capacity units \(LCU\) used by your load balancer for TLS.

</td></tr><tr><td>

aws.networkElb.ConsumedLCUs\_UDP.Average

</td><td>

Average number of load balancer capacity units \(LCU\) used by your load balancer for UDP.

</td></tr><tr><td>

aws.networkElb.HealthyHostCount.Maximum\(Featured metric\)

</td><td>

The maximum number of targets that are considered healthy.

</td></tr><tr><td>

aws.networkElb.NewFlowCount.Sum\(Featured metric\)

</td><td>

Total number of new flows \(or connections\) established from clients to targets in the time period.

</td></tr><tr><td>

aws.networkElb.NewFlowCount\_TCP.Sum\(Featured metric\)

</td><td>

Total number of new TCP flows \(or connections\) established from clients to targets in the time period.

</td></tr><tr><td>

aws.networkElb.NewFlowCount\_TLS.Sum\(Featured metric\)

</td><td>

Total number of new TLS flows \(or connections\) established from clients to targets in the time period.

</td></tr><tr><td>

aws.networkElb.NewFlowCount\_UDP.Sum\(Featured metric\)

</td><td>

Total number of new UDP flows \(or connections\) established from clients to targets in the time period.

</td></tr><tr><td>

aws.networkElb.PeakBytesPerSecond.Maximum\(Featured metric\)

</td><td>

Maximum average throughput \(bytes per second\), calculated every 10 seconds during the sampling window. This metric includes health check traffic.

</td></tr><tr><td>

aws.networkElb.PeakPacketsPerSecond.Maximum\(Featured metric\)

</td><td>

Maximum average packet rate \(packets processed per second\), calculated every 10 seconds during the sampling window. This metric includes health check traffic.

</td></tr><tr><td>

aws.networkElb.ProcessedBytes.Sum

</td><td>

Total number of bytes processed by the load balancer, including TCP/IP headers. This count includes traffic to and from targets, minus health check traffic.

</td></tr><tr><td>

aws.networkElb.ProcessedBytes\_TCP.Sum

</td><td>

Total number of bytes processed by TCP listeners.

</td></tr><tr><td>

aws.networkElb.ProcessedBytes\_TLS.Sum

</td><td>

Total number of bytes processed by TLS listeners.

</td></tr><tr><td>

aws.networkElb.ProcessedBytes\_UDP.Sum

</td><td>

Total number of bytes processed by UDP listeners.

</td></tr><tr><td>

aws.networkElb.ProcessedPackets.Sum

</td><td>

Total number of packets processed by the load balancer. This count includes traffic to and from targets, including health check traffic.

</td></tr><tr><td>

aws.networkElb.TargetTLSNegotiationErrorCount.Sum\(Featured metric\)

</td><td>

Total number of TLS handshakes that failed during negotiation between a TLS listener and a target.

</td></tr><tr><td>

aws.networkElb.TCP\_Client\_Reset\_Count.Sum

</td><td>

Total number of reset \(RST\) packets sent from a client to a target. These resets are generated by the client and forwarded by the load balancer.

</td></tr><tr><td>

aws.networkElb.TCP\_ELB\_Reset\_Count.Sum

</td><td>

Total number of reset \(RST\) packets generated by the load balancer.

</td></tr><tr><td>

aws.networkElb.TCP\_Target\_Reset\_Count.Sum

</td><td>

Total number of reset \(RST\) packets sent from a target to a client. These resets are generated by the target and forwarded by the load balancer.

</td></tr><tr><td>

aws.networkElb.UnHealthyHostCount.Maximum\(Featured metric\)

</td><td>

Maximum number of targets that can be considered unhealthy.

</td></tr></tbody>
</table><table id="table_lb2_bmw_wrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws.applicationElb.ActiveConnectionCount.Sum\(Featured metric\)

</td><td>

Total number of concurrent TCP connections active from clients to the load balancer and from the load balancer to targets.

</td></tr><tr><td>

aws.applicationElb.ClientTLSNegotiationErrorCount.Sum\(Featured metric\)

</td><td>

Total number of TLS connections initiated by the client that did not establish a session with the load balancer due to a TLS error.

</td></tr><tr><td>

aws.applicationElb.ConsumedLCUs.Average

</td><td>

The average number of load balancer capacity units \(LCU\) used by your load balancer. You pay for the number of LCUs that you use per hour. For more information, see Elastic Load Balancing pricing.

</td></tr><tr><td>

aws.applicationElb.DesyncMitigationMode\_NonCompliant\_Request\_Count.Sum\(Featured metric\)

</td><td>

Total number of requests that do not comply with RFC 7230.

</td></tr><tr><td>

aws.applicationElb.DroppedInvalidHeaderRequestCount.Average\(Featured metric\)

</td><td>

Average number of requests where the load balancer removed HTTP headers with header fields that are not valid before routing the request. The load balancer removes these headers only if the routing.http.drop\_invalid\_header\_fields.enabled attribute is set to true.

</td></tr><tr><td>

aws.applicationElb.ForwardedInvalidHeaderRequestCount.Average\(Featured metric\)

</td><td>

Average number of requests routed by the load balancer that had HTTP headers with header fields that are not valid. The load balancer forwards requests with these headers only if the routing.http.drop\_invalid\_header\_fields.enabled attribute is set to false.

</td></tr><tr><td>

aws.applicationElb.GrpcRequestCount.Sum

</td><td>

Total number of gRPC requests processed over IPv4 and IPv6.

</td></tr><tr><td>

aws.applicationElb.HTTP\_Fixed\_Response\_Count.Sum

</td><td>

Total number of fixed-response actions that were successful.

</td></tr><tr><td>

aws.applicationElb.HTTP\_Redirect\_Count.Sum

</td><td>

Total number of redirect actions that were successful.

</td></tr><tr><td>

aws.applicationElb.HTTP\_Redirect\_Url\_Limit\_Exceeded\_Count.Sum\(Featured metric\)

</td><td>

Total number of redirect actions that couldn't be completed because the URL in the response location header is larger than 8K.

</td></tr><tr><td>

aws.applicationElb.HTTPCode\_ELB\_3XX\_Count.Sum\(Featured metric\)

</td><td>

Total number of HTTP 3XX redirection codes that originate from the load balancer. This count does not include response codes generated by targets.

</td></tr><tr><td>

aws.applicationElb.HTTPCode\_ELB\_4XX\_Count.Sum\(Featured metric\)

</td><td>

Total number of HTTP 4XX client error codes that originate from the load balancer. This count does not include response codes generated by targets.

</td></tr><tr><td>

aws.applicationElb.HTTPCode\_ELB\_5XX\_Count.Sum\(Featured metric\)

</td><td>

Total number of HTTP 5XX server error codes that originate from the load balancer. This count does not include any response codes generated by the targets.

</td></tr><tr><td>

aws.applicationElb.HTTPCode\_ELB\_500\_Count.Sum\(Featured metric\)

</td><td>

Total number of HTTP 500 error codes that originate from the load balancer.

</td></tr><tr><td>

aws.applicationElb.HTTPCode\_ELB\_502\_Count.Sum\(Featured metric\)

</td><td>

Total number of HTTP 502 error codes that originate from the load balancer.

</td></tr><tr><td>

aws.applicationElb.HTTPCode\_ELB\_503\_Count.Sum\(Featured metric\)

</td><td>

Total number of HTTP 503 error codes that originate from the load balancer.

</td></tr><tr><td>

aws.applicationElb.HTTPCode\_ELB\_504\_Count.Sum\(Featured metric\)

</td><td>

Total number of HTTP 504 error codes that originate from the load balancer.

</td></tr><tr><td>

aws.applicationElb.IPv6ProcessedBytes.Sum

</td><td>

Total number of bytes processed by the load balancer over IPv6.

</td></tr><tr><td>

aws.applicationElb.IPv6RequestCount.Sum

</td><td>

Total number of IPv6 requests received by the load balancer.

</td></tr><tr><td>

aws.applicationElb.NewConnectionCount.Sum

</td><td>

Total number of new TCP connections established from clients to the load balancer and from the load balancer to targets.

</td></tr><tr><td>

aws.applicationElb.NonStickyRequestCount.Sum

</td><td>

Total number of requests where the load balancer chose a new target because it couldn't use an existing sticky session.

</td></tr><tr><td>

aws.applicationElb.ProcessedBytes.Sum\(Featured metric\)

</td><td>

Total number of bytes processed by the load balancer over IPv4 and IPv6.

</td></tr><tr><td>

aws.applicationElb.RejectedConnectionCount.Sum\(Featured metric\)

</td><td>

Total number of connections that were rejected because the load balancer had reached its maximum number of connections.

</td></tr><tr><td>

aws.applicationElb.RequestCount.Sum

</td><td>

Total number of requests processed over IPv4 and IPv6.

</td></tr><tr><td>

aws.applicationElb.RuleEvaluations.Sum

</td><td>

Total number of rules processed by the load balancer given a request rate averaged over an hour.

</td></tr></tbody>
</table>|Metric Name|Description|
|-----------|-----------|
|aws.ec2.types.&lt;type\_name&gt;|Count of EC2 instances for the specified type in AWS Datacenter.|
|aws.ec2.status.running|Count of EC2 instances in Active state in an AWS Datacenter.|
|aws.ec2.status.stopped|Count of EC2 instances in Stopped state in an AWS Datacenter.|
|aws.ec2.status.total|Count of all EC2 instances in an AWS Datacenter.|

<table id="table_qwz_2by_2sb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws.dynamodb.ConsumedWriteCapacityUnits.Average\(Featured metric\)

</td><td>

Number of write capacity units consumed over the specified time period, for tracking how much provisioned throughput is used.

</td></tr><tr><td>

aws.dynamodb.ConsumedReadCapacityUnits.Average\(Featured metric\)

</td><td>

Number of read capacity units consumed over the specified time period, for tracking how much provisioned throughput is used.

</td></tr><tr><td>

aws.dynamodb.ProvisionedWriteCapacityUnits.Average\(Featured metric\)

</td><td>

Number of provisioned write capacity units for a table.

</td></tr><tr><td>

aws.dynamodb.ProvisionedReadCapacityUnits.Average\(Featured metric\)

</td><td>

Number of provisioned read capacity units for a table.

</td></tr><tr><td>

aws.dynamodb.SuccessfulRequestLatency.GetItem.Average\(Featured metric\)

</td><td>

Successful requests to DynamoDB or Amazon DynamoDB streams during the specified time period. Run by a GetItem operation.

</td></tr><tr><td>

aws.dynamodb.SuccessfulRequestLatency.BatchGetItem.Average

</td><td>

Successful requests to DynamoDB or Amazon DynamoDB streams during the specified time period. Run by a BatchGetItem operation.

</td></tr><tr><td>

aws.dynamodb.SuccessfulRequestLatency.PutItem.Average\(Featured metric\)

</td><td>

Successful requests to DynamoDB or Amazon DynamoDB streams during the specified time period. Run by a PutItem operation.

</td></tr><tr><td>

aws.dynamodb.SuccessfulRequestLatency.BatchPutItem.Average

</td><td>

Successful requests to DynamoDB or Amazon DynamoDB streams during the specified time period. Run by a BatchPutItem operation.

</td></tr><tr><td>

aws.dynamodb.SuccessfulRequestLatency.Query.Average

</td><td>

Successful requests to DynamoDB or Amazon DynamoDB streams during the specified time period. Run by a Query operation.

</td></tr><tr><td>

aws.dynamodb.SuccessfulRequestLatency.Scan.Average

</td><td>

Successful requests to DynamoDB or Amazon DynamoDB Streams during the specified time period. Run by a Scan operation.

</td></tr><tr><td>

aws.dynamodb.ReturnedItemCount.Scan.Average

</td><td>

Number of items returned by Scan operations during the specified time period.

</td></tr><tr><td>

aws.dynamodb.ReturnedItemCount.Query.Average

</td><td>

Number of items returned by Query operations during the specified time period.

</td></tr><tr><td>

aws.dynamodb.UserErrors.Average\(Featured metric\)

</td><td>

Requests to DynamoDB or Amazon DynamoDB streams that generate an HTTP 400 status code during the specified time period. An HTTP 400 usually indicates a client-side error, such as an invalid combination of parameters, an attempt to update a nonexistent table, or an incorrect request signature.

</td></tr><tr><td>

aws.dynamodb.SystemErrors.GetItem.Average\(Featured metric\)

</td><td>

Requests to DynamoDB or Amazon DynamoDB streams that generate an HTTP 500 status code during the specified time period. An HTTP 500 usually indicates an internal service error. Run by a GetItem operation.

</td></tr><tr><td>

aws.dynamodb.SystemErrors.Scan.Average

</td><td>

The requests to DynamoDB or Amazon DynamoDB streams that generate an HTTP 500 status code during the specified time period. An HTTP 500 usually indicates an internal service error. Run by a Scan operation.

</td></tr><tr><td>

aws.dynamodb.SystemErrors.Query.Average

</td><td>

Requests to DynamoDB or Amazon DynamoDB streams that generate an HTTP 500 status code during the specified time period. An HTTP 500 usually indicates an internal service error. Run by a Query operation.

</td></tr><tr><td>

aws.dynamodb.SystemErrors.BatchGetItem.Average

</td><td>

Requests to DynamoDB or Amazon DynamoDB streams that generate an HTTP 500 status code during the specified time period. An HTTP 500 usually indicates an internal service error. Run by a BatchGet operation.

</td></tr><tr><td>

aws.dynamodb.SystemErrors.PutItem.Average\(Featured metric\)

</td><td>

Requests to DynamoDB or Amazon DynamoDB streams that generate an HTTP 500 status code during the specified time period. An HTTP 500 usually indicates an internal service error. Run by a PutItem operation.

</td></tr><tr><td>

aws.dynamodb.SystemErrors.UpdateItem.Average

</td><td>

The requests to DynamoDB or Amazon DynamoDB streams that generate an HTTP 500 status code during the specified time period. An HTTP 500 usually indicates an internal service error. Run by an UpdateItem operation.

</td></tr><tr><td>

aws.dynamodb.SystemErrors.DeleteItem.Average

</td><td>

Requests to DynamoDB or Amazon DynamoDB streams that generate an HTTP 500 status code during the specified time period. An HTTP 500 usually indicates an internal service error. Run by a DeleteItem operation.

</td></tr><tr><td>

aws.dynamodb.SystemErrors.BatchWriteItem.Average

</td><td>

Requests to DynamoDB or Amazon DynamoDB streams that generate an HTTP 500 status code during the specified time period. An HTTP 500 usually indicates an internal service error. Run by a BatchWrite operation.

</td></tr><tr><td>

aws.dynamodb.ConditionalCheckFailedRequests.Average\(Featured metric\)

</td><td>

Number of failed attempts to perform conditional writes.

</td></tr><tr><td>

aws.dynamodb.TimeToLiveDeletedItemCount.Average

</td><td>

Number of items deleted by Time to Live \(TTL\) during the specified time period. This metric helps you monitor the rate of TTL deletions on your table.

</td></tr><tr><td>

aws.dynamodb.TransactionConflict.Average

</td><td>

Rejected item-level requests due to transactional conflicts between concurrent requests on the same items.

</td></tr><tr><td>

aws.dynamodb.ReadThrottleEvents.Average\(Featured metric\)

</td><td>

Requests to DynamoDB that exceed the provisioned read capacity units for a table.

</td></tr><tr><td>

aws.dynamodb.WriteThrottleEvents.Average\(Featured metric\)

</td><td>

Requests to DynamoDB that exceed the provisioned write capacity units for a table.

</td></tr><tr><td>

aws.dynamodb.ThrottledRequests.GetItem.Average

</td><td>

Requests to DynamoDB that exceed the provisioned throughput limits on a resource for a GetItem operation.

</td></tr><tr><td>

aws.dynamodb.ThrottledRequests.PutItem.Average

</td><td>

Requests to DynamoDB that exceed the provisioned throughput limits on a resource for a PutItem operation.

</td></tr><tr><td>

aws.dynamodb.ThrottledRequests.DeleteItem.Average

</td><td>

Requests to DynamoDB that exceed the provisioned throughput limits on a resource for a DeleteItem operation.

</td></tr><tr><td>

aws.dynamodb.ThrottledRequests.UpdateItem.Average

</td><td>

Requests to DynamoDB that exceed the provisioned throughput limits on a resource for an UpdateItem operation.

</td></tr><tr><td>

aws.dynamodb.ThrottledRequests.BatchGetItem.Average

</td><td>

Requests to DynamoDB that exceed the provisioned throughput limits on a resource for a BatchGetItem operation.

</td></tr><tr><td>

aws.dynamodb.ThrottledRequests.Scan.Average

</td><td>

Requests to DynamoDB that exceed the provisioned throughput limits on a resource for a Scan operation.

</td></tr><tr><td>

aws.dynamodb.ThrottledRequests.Query.Average

</td><td>

Requests to DynamoDB that exceed the provisioned throughput limits on a resource for a Query operation.

</td></tr><tr><td>

aws.dynamodb.ThrottledRequests.BatchWriteItem.Average

</td><td>

Requests to DynamoDB that exceed the provisioned throughput limits on a resource for a BatchWriteItem operation.

</td></tr><tr><td>

aws.dynamodb.SuccessfulRequestLatency.GetRecords.Average

</td><td>

The successful requests to DynamoDB or Amazon DynamoDB Streams during the specified time period. Run by a GetRecords operation.

</td></tr><tr><td>

aws.dynamodb.ReturnedBytes.GetRecords.Average

</td><td>

The number of bytes returned by GetRecords operations \(Amazon DynamoDB streams\) during the specified time period.

</td></tr><tr><td>

aws.dynamodb.ReturnedRecordsCount.GetRecords.Average

</td><td>

The number of stream records returned by GetRecords operations \(Amazon DynamoDB streams\) during the specified time period.

</td></tr></tbody>
</table><table id="table_zpd_wxy_2sb"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws.ecs.cluster.CPUReservation.Average\(Featured metric\)

</td><td>

Percentage of CPU units reserved by running tasks in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.CPUUtilization.Average\(Featured metric\)

</td><td>

Percentage of CPU units used in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.MemoryReservation.Average\(Featured metric\)

</td><td>

Percentage of memory reserved by running tasks in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.MemoryUtilization.Average\(Featured metric\)

</td><td>

Percentage of memory used in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.CpuReserved.Average

</td><td>

CPU units reserved by tasks in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.CpuUtilized.Average

</td><td>

CPU units used by tasks in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.NetworkRxBytes.Average\(Featured metric\)

</td><td>

Number of bytes received by the cluster.

</td></tr><tr><td>

aws.ecs.cluster.NetworkTxBytes.Average\(Featured metric\)

</td><td>

Number of bytes transmitted by the cluster.

</td></tr><tr><td>

aws.ecs.cluster.EphemeralStorageReserved.Average

</td><td>

Ephemeral storage is the volatile temporary storage attached to your instances, present only during the running lifetime of the instance.

</td></tr><tr><td>

aws.ecs.cluster.MemoryUtilized.Average\(Featured metric\)

</td><td>

Memory being used by tasks in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.MemoryReserved.Average\(Featured metric\)

</td><td>

Memory reserved by tasks in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.StorageReadBytes.Average\(Featured metric\)

</td><td>

Number of bytes read from storage in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.StorageWriteBytes.Average\(Featured metric\)

</td><td>

Number of bytes written to storage in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.ContainerInstanceCount.Average\(Featured metric\)

</td><td>

Number of EC2 instances running the Amazon ECS agent that are registered with a cluster.

</td></tr><tr><td>

aws.ecs.cluster.ServiceCount.Average\(Featured metric\)

</td><td>

Number of services in the cluster.

</td></tr><tr><td>

aws.ecs.cluster.TaskCount.Average

</td><td>

Number of tasks running in the cluster.

</td></tr></tbody>
</table><table id="table_wkn_xxy_2sb"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws.ecs.service.CPUUtilization.Average\(Featured metric\)

</td><td>

Percentage of CPU units used in the service.

</td></tr><tr><td>

aws.ecs.service.MemoryUtilization.Average\(Featured metric\)

</td><td>

Percentage of memory used in the service.

</td></tr><tr><td>

aws.ecs.service.CpuReserved.Average

</td><td>

CPU units reserved by tasks in the service.

</td></tr><tr><td>

aws.ecs.service.CpuUtilized.Average

</td><td>

CPU units used by tasks in the service.

</td></tr><tr><td>

aws.ecs.service.NetworkRxBytes.Average\(Featured metric\)

</td><td>

Number of bytes received by the service.

</td></tr><tr><td>

aws.ecs.service.NetworkTxBytes.Average\(Featured metric\)

</td><td>

Number of bytes transmitted by the service.

</td></tr><tr><td>

aws.ecs.service.EphemeralStorageReserved.Average

</td><td>

Ephemeral storage is the volatile temporary storage attached to your instances which is present only during the running lifetime of the instance.

</td></tr><tr><td>

aws.ecs.service.MemoryUtilized.Average

</td><td>

Memory being used by tasks in the service.

</td></tr><tr><td>

aws.ecs.service.MemoryReserved.Average

</td><td>

Memory reserved by tasks in the service.

</td></tr><tr><td>

aws.ecs.service.StorageReadBytes.Average\(Featured metric\)

</td><td>

Number of bytes read from storage in the service.

</td></tr><tr><td>

aws.ecs.service.StorageWriteBytes.Average\(Featured metric\)

</td><td>

Number of bytes written to storage in the service.

</td></tr><tr><td>

aws.ecs.service.RunningTaskCount.Average\(Featured metric\)

</td><td>

Number of tasks currently in the RUNNING state.

</td></tr><tr><td>

aws.ecs.service.DeploymentCount.Average

</td><td>

Number of deployments in an Amazon ECS service.

</td></tr><tr><td>

aws.ecs.service.DesiredTaskCount.Average\(Featured metric\)

</td><td>

Desired number of tasks for an Amazon ECS service.

</td></tr><tr><td>

aws.ecs.service.TaskSetCount.Average\(Featured metric\)

</td><td>

Number of task sets in the service.

</td></tr><tr><td>

aws.ecs.service.PendingTaskCount.Average\(Featured metric\)

</td><td>

Number of tasks currently in the PENDING state.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

