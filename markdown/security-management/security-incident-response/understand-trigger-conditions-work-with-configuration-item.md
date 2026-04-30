---
title: Understand how trigger conditions work with a configuration item
description: After you create a profile and select the FireEye capabilities that you want the profile to run, configure the profile settings so that it runs only when a set of specific conditions are met.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Understand how trigger conditions work with a configuration item

After you create a profile and select the FireEye capabilities that you want the profile to run, configure the profile settings so that it runs only when a set of specific conditions are met.

You can set trigger conditions so the profile runs automatically whenever a security incident matching the trigger condition is created. If the trigger condition is not set, these profiles can be manually run by clicking the form 'Run EDR profile\(s\)' on the security incident, and selecting the profile.

By default, the integration uses the Configuration Item \(CI\) field on the Security incident. This value is used to match the IDs of your assets with the information stored in the Now Platform CMDB. When a security incident is created, and a profile is run either automatically or manually, the CMDB is searched to retrieve the hostname and/or IP address based on the value of the CI field. The host name and or IP is used to resolve the Agent ID on FireEye HX to identify the endpoint.

In an ideal case, a matching value is found in the database, and data is gathered from the FireEye HX console for the matching asset. The data for various capabilities are pulled into your ServiceNow AI Platform instance and displayed in the related lists of a security incidents. When the Configuration item \(CI\) field is not populated on the security incident with a host name, or an IP address that matches the database, you can select an alternate field on the security incident that contains either the host name or the IP to perform the Agent ID resolution.

During the configuration step of the profile setup, you can select an alternate CI field for endpoint identification to ensure that the you are able to identify the endpoint on FireEye HX. You can select any field on the security incident as an alternate CI trigger field including custom fields that you create. By selecting this alternate CI field as a backup, you ensure that your profiles run even if the CI field is not populated on the associated security incident upon incident creation.

**Note:** The alternate CI fields are considered only for capabilities that could be added to a profile. For all the additional actions, the alternate CI is picked from the default settings page.

![Security Incident New record](../image/trigger-condition.png)

