---
title: Configure Remove App Restriction capability in Microsoft Defender for Endpoint
description: If needed, remove the restrictions of any application on the device.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Additional Configurations, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Remove App Restriction capability in Microsoft Defender for Endpoint

If needed, remove the restrictions of any application on the device.

## Before you begin

Role required: sn\_si.admin or sn\_si.analyst

|Input|Description|
|-----|-----------|
|Comment|\(Required: Comment to associate with the action\)|

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the Microsoft Defender for Endpoint information.

    1.  In the related links section, click **Run Additional Actions on Endpoint**.

    2.  Browse and select the **Remove App Restriction** capability.

    ![Remove App Restriction capability implementation](../image/remove_app.png "Remove App Restriction")

    Alternatively, you can perform the following steps:

    1.  In the related lists section, click **Show All Related Lists**.
    2.  Click the **Configuration Item** related list.
    3.  Select the added configuration items.
    4.  Select **Run Additional Actions on Endpoint**.
    The Additional Comment input field is displayed.

3.  To remove app restriction, click **Run Additional Action**.

4.  View the automation activities of the execution, and validate them.

5.  Validate the status of the action on the Additional Actions on Endpoint related lists.


**Parent Topic:**[Additional Configurations in Microsoft Defender for Endpoint](../concept/additional-configurations-in-defender.md)

**Related topics**  


[Configure Isolate Host capability in Microsoft Defender for Endpoint](isolate-host-ms-defender-for-endpoint.md)

[Configure Remove Host Isolation capability in Microsoft Defender for Endpoint](remove-isolation-ms-defender-for-endpoint.md)

[Configure Run Antivirus Scan capability in Microsoft Defender for Endpoint](run-antivirus-scan-capability-ms-defender.md)

[Configure Restrict App Execution capability in Microsoft Defender for Endpoint](restrict-app-execution-capability-ms-defender.md)

[Configure Get Related Machines from Defender Capability in Microsoft Defender for Endpoint](get-related-machines-defender-capability-ms-defender.md)

[Configure Stop and Quarantine File capability in Microsoft Defender for Endpoint](stop-and-quarantine-file-capability.md)

