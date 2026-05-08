---
title: Set up your ServiceNow AI Platform instance for the Splunk Enterprise Security integration
description: The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform instance prior to installing the application from the ServiceNow Store.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up your ServiceNow AI Platform instance for the Splunk Enterprise Security integration

The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform® instance prior to installing the application from the ServiceNow Store.

Role required: sn\_si.ingestion\_profile\_admin.

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

Refer to the following table and verify that you have completed all the listed tasks before you download and install the application to ensure a smooth installation and configuration.

1.  Verify that you have assigned the required ServiceNow AI Platform® and Security Incident Response \(SIR\) roles.

    The following roles are required for the installation, setup, and use of the integration in your ServiceNow AI Platform® instance.

    -   A user with the ServiceNow AI Platform® administrator role \(admin\) installs the application from the ServiceNow Store and assigns the security incident administrator \(sn\_si.admin\) role.
    -   If you want to forward notable events manually from Splunk Enterprise Security for this integration, a user with the ServiceNow AI Platform® admin role assigns a user with the \(sn\_sec\_splunkes.api\_account\_access\) role in the ServiceNow AI Platform®. This role permits a user with the Splunk Enterprise Security administrator role to access the API in the ServiceNow AI Platform® that is required for manual event forwarding for this integration.

        The \(sn\_sec\_splunkes.api\_account\_access\) role is not required for the integration if you are ingesting notable events automatically from Splunk Enterprise Security into your ServiceNow AI Platform® instance.

    -   A user with the **sn\_si.ingestion\_profile\_admin** role oversees the following tasks in the ServiceNow AI Platform®:
        -   Names, creates, and edits event profiles.
        -   Selects and maps values from Splunk Enterprise Security to ServiceNow AI Platform® security incidents.
        -   Previews security incident details for accuracy prior to finalizing the configuration.
        -   Schedules on-going notable event ingestion.
        -   Enables notable event updates when a SIR incident is created and closed.
        -   Assigns the security incident analyst \(sn\_si.analyst\) role.
        -   Users with the sn\_si.analyst work with security incidents.
    For more information, see Managing roles.

2.  Assign the Splunk user role.

    Assign a Security Analyst \(ess\_analyst\) user role in Splunk ES to perform all integration-related activities on the Splunk server.

3.  Verify that you are using version 7.2.6 or later of the Splunk API. Earlier versions are not supported.

    If you have access to the Splunk Enterprise Security console, you have access to the API that is required for this integration. There is no other special setup required for the API.

4.  Verify that you have installed and configured a MID Server.

    A MID Server in your ServiceNow AI Platform® instance is required to connect to the Splunk service if the Splunk server is deployed within your corporate network. For information, see MID Server.

    If you are using the Splunk Enterprise Security Cloud service, a MID Server is not required.

5.  Verify that the ServiceNow core applications that are required to support the integration are installed and activated.

    The Security Incident Response Dependency plugin \(com.snc.si\_dep\) is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications required by the integration.

    Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

    1.  Security Incident Response
    2.  Security Integration Framework
    3.  Security Support Common
    For more information about installing the Security Operations core applications, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).


You have successfully set up your ServiceNow AI Platform® instance for the integration. The next step is to install the Splunk Enterprise Security Notable Event Ingestion application from the ServiceNow Store for the integration. For more information, see [Install and configure Splunk Enterprise Security Notable Event Ingestion integration](../task/splunk-event-ingest-install-and-configure-security.md).

