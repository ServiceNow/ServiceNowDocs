---
title: Configure Isolate Host capability in Microsoft Defender for Endpoint
description: Isolate the host from accessing the network in Microsoft Defender for Endpoint based on the severity of the attack. Isolating the host from the network enables you to prevent any other malicious activities or potential attacks on other hosts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/isolate-host-ms-defender-for-endpoint.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Additional Configurations, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Isolate Host capability in Microsoft Defender for Endpoint

Isolate the host from accessing the network in Microsoft Defender for Endpoint based on the severity of the attack. Isolating the host from the network enables you to prevent any other malicious activities or potential attacks on other hosts.

## Before you begin

Role required: sn\_si.admin or sn\_si.analyst

|Capability|Required|Description|
|----------|--------|-----------|
|Isolate Host|Isolation Type|\(Required\) Type of the Isolation \(Full or Selective\).|
|Comment|\(Required\) Comment to associate with the action.|

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the Microsoft Defender for Endpoint information.

3.  In the Related Links section, select **Run EDR Profile\(s\)**.

4.  Browse and select a profile with **Isolate Host capability** selected from the list of available profiles, and select **Submit**.

    Alternatively, you can perform the following steps:

    1.  In the related lists section, select **Show All Related Lists**.
    2.  Select the **Configuration Item** related list.
    3.  Select **Isolate Host** and select the corresponding capabilities.
5.  Validate the automation activity and activities section, and make sure that the data is as expect.

6.  View the data, and validate the isolate host details on the related lists.


**Parent Topic:**[Additional Configurations in Microsoft Defender for Endpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/additional-configurations-in-defender.md)

**Related topics**  


[Configure Remove Host Isolation capability in Microsoft Defender for Endpoint]()

[Configure Run Antivirus Scan capability in Microsoft Defender for Endpoint]()

[Configure Restrict App Execution capability in Microsoft Defender for Endpoint]()

[Configure Remove App Restriction capability in Microsoft Defender for Endpoint]()

[Configure Get Related Machines from Defender Capability in Microsoft Defender for Endpoint]()

[Configure Stop and Quarantine File capability in Microsoft Defender for Endpoint]()

