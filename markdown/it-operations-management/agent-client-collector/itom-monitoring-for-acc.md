---
title: Operating system and application monitoring using Agent Client Collector
description: IT Operations Management \(ITOM\) monitoring for the Agent Client Collector is installed on the ServiceNow instance. It monitors the specific operating system and applications that are installed on the host machine.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Operating system and application monitoring using Agent Client Collector

IT Operations Management \(ITOM\) monitoring for the Agent Client Collector is installed on the ServiceNow® instance. It monitors the specific operating system and applications that are installed on the host machine.

The Agent Client Collector monitors the following applications.

<table id="table_wfm_tz5_bkb"><thead><tr><th>

Operating System/Application

</th><th>

Configuration description

</th></tr></thead><tbody><tr><td>

Windows

</td><td>

No special configuration required.

</td></tr><tr><td>

Linux

</td><td>

No special configuration required.

</td></tr><tr><td>

Apache HTTP Server

</td><td>

See [Configure Agent Client Collector Apache HTTP server monitoring](../task/acc-apache-http-server.md).

</td></tr><tr><td>

Apache Tomcat

</td><td>

See [Configure Agent Client Collector Apache Tomcat monitoring](../task/acc-apache-tomcat-monitoring.md).

</td></tr><tr><td>

IBM WebSphere

</td><td>

No special configuration required. Accessed through JMX. Default management port is **9100**.

</td></tr><tr><td>

IIS

</td><td>

No special configuration required.

</td></tr><tr><td>

JBoss/WildFly

</td><td>

No special configuration required. Default port is **9990**. For troubleshooting information, see [Monitoring performance](https://access.redhat.com/documentation/en-us/red_hat_jboss_enterprise_application_platform/7.1/html/performance_tuning_guide/monitoring_performance) in the Red Hat customer portal.

</td></tr><tr><td>

Microsoft SQL Server

</td><td>

No special configuration required. Ensure that the instance name is populated in the CI record, either by running Discovery or by manually populating the record.

</td></tr><tr><td>

My SQL

</td><td>

No special configuration required. Default port is **3306**.

</td></tr><tr><td>

Oracle Database

</td><td>

No special configuration required. Ensure that the SID and Oracle Home path are populated in the CI record, either by running Discovery or by manually populating the record. Default port is **1521**.

</td></tr><tr><td>

Oracle WebLogic

</td><td>

No special configuration required. Accessed via a JMX port. Default port is **7001**. Ensure that the WebLogic home \(wls\_home\) parameter is populated in the CI record, either by running Discovery or by manually populating the record.Ensure that the user running the agent has sufficient permissions to access the JAR files in the **Weblogic** installation directories.

</td></tr></tbody>
</table>When using the **Microsoft SQL Server**, **Oracle Database**, and **Oracle WebLogic** applications, you must run Discovery to configure CI fields on the instance. Ensure that the Discovery plugin \(com.snc.discovery\) is installed to enable running Discovery.

When the application is running on a port other than the default, ensure that you update the port number in the check instance's parameters.

