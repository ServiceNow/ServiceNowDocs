---
title: Configure Stop and Quarantine File capability in Microsoft Defender for Endpoint
description: Stop and quarantine files from the Microsoft Defender platform.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Additional Configurations, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Stop and Quarantine File capability in Microsoft Defender for Endpoint

Stop and quarantine files from the Microsoft Defender platform.

## Before you begin

Supported Observable Types: SHA1 hash.

|Input|Description|
|-----|-----------|
|Comment|\(Required: Comment to associate with the action\)|

Role required: sn\_si.admin or sn\_si.analyst

## About this task

You can run the Stop and Quarantine File action on the particular observables of type SHA1 only. Store the details on the Additional Actions on Endpoint table. You can trigger the Stop and Quarantine File capability from the Microsoft Defender for Endpoint Related Machines details related list.

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the Microsoft Defender for Endpoint information.

3.  In the related links section, click **Show All Related Lists**.

4.  Click the Microsoft Defender for Endpoint Related Machines Details related list.

5.  Select one or more records.

6.  From the **Actions** on selected rows, select the **Stop and Quarantine File** capability.

7.  Validate the automation activity and activities section.

8.  View the data, and validate the data on the related lists.

9.  View the automation activities of the execution, and validate them.


**Parent Topic:**[Additional Configurations in Microsoft Defender for Endpoint](../concept/additional-configurations-in-defender.md)

**Related topics**  


[Configure Isolate Host capability in Microsoft Defender for Endpoint](isolate-host-ms-defender-for-endpoint.md)

[Configure Remove Host Isolation capability in Microsoft Defender for Endpoint](remove-isolation-ms-defender-for-endpoint.md)

[Configure Run Antivirus Scan capability in Microsoft Defender for Endpoint](run-antivirus-scan-capability-ms-defender.md)

[Configure Restrict App Execution capability in Microsoft Defender for Endpoint](restrict-app-execution-capability-ms-defender.md)

[Configure Remove App Restriction capability in Microsoft Defender for Endpoint](remove-app-restriction-capability-ms-defender.md)

[Configure Get Related Machines from Defender Capability in Microsoft Defender for Endpoint](get-related-machines-defender-capability-ms-defender.md)

