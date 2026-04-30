---
title: Configure Remove Host Isolation capability in Microsoft Defender for Endpoint
description: If needed, remove the isolation of a host that was previously isolated from the network in Microsoft Defender for Endpoint. You can prevent any other malicious activities or potential attacks on other hosts.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Additional Configurations, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Remove Host Isolation capability in Microsoft Defender for Endpoint

If needed, remove the isolation of a host that was previously isolated from the network in Microsoft Defender for Endpoint. You can prevent any other malicious activities or potential attacks on other hosts.

## Before you begin

|Capability|Required Input|Description|
|----------|--------------|-----------|
|Remove Isolation|Comment|\(Required\) Comment to associate with the action.|

Role required: sn\_si.admin or sn\_si.analyst

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the Microsoft Defender for Endpoint information.

3.  In the Related Links section, click **Run EDR Profile\(s\)**.

4.  Browse and select a profile with **Remove Isolation capability** selected from the list of available profiles, and click **Submit**.

    ![Remove Isolation capability in Microsoft Defender for Endpoint](../image/remove_isolation.png "Remove Isolation")

    Alternatively, you can perform the following steps:

    1.  Click **Show All Related Lists** in the related lists section.
    2.  Click the **Configuration Item** related list.
    3.  Select **Remove Isolation** and select the corresponding capabilities.
5.  Validate the automation activity and activities section.

6.  View the data, and validate the isolate host details on the related lists.

7.  Validate the automation activities of the execution.


**Parent Topic:**[Additional Configurations in Microsoft Defender for Endpoint](../concept/additional-configurations-in-defender.md)

**Related topics**  


[Configure Isolate Host capability in Microsoft Defender for Endpoint](isolate-host-ms-defender-for-endpoint.md)

[Configure Run Antivirus Scan capability in Microsoft Defender for Endpoint](run-antivirus-scan-capability-ms-defender.md)

[Configure Restrict App Execution capability in Microsoft Defender for Endpoint](restrict-app-execution-capability-ms-defender.md)

[Configure Remove App Restriction capability in Microsoft Defender for Endpoint](remove-app-restriction-capability-ms-defender.md)

[Configure Get Related Machines from Defender Capability in Microsoft Defender for Endpoint](get-related-machines-defender-capability-ms-defender.md)

[Configure Stop and Quarantine File capability in Microsoft Defender for Endpoint](stop-and-quarantine-file-capability.md)

