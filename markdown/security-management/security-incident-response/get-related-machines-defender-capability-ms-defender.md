---
title: Configure Get Related Machines from Defender Capability in Microsoft Defender for Endpoint
description: Get the list of related machines of specific observables.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Additional Configurations in Microsoft Defender for Endpoint, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Get Related Machines from Defender Capability in Microsoft Defender for Endpoint

Get the list of related machines of specific observables.

## Before you begin

**Note:** Supported Observable Types are Domain name, SHA1 hash, and Username.

Role required: sn\_si.admin or sn\_si.analyst

## About this task

You can retrieve the list of machines that have accessed the particular observables. You can store the list on the Microsoft Defender for Endpoint Related Machines Details table. You can trigger the Get Related Machines from Defender capability from the Associated Observables related list.

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the Microsoft Defender for Endpoint information.

    ![Get Related Machines from Defender capability implementation](../image/get_related_machines.png "Get Related Machines from Defender")

3.  In the Related links section, click **Show IoC**.

4.  Click the Associated Observables related list.

5.  Select the associated observables.

6.  From the Actions list, select the **Get Related Machines from Defender** capability.

7.  Validate the automation activity and activities section.

8.  View the data, and validate the Microsoft Defender for Endpoint Related Machines details on the related lists.

9.  View the automation activities of the execution, and validate them.


**Parent Topic:**[Additional Configurations in Microsoft Defender for Endpoint](../concept/additional-configurations-in-defender.md)

**Related topics**  


[Configure Isolate Host capability in Microsoft Defender for Endpoint](isolate-host-ms-defender-for-endpoint.md)

[Configure Remove Host Isolation capability in Microsoft Defender for Endpoint](remove-isolation-ms-defender-for-endpoint.md)

[Configure Run Antivirus Scan capability in Microsoft Defender for Endpoint](run-antivirus-scan-capability-ms-defender.md)

[Configure Restrict App Execution capability in Microsoft Defender for Endpoint](restrict-app-execution-capability-ms-defender.md)

[Configure Remove App Restriction capability in Microsoft Defender for Endpoint](remove-app-restriction-capability-ms-defender.md)

[Configure Stop and Quarantine File capability in Microsoft Defender for Endpoint](stop-and-quarantine-file-capability.md)

