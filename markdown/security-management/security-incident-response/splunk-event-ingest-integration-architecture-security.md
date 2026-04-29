---
title: Key terms used in this integration
description: This section describes some of the key terms used in this integration.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Key terms used in this integration

This section describes some of the key terms used in this integration.

The following key terms are used during the installation and configuration. For more information about these terms, see the [ServiceNow Product Documentation website](https://servicenow.com/docs) and the [Splunk website](https://www.splunk.com/) and resources on [Splunk Resources](https://www.splunk.com/en_us/resources/getting-started.html) page.

-   **ServiceNow AI Platform**

    An enterprise ServiceNow product. The ServiceNow AI Platform is the base upon which individual components such as Security Incident Response \(SIR\), IT Service Management \(ITSM\), and other products are built.

-   **ServiceNow Splunkbase Addon**

    A ServiceNow application that is installed on your Splunk Enterprise Security console that supports the manual event forwarding option of the integration. Manual event forwarding is an optional feature of the integration. This ServiceNow Splunkbase add-on is not required for the automated notable event ingestion that is provided by the integration which pulls events from Splunk.

-   **Security Incident Response \(SIR\)**

    A ServiceNow AI Platform application that tracks the progress of security incidents from discovery and initial analysis, through containment, eradication, and recovery, and into the final post incident review and closure.

-   **Splunk Enterprise Security**

    Splunk Enterprise Security helps teams gain organization-wide visibility and security intelligence for continuous monitoring, incident response, SOC operations, and providing executives a window into business risk. Splunk Enterprise Security is a premium security solution requiring a paid license. This service is on a host or a Splunk cloud offering that is referred to as a Splunk console in this guide.

-   **Splunk Enterprise Security notable event**

    When a correlation search identifies an event or a pattern of events, it creates a notable event. Correlation searches filter the security data and correlate across events to identify a particular type of incident \(or pattern of events\) and then create notable events.

-   **Splunk event**

    One or more data elements that result in the notable events of the Splunk service. From your ServiceNow AI Platform instance, you can look up which Splunk events triggered ServiceNow AI Platform security incidents.

-   **MID Server**

    This application facilitates communication and movement of data between the ServiceNow AI Platform and external applications, data sources, and services. This application is typically required for integration with on-premises technologies, and, for this Splunk Enterprise Security event ingestion integration, the MID Server facilitates communication between the ServiceNow AI Platform and the on-premises instance of Splunk Enterprise Security. A MID Server is not required if you are integrating your ServiceNow AI Platform instance with a Splunk Cloud instance.

-   **Security incident admin \(sn\_si.admin\)**

    The user with this role oversees the configuration of the integration with the SIR product in your ServiceNow AI Platform instance.

-   **Security incident analyst \(sn\_si.analyst\)**

    The user with this role interacts with and analyzes security incidents in the ServiceNow Security Incident Response product.


