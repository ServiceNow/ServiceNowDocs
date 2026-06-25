---
title: Configure Run Antivirus Scan capability in Microsoft Defender for Endpoint
description: Remotely initiate an anti virus scan to help identify and remediate malware that might be present on a compromised device. Run the scan as part of the investigation or response process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/run-antivirus-scan-capability-ms-defender.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Additional Configurations, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Run Antivirus Scan capability in Microsoft Defender for Endpoint

Remotely initiate an anti virus scan to help identify and remediate malware that might be present on a compromised device. Run the scan as part of the investigation or response process.

## Before you begin

Role required: sn\_si.admin or sn\_si.analyst

|Input|Description|
|-----|-----------|
|Scan Type|\(Required\) Type of the Scan \(Full or Quick\).|
|Comment|\(Required\) Comment to associate with the action.|

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the Microsoft Defender for Endpoint information.

    1.  In the related links section, select **Run Additional Actions on Endpoint**.

    2.  Browse and select the required capability.

        For example, select **Run Antivirus Scan** capability.

    Alternatively, you can perform the following steps:

    1.  In the related lists section, select **Show All Related Lists**.
    2.  Select the **Configuration Item** related list.
    3.  Select the added configuration items, and from the Actions on selected rows, select **Run Additional Actions on Endpoint**.
    After you select the **Run Antivirus Scan** capability implementation, the **Additional Scan Type** and **Comment input** fields are displayed.

3.  Select the **Scan type** that you want to run \(Quick or Full\), and add a comment before executing the scan.

4.  To initiate the anti virus scan, select **Run Additional Action**.

5.  View the automation activities of the execution, and validate them.

6.  Validate the status of the action on the Additional Actions on Endpoint related lists.


**Parent Topic:**[Additional Configurations in Microsoft Defender for Endpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/additional-configurations-in-defender.md)

**Related topics**  


[Configure Isolate Host capability in Microsoft Defender for Endpoint]()

[Configure Remove Host Isolation capability in Microsoft Defender for Endpoint]()

[Configure Restrict App Execution capability in Microsoft Defender for Endpoint]()

[Configure Remove App Restriction capability in Microsoft Defender for Endpoint]()

[Configure Get Related Machines from Defender Capability in Microsoft Defender for Endpoint]()

[Configure Stop and Quarantine File capability in Microsoft Defender for Endpoint]()

