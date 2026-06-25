---
title: ECC Queue performance metrics
description: The metrics provide the ECC Queue performance snapshot within the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-ecc-queue-perf-metrics.html
release: australia
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 4
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# ECC Queue performance metrics

The metrics provide the ECC Queue performance snapshot within the ServiceNow AI Platform®.

## ECC Queue Metrics

-   **ECC Queue message count \(Input\)**

    The External Communication Channel \(ECC\) Queue is a connection point between an instance and the MID Server. This metrics represent the count of input messages by respective queue agent name that is, name of the external system when it is in ready or processing state.

-   **ECC Queue message count \(Output\)**

    The External Communication Channel \(ECC\) Queue is a connection point between an instance and the MID Server. This metrics represent the count of output messages by respective queue agent name that is, name of the external system when it is in ready or processing state.

-   **Avg waiting time \(Input\)**

    This metric represents the average age for input message at ready state. This will tell us the load on mid server, since the messages are not picked up by mid server for processing.

-   **Avg waiting time \(Output\)**

    This metric represents the average age for output message at ready state. This will tell us the load on mid server since the messages are not picked up by mid server for processing.

-   **Processed message delta \(Input\)**

    This represents the delta change in the number of input messages that are in "processed" state since the previous data collection point \(that is, in the previous 5 minutes\) by respective queue agent name.

-   **Processed message delta \(Output\)**

    This represents the delta change in the number of output messages that are in "processed" state since the previous data collection point \(that is, in the previous 5 minutes\) by respective queue agent name.


**Note:**

The MID Server status is not an indication of whether the MID Server service is running or stopped. Rather, the MID Server status is a representation of the communication between the MID Server and the instance. The MID Server status is decided based on the ecc\_queue record inputs received by the instance from a MID Server. The MID Server status may be set to down if:

-   The MID Server configuration file has incorrect configuration such as invalid credentials, incorrect instance URL, or misconfigured proxy information.
-   The communication from the MID Server to the instance is being blocked, which could be due to a proxy or a firewall.
-   The MID Server service is not running, which could be caused by a manual stop or a crash of the MID Server service.

**Parent Topic:**[Overview of Instance Observer metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-observer-ovr-metric.md)

**Related topics**  


[Instance Observer reports overview]()

[Anomaly insights]()

[Feature availability based on package]()

[Auriga Intelligent Alert report]()

[Transaction or response metrics]()

[Database performance metrics]()

[Semaphores performance metrics]()

[Event queues performance metrics]()

[Email performance metrics]()

[Scheduler performance metrics]()

[Job details performance metrics]()

[Node health performance metrics]()

[Host health performance metrics]()

[Standby replication Lag]()

[Pool Replication Lag]()

[Chat details performance metrics]()

[Cluster details performance metrics]()

[Load balancer performance metrics]()

[User information metrics]()

[Instance Data Replication]()

