---
title: Configure Agent Client Collector Apache Tomcat monitoring
description: To configure the Agent Client Collector to perform Apache Tomcat monitoring, set the following configurations in the Apache Tomcat application.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Operating system and application monitoring using Agent Client Collector, Exploring Agent Client Collector Monitoring, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Configure Agent Client Collector Apache Tomcat monitoring

To configure the Agent Client Collector to perform Apache Tomcat monitoring, set the following configurations in the Apache Tomcat application.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Open a management JMX port when starting the server:

    1.  In a Linux environment:

        1.  In `bin` directory in the Tomcat home directory, create a `setenv.sh` file.
        2.  Ensure that the file contains the following:

            ```
            export CATALINA_OPTS=$CATALINA_OPTS"
            -Dcom.sun.management.jmxremote=true
            -Dcom.sun.management.jmxremote.port={PORT NUMBER}
            -Dcom.sun.management.jmxremote.rmi.port={PORT NUMBER}
            -Dcom.sun.management.jmxremote.ssl=false
            -Dcom.sun.management.jmxremote.authenticate=false
            -Djava.rmi.server.hostname=127.0.0.1"
            
            ```

        3.  Run `chmod 755 setenv.sh` to give the `setenv.sh` file executable permissions.
    2.  In a Windows environment:

        1.  In `bin` directory in the Tomcat home directory, create a `setenv.bat` file.
        2.  Ensure that the file contains the following:

            ```
            @echo=off
            if defined CATALINA_OPTS (
            set CATALINA_OPTS=%CATALINA_OPTS% -
            Dcom.sun.management.jmxremote=true
            ) else (
            set CATALINA_OPTS=-
            Dcom.sun.management.jmxremote=true
            )
            set CATALINA_OPTS=%CATALINA_OPTS% -
            Dcom.sun.management.jmxremote.port={PORT NUMBER}
            set CATALINA_OPTS=%CATALINA_OPTS% -
            Dcom.sun.management.jmxremote.rmi.port={PORT NUMBER}
            set CATALINA_OPTS=%CATALINA_OPTS% -
            Dcom.sun.management.jmxremote.authenticate=false
            set CATALINA_OPTS=%CATALINA_OPTS% -
            Dcom.sun.management.jmxremote.ssl=false
            set CATALINA_OPTS=%CATALINA_OPTS% -
            Djava.rmi.server.hostname=127.0.0.1
            
            ```

            \{PORT NUMBER\} represents the number of the port you open for JMX RMI monitoring. The default value created by the check definition is **9000**.

2.  Restart Tomcat.

    1.  In a Linux environment: Run the `shutdown.sh` script, followed by the `startup.sh` script.

    2.  In a Windows environment: Run the `shutdown.bat` script, followed by the `startup.bat` script.


