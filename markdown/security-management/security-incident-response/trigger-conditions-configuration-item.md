---
title: Trigger conditions in a configuration item
description: After you create a profile and select the Microsoft Defender for Endpoint capabilities that you want the profile to run, configure the profile settings so that the profile runs only when a set of specific conditions is met.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Trigger conditions in a configuration item

After you create a profile and select the Microsoft Defender for Endpoint capabilities that you want the profile to run, configure the profile settings so that the profile runs only when a set of specific conditions is met.

## How to trigger conditions in a configuration item

You can set trigger conditions so the profile runs automatically whenever a security incident is created that matches the trigger condition. If the trigger condition is not set, these profiles can be manually run by clicking the Run EDR profile\(s\) form on the security incident, and selecting the profile.

By default, the integration uses the Configuration Item \(CI\) field on the Security incident. This value is used to match the IDs of your assets with the information stored in the ServiceNow AI Platform Configuration Management Database \(CMDB\). When a security incident is created, and a profile is run either automatically or manually, the CMDB is searched to retrieve the host name or IP address based on the value of the CI field. The host name or IP is used to resolve the Agent ID on Microsoft Defender for Endpoint to identify the endpoint.

In an ideal scenario, a matching value is found in the database, and data is gathered from the Microsoft Defender for Endpoint console for the matching asset. The data for various capabilities are pulled into your ServiceNow AI Platform Configuration Management Database \(CMDB\) instance and displayed in the related lists of a security incident. When the Configuration item \(CI\) field is not populated on the security incident with a host name with or an IP address that matches the database, you can select an alternate field on the security incident that contains either the host name or the IP to perform the Agent ID resolution.

During the configuration step of the profile setup, you can select an alternate CI field for endpoint identification to ensure that you are able to identify the endpoint on Microsoft Defender for Endpoint. You can select any field on the security incident as an alternate CI trigger field, including custom fields that you create. By selecting this alternate CI field as a backup, you ensure that your profiles run even if the CI field is not populated on the associated security incident on incident creation.

**Note:** The alternate CI fields are considered only for capabilities that could be added to a profile. These capabilities include Get Host Details, Get Logged On Users, Isolate Host, and Remove Isolation. For all the additional actions, the alternate CI must be configured in the Default Settings module.

