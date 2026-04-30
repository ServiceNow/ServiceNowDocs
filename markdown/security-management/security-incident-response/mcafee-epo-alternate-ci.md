---
title: Defining triggering conditions with a Configuration item \(CI\) field for a McAfee ePO profile
description: After you create a profile and select the McAfee ePO capabilities that you want the profile to run, you configure the settings of the profile so that it runs only when a set of specific conditions are met.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [McAfee ePO integration capability profiles, McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Defining triggering conditions with a Configuration item \(CI\) field for a McAfee ePO profile

After you create a profile and select the McAfee ePO capabilities that you want the profile to run, you configure the settings of the profile so that it runs only when a set of specific conditions are met.

You have the flexibility to set these triggering conditions so the profile runs automatically based on the default field values that are matched on a ServiceNow AI Platform® Security Incident Response security incident. Alternatively, you can set up a profile so it searches for matches on field values you specifically identify on the security incident.

One of the keys to the functionality of the integration and how a profile works is the Configuration Item \(CI\) field on the ServiceNow AI Platform® Security Incident Response \(SIR\) security incident. The value of this field is the principle value on a security incident. This value is used to match the IDs of your assets with the information stored in the ServiceNow AI Platform® database. When a SIR security incident is created by a security event, and a profile is activated, your assets are scanned for a matching value for a Fully Qualified Domain Name \(FQDN\), a host name, or an IP address based on the value of the Configuration Item field.

In an ideal case, a matching value is found in the database, and data can be gathered from the McAfee ePO console for the matching asset, pulled into your ServiceNow AI Platform® instance, and displayed on the related lists of a security incident. The following figure shows an example of the Configuration Item field populated with a host name on a SIR security incident.

![CI field with a value highlighted.](../image/mcafee-si-ci-fieldexmp.png "Security incident - Configuration item")

In cases when the Configuration item \(CI\) field is not populated on the security incident, or a match cannot be found for a FQDN, a host name, or an IP address that matches the database, you can select an alternate field on the security incident to display any matching CI enrichment data found during the scan of your assets.

During the configuration step of the profile setup, you can select an alternate CI trigger field for endpoint identification to ensure that the CI enrichment data from the McAfee ePO lookup is populated on the associated security incident. You can select any field on the security incident as an alternate CI trigger field including custom fields that you create. By selecting this alternate CI field as a backup, you ensure that your profiles run even if the CI field is not populated on the associated security incident upon incident creation.

As an example, as a security operations center \(SOC\) analyst, you create a custom field for a security incident called, IP Address on my security incident. If you do not think that the value of this custom field will be displayed in the Configuration Item field on the security incident upon incident creation, you can set up the profile so it scans for this IP address. If matched, the IP address is displayed on the security incident in the field of your choice. In the following figure, the `Identified CI` field is selected as the alternate field for the IP Address for this example.

![Identified CI field highlighted as alternate CI field.](../image/mcafee-si-ci-fieldexmp2.png "Security incident - Identified CI")

The following figure illustrates how the first search of the workflow scans for matches for Configuration Items. If the Alternate CI trigger field is enabled, the second search scans for matches for alternate values.

![Alt CI flow.](../image/mcafee-alt-ci.png "Configuration items workflow")

If matching IDs are not found for the CI field or the alternate CI field, a work note is logged and a message is displayed on the security incident. When no matches are found, no enrichment data are populated on the security incidents related to the event.

You enable the alternate CI trigger field and select the field you want to display the matching ID during the configuration step for a profile. This step for enabling the alternate CI field is described along with the other profile configuration requirements in [Configuring profiles for the McAfee ePO integration](mcafee-epo-configuring-profile.md).

**Parent Topic:**[McAfee ePO integration capability profiles](mcafee-epo-creating-profiles.md)

