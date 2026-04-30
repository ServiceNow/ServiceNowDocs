---
title: Legacy: JBoss probes and sensors
description: Discovery identifies a Linux JBoss application server using probes and sensors.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Red Hat JBoss server, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Legacy: JBoss probes and sensors

Discovery identifies a Linux JBoss application server using probes and sensors.

## Linux

This process describes the use of probes, which are active on your instance if you upgrade. For new instances, Discovery uses the JBoss pattern.

1.  The UNIX - Active Processes probe detects a running process that matches an **org.jboss.main** entry point parameter.
2.  If there’s a match, a record is created in the JBoss Application Server \[cmdb\_ci\_app\_server\_jboss\] table. The following probes are also triggered:
    -   JBoss - Find web.xml list: The sensor of this probe populates information in the Web Application \[cmdb\_ci\_web\_application\] table if applicable.
    -   JBoss - Get jboss-service.xml: The sensor of this probe populates information in the Web Service \[cmdb\_ci\_web\_service\] table.
3.  The JBoss - Find web.xml list probe searches for the `web.xml` files of JBoss application server. The probe uses the **classpath** parameter in the running process, and then searches in the related `server\default\deploy` directory for the JBoss installation.
4.  If associated web applications reside in the `server\default\deploy` directory, the JBoss - Get web.xml probe triggers for each application. This probe reads the `web.xml` file for each web application and the sensor populates additional information to the Web Service \[cmdb\_ci\_web\_service\] table.
5.  The Boss - Get jboss-service.xml probe uses the **classpath** parameter in the running process to search for the `jboss-service.xml`file in the related `server\default\conf\` directory for the JBoss installation.
6.  If the probe successfully finds the `jboss-service.xml` file in the `server\default\conf\` directory, the sensor reads the contents of the XML file. It then creates additional records in the Web Service \[cmdb\_ci\_web\_service\] table as necessary.

## Windows

This process describes the use of probes, which are active on your instance if you upgrade. For new instances, Discovery uses the JBoss pattern.

1.  The Windows - Active Processes probe detects a running process that matches an **org.jboss.main** entry point parameter.
2.  If there’s a match, a record is created in the JBoss Application Server \[cmdb\_ci\_app\_server\_jboss\] table. The following probes are also triggered:
    -   JBoss - Find web.xml list: The sensor of this probe populates information in the Web Application \[cmdb\_ci\_web\_application\] table if applicable.
    -   JBoss - Get jboss-service.xml: The sensor of this probe populates information in the Web Service \[cmdb\_ci\_web\_service\] table.
3.  The JBoss - Find web.xml list probe searches for the `web.xml` files of JBoss application server. The probe uses the **classpath** parameter in the running process, and then searches in the related `server\default\deploy` directory for the JBoss installation.
4.  If associated web applications reside in the `server\default\deploy` directory, the JBoss - Get web.xml probe triggers for each application. This probe reads the `web.xml` file for each web application and the sensor populates additional information to the Web Service \[cmdb\_ci\_web\_service\] table.
5.  The Boss - Get jboss-service.xml probe uses the **classpath** parameter in the running process to search for the `jboss-service.xml`file in the related `server\default\conf\` directory for the JBoss installation.
6.  If the probe successfully finds the `jboss-service.xml` file in the `server\default\conf\` directory, the sensor reads the contents of the XML file. It then creates additional records in the Web Service \[cmdb\_ci\_web\_service\] table as necessary.

**Parent Topic:**[Red Hat JBoss server discovery](../concept/c_DataCollDiscoJBossServers.md)

