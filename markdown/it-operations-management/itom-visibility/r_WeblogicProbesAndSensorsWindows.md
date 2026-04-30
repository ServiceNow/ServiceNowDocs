---
title: Identifying Windows WebLogic application servers
description: If you are not using the Weblogic pattern, Discovery follows this process when it uses the Windows - Active Processes or Linux - Active Processes probes.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [WebLogic application server, Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Identifying Windows WebLogic application servers

If you are not using the Weblogic pattern, Discovery follows this process when it uses the Windows - Active Processes or Linux - Active Processes probes.

This process describes the use of probes, which are active on your instance if you upgrade. For new instances, Discovery uses the Weblogic pattern.

1.  The Windows - Active Processes probe or Linux - Active Processes detects a running process that matches one of the follow criteria:
    -   The parameters of the process contain **weblogic.Server**.
    -   The parameters of the process contain **-Dweblogic.name**.
2.  If there is a match on one of the criteria:
    -   A record is created in the BEA Weblogic \[cmdb\_ci\_app\_server\_weblogic\] table. The record is populated with the server name and TCP port, which is gathered from the running process.
    -   The Windows - Weblogic - Find config.xml probe or the Linux - Weblogic - Find config.xml probe triggers. The sensor of this probe populates additional information in the BEA Weblogic \[cmdb\_ci\_app\_server\_weblogic\] record and the Web Application \[cmdb\_ci\_web\_application\] record if applicable.
3.  The Windows - Weblogic - Find config.xml probe or the Linux - Weblogic - Find config.xml probe attempts to find the related `config.xml` file for the server by:
    -   Using the **-Dweblogic.RootDirectory=&lt;path&gt;** parameter defined in the running process.
    -   \[Windows\] Searching for `config.xml` files under the **–Dplatform.home=&lt;path&gt;** parameter defined in the running process \(not as efficient using the parameters of the process\).
    -   \[Linux\] Searching for the parent process that started the WebLogic server \(only viable if the weblogic jvm was started via the `startWeblogic.sh` or related custom script and not the init process\).
4.  If there are associated web applications found in the WebLogic `config.xml` file, the Windows – Weblogic find web.xml probe triggers for each application. This probe reads the WebLogic `web.xml` file for each web application and the sensor, and then populates additional information.

**Parent Topic:**[WebLogic application server discovery](../concept/c_DataCollDiscoWebLogicServers.md)

