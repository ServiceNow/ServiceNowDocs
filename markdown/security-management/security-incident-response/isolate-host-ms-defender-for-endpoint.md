---
title: Configure Isolate Host capability in Microsoft Defender for Endpoint
description: Isolate the host from accessing the network in Microsoft Defender for Endpoint based on the severity of the attack. Isolating the host from the network enables you to prevent any other malicious activities or potential attacks on other hosts.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Additional Configurations in Microsoft Defender for Endpoint, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
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

3.  In the Related Links section, click **Run EDR Profile\(s\)**.

4.  Browse and select a profile with **Isolate Host capability** selected from the list of available profiles, and click **Submit**.

    ![Isolate Host capability in Microsoft Defender for Endpoint](../image/Isolate_host.png "Isolate Host")

    Alternatively, you can perform the following steps:

    1.  In the related lists section, click **Show All Related Lists**.
    2.  Click the **Configuration Item** related list.
    3.  Select **Isolate Host** and select the corresponding capabilities.
5.  Validate the automation activity and activities section, and make sure that the data is as expect.

6.  View the data, and validate the isolate host details on the related lists.


**Parent Topic:**[Additional Configurations in Microsoft Defender for Endpoint](../concept/additional-configurations-in-defender.md)

**Related topics**  


[Configure Remove Host Isolation capability in Microsoft Defender for Endpoint](remove-isolation-ms-defender-for-endpoint.md)

[Configure Run Antivirus Scan capability in Microsoft Defender for Endpoint](run-antivirus-scan-capability-ms-defender.md)

[Configure Restrict App Execution capability in Microsoft Defender for Endpoint](restrict-app-execution-capability-ms-defender.md)

[Configure Remove App Restriction capability in Microsoft Defender for Endpoint](remove-app-restriction-capability-ms-defender.md)

[Configure Get Related Machines from Defender Capability in Microsoft Defender for Endpoint](get-related-machines-defender-capability-ms-defender.md)

[Configure Stop and Quarantine File capability in Microsoft Defender for Endpoint](stop-and-quarantine-file-capability.md)

