---
title: Domain separation and Health Log Analytics
description: Domain separation is supported for Health Log Analytics. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Domain separation and Health Log Analytics

Domain separation is supported for Health Log Analytics. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Domain separation and Health Log Analytics overview

Domain separation is present in all aspects of the Health Log Analytics application. Users belonging to a specific domain see only the data existing in their own domain.

## How domain separation works in Health Log Analytics

When data is domain separated using a single Health Log Analytics server, each Managed Service Provider \(MSP\) can see the log data only in its own domain or the child domains below it​​. Users can view alerts that Health Log Analytics generates only in their own domain. Actions to remediate the alerts apply only for the scope of that domain. By default, all users and records are set to the parent domain unless the admin assigns them to a specific domain.

The Health Log Analytics Domain Separation plugin must be installed before you configure your data inputs in the Health Log Analytics application. There is no setup procedure for the plugin. Install the plugin with the Health Log Analytics application Version 21.0.1 - September 2021, and then activate it. Make sure that you map your data into logical silos and configure rules and entities.

You define the domain-separated environment when you configure your data inputs. Users can use data inputs that are only available in their own domain. Health Log Analytics creates alerts only for logs that arrive in those data inputs. All relevant records and all data processing in the Health Log Analytics program flow reside in the same domain as the data input. A data input's domain name is shown in the **Domain** column displayed in the tables in your instance.

Using domain separation in your instance is transparent to Health Log Analytics. The application manages all aspects of the data, such as system settings and custom operations, separately. When a property is changed, the new value affects new sources only in the specific domain. System properties affecting the server are common to all domains because all domains use the Health Log Analytics server.

**Note:** Health Log Analytics supports up to 60 kilobytes events per second \(EPS\) across all domains, without the ability to provide a service level agreement \(SLA\) to a specific domain and without fairness. If a domain streams a large amount of data, the Health Log Analytics server processes it. Other domains might suffer latency, drops, or other issues as a result, even if they stream a low number of logs. On the MID Server side, 10 kilobytes EPS is expected.

​

## Use cases

-   An MSP wants to provide the Health Log Analytics application to multiple customers in a similar environment with a single instance​​.
-   An organization with many tenants wants to isolate its sensitive data, such as security logs​.
-   An administrator of a tenant organization wants to define a data input only for their own domain.
-   An operator in a tenant organization wants to view logs only in their own domain​.
-   An operator in a tenant organization wants to provide feedback for alerts only in their own domain​.
-   An MSP Admin wants to view log data from all of their organization's tenant domains.

**Parent Topic:**[Health Log Analytics reference](hla-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

