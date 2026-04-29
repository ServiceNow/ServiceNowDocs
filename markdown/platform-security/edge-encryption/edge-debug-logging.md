---
title: Increase debug logging for the Edge Encryption proxy
description: Increase the level of logging to interpret the logs and debug issues with the proxy.Use this method to debug issues with the Edge Encryption application, without stopping and restarting the proxy. These steps increase logging level and help troubleshooting the root cause with more verbose log statements.Enable timing metric logging to add a metric statement for each request handled by the Edge Encryption proxy. Each of these timing metric log statements contains useful information about the request, such as processing times and which encryption rule was used.Use this method to debug issues with SSL connectivity between the Edge Encryption proxy and your instance, such as access to the instance fails via the proxy. These steps increase logging and help find the verbose log statements.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Increase debug logging for the Edge Encryption proxy

Increase the level of logging to interpret the logs and debug issues with the proxy.

There are currently three options for increasing debug logging in the Edge Encryption proxy. Increase the level of logging to debug issues provide technical support with information to look into the issue with the benefit of more verbose log statements.

Depending on the issue being debugged, set up debug logging in one of three ways:

-   Debugging issues other than SSL connectivity
-   Logging timing metrics for requests through the proxy
-   Debugging issues with SSL connectivity between the Edge Encryption Proxy and the instance

For all debug cases, you may view and interpret the logs in your own or open an incident to get an interpretation from ServiceNow technical support providing the description of the issue and how it’s reproduced.

**Parent Topic:**[Configuring Edge Encryption](edge-config.md)

## Debugging issues with the Edge Encryption application other than SSL connectivity

Use this method to debug issues with the Edge Encryption application, without stopping and restarting the proxy. These steps increase logging level and help troubleshooting the root cause with more verbose log statements.

### Before you begin

Role required: admin

**Note:** Changes made to the `$proxy_installation_location/conf/log4j2.properties` file are taken up by the proxy within about 60 seconds after you make your changes. You don’t have to restart the proxies.

### Procedure

1.  In the `$proxy_installation_location/conf/log4j2.properties` file find the following line.

    ```
    logger.edge.level=info
    ```

2.  Change the above line to the following:

    ```
    logger.edge.level=debug
    ```

3.  Save the change.

    It may take up to 60 seconds for the change to take effect, but this doesn’t require a proxy restart.

4.  Reproduce your issue.

5.  Check for debug log statements related to the application in the `$proxy_installation_location/logs/edgeencryption.log` file.


### Result

After making the property change, you can see additional detail in your `$proxy_installation_location/logs/edgeencryption.log` file. When you have finished debugging, revert the change made to the `$proxy_installation_location/conf/log4j2.properties` file.

## Logging timing metrics for requests through the proxy

Enable timing metric logging to add a metric statement for each request handled by the Edge Encryption proxy. Each of these timing metric log statements contains useful information about the request, such as processing times and which encryption rule was used.

### Before you begin

Role required: admin

**Note:**

The additional logging settings are added to the `$proxy_installation_location/conf/log4j2.properties` file. Changes made are taken up by the proxy dynamically within about a minute after the changes to the file are made, so you do not have to restart the proxies.

### Procedure

1.  Modify the `$proxy_installation_location/conf/log4j2.properties` file by adding the following lines at the end of the file

    ```
    appender.timinglog.type=RollingFile
    appender.timinglog.name=TimingLog
    appender.timinglog.fileName=../logs/edgenetwork.log
    appender.timinglog.filePattern=../logs/$${date:yyyy-MM}/edgenetwork-%d{yyyy-MM-dd-HH}-%i.log.gz
    appender.timinglog.layout.type=PatternLayout
    appender.timinglog.layout.pattern=%d [%t] %-5p %m%n
    appender.timinglog.policies.type=Policies
    appender.timinglog.policies.size.type=SizeBasedTriggeringPolicy
    appender.timinglog.policies.size.size=500MB
    appender.timinglog.strategy.type=DefaultRolloverStrategy
    appender.timinglog.strategy.max=4
    
    logger.timing.name=com.snc.edgeencryption.metrics.EdgeEncryptionTimingMetricCache
    logger.timing.level=debug
    logger.timing.additivity=false
    logger.timing.appenderRef.rolling.ref=TimingLog
    ```

2.  Save the file.


### Result

After the `log4j.properties` file is saved, the following types of messages appear in the `$proxy_installation_location/logs/edgenetwork.log` log file for network times.

```
2022-07-21 12:56:15,783 [qtp1971991758-7700] DEBUG com.snc.edgeencryption.metrics.EdgeEncryptionTimingMetricCache -  request_uri=/api/now/ui/presencesysparm_auto_request=true&cd=1658433375754 request_method=POST client_request_received="2022-07-21 12:56:15,015" proxy_request_processing_time=6 all_rules_processing_time=0 rule_executed="REST JSON" rule_execution_time=1 proxy_instance_round_trip=14 proxy_response_processing_time=1 total_time_from_proxy=21 reponse_code=201 glide_user=SCv3_1:BAz1ZK7ee9XoroG2nvMlixHpgTvsT4fY2bwQvnH2WdU=:y5HGsTTqo3Pjq6G0xk4LoazCwCiWRJk4/6SpbXuBzqg=:6816f79cc0a8016401c5a33be04be441 jsessionid_suffix=037A66

```

The values in the log messages are as follows:

```
request_uri: The URI being requested

request_method: The HTTP method being used, for example, GET, POST, PUT, PATCH, DELETE

client_request_received: The timestamp noting when the HTTP client request arrived at the Edge proxy

proxy_request_processing_time: How long the Edge proxy took to process the request in milliseconds

all_rules_processing_time: Total time it took to execute all of the Edge Encryption rules for the request in milliseconds

rule_executed: The name of the encryption rule that was executed

rule_execution_time: How long it took to execute listed rule_executed in milliseconds

proxy_instance_round_trip: The time from when the Edge proxy sent the request to the instance until the instance sent the response and was received by the edge proxy in milliseconds

proxy_response_processing_time: How long the Edge proxy took to process the response in milliseconds

total_time_from_proxy: The total time from when the Edge proxy received the request from the client and returned the response to the client in milliseconds

response_code: HTTP response code 

glide_user: The glide_user cookie value

jsessionid_suffix: The JSession cookie suffix associated with the request
```

## Debug issues with SSL connectivity between the Edge Encryption proxy and the instance

Use this method to debug issues with SSL connectivity between the Edge Encryption proxy and your instance, such as access to the instance fails via the proxy. These steps increase logging and help find the verbose log statements.

### Before you begin

Role required: admin

**Note:** SSL connectivity debugging is only relevant when troubleshooting TLS connectivity type issues. In practice, this is not common and rarely needed.

### Procedure

1.  Stop the proxy server.

2.  Add the following line to the file `$proxy_installation_location/conf/wrapper.conf`, which is a Java startup property:

    ```
    wrapper.java.additional.<next available number in sequence> = -Djavax.net.debug=all
    
    ```

    For example:

    ```
    For example: wrapper.java.additional.4 = -Djavax.net.debug=all
    ```

3.  Save the change and restart the proxy server.

4.  Reproduce your connectivity issue.


### Result

After reproducing the issue debug log statements related to the SSL exchange can be found in the`$proxy_installation_location/logs/wrapper_<current date>.log` file. When you are finished debugging. You can remote the additional logging by removing or commenting out the line created in the previous steps.

