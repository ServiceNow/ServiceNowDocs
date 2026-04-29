---
title: How trigger conditions work with a configuration item for a profile
description: You can configure the profile settings so that a profile runs only when a set of specific conditions is met or you can set up a profile to search for specific field values on a security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# How trigger conditions work with a configuration item for a profile

You can configure the profile settings so that a profile runs only when a set of specific conditions is met or you can set up a profile to search for specific field values on a security incident.

After you create a profile and select the CrowdStrike Falcon Insight capabilities that you want the profile to run on, you can set trigger conditions so that your profile runs automatically when the default field values match the ServiceNow AI Platform security incident.

By default, the integration uses the **Configuration Item** \(CI\) field on a security incident. This field is used to match your asset IDs with the information that is stored in the ServiceNow AI Platform database. When a SIR security incident is created by a security event and a profile is activated, your assets are scanned for a matching value on the host name or an IP address.

When a matching value is found in the database, that data is gathered from the CrowdStrike Falcon Insight console and is pulled into your ServiceNow AI Platform instance where it is displayed on the related lists of a security incident.

The following example shows a Configuration Item field that is populated with a host name on a SIR security incident.![Configuration item field populated with a host name.](../image/falcon-insight-trigger-ci.png)

When the **Configuration item** \(CI\) field is not populated with a host name or an IP address that matches the database, you can select another field on the security incident to display any matching CI data that you find while scanning your assets.

When you are configuring the profile setup, you can select an alternate **CI trigger** field for endpoint identification to ensure that the CI data from the CrowdStrike Falcon Insight lookup is populated on the associated security incident. You can select any field on the security incident as an alternate CI trigger field, including custom fields that you create. If the CI field is not populated on the associated security incident when the incident is created, select the alternate CI field to ensure that your profiles get triggered.

The following example shows an alternate field that is populated with a host name on a SIR security incident. The alternate field is the **Description** field.![Alternate field used as a trigger instead of the CI field.](../image/falcon-insight-trigger-description.png)

