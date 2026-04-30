---
title: Configuring Event Management
description: Event Management administrators administer events, manage and monitor alerts, aggregate alerts, and work review and monitor services' status with the Operator Workspace service monitor.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Event Management, ITOM Health, IT Operations Management]
---

# Configuring Event Management

Event Management administrators administer events, manage and monitor alerts, aggregate alerts, and work review and monitor services' status with the Operator Workspace service monitor.

Event Management operators find alerts, analyze them, and take action to resolve the underlying issue.

-   **[Request Event Management](../task/t_EMActivatePlugin.md#)**  
Event Management plugin \(com.glideapp.itom.snac\) requires a separate subscription and must be activated by ServiceNow personnel. This plugin includes demo data and activates related plugins if they are not already active.
-   **[Install Event Management](../task/install-event-management.md)**  
Retrieve the most updated apps for the Event Management application \(com.glideapp.itom.snac\) in the ServiceNow® Store. Periodically check the ServiceNow® Store for new app versions.
-   **[Enhance Event Management performance](../task/improve-event-mgmt-performance.md)**  
The Event Management Accelerator plugin ensures that Event Management maintains performance at a high level. This plugin is optional.
-   **[Event Management setup](c_EMConfiguration.md)**  
After activating Event Management, set it up to receive and process events, and generate and analyze alerts.
-   **[Domain separation and Event Management](domain-separation-event-management.md)**  
Domain separation is supported in Event Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Event Management Integrations](c_EMEvent.md)**  
An event is a notification from one or more monitoring tools that indicate something of interest has occurred, such as a log message, warning, or error.
-   **[Event forwarding](event-forwarding-em.md)**  
Accelerate the event processing testing life cycle by forwarding a stream of events from your ServiceNow production environment to your non-production environment.
-   **[Processing Events](processing-events.md)**  
Event processing is the process of taking events or streams of events, analyzing them and taking automatic action. The process includes viewing events, event binding, event rules and event field mapping.
-   **[Manage and monitor alerts](c_EMAlert.md)**  
An alert is a notification for selected events that are considered to be important and require attention. Event Management generates alerts based on event rules.
-   **[Application services in Event Management](application-service-event-management.md)**  
An application service is a set of interconnected applications and hosts which are configured to offer a service to the organization.
-   **[View Event Management license usage](../task/license-usage.md)**  
Event Management is licensed based on the number of CIs bound to alerts during the last year. For alerts that are not bound to CIs, the system calculates the number of nodes \(servers\) that can send events to the instance directly or through a third-party monitoring tool during the last year.

**Parent Topic:**[Event Management](c_EM.md)

