---
title: Use the Endpoint Detection playbook
description: Use this playbook to investigate malware alerts triggered on a host or endpoint. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Endpoint Detection playbook.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Playbook for Endpoint Detection, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Endpoint Detection playbook

Use this playbook to investigate malware alerts triggered on a host or endpoint. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Endpoint Detection playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, you need to verify if the file or hash is malicious by analyzing the Threat lookup results in SIR and gathering intel from VirusTotal, WildFire, ThreatCrowd, etc.

2.  In Action 2, you need to check whether the file or hash is malicious or not.

3.  In Action 3, if the file or hash is malicious, perform the following actions:

    1.  In Action 4, you need to identify the application or the process being detected as a threat and gather information about the detection reasoning to proceed further on to safe listing.

        ![Response tasks to determine whether the file is not malicious.](../image/playbook-endpoint-detection-malicious.png "Endpoint Detection playbook")

    2.  In Action 5, you need to check whether the application is from a trusted source \(For example, Microsoft, Adobe, or other well-known software vendors\).

    3.  In Action 6, if the application is from a trusted source, then you need to take action on the CrowdStrike Falcon alerts.

        ![Response tasks to take action on CrowdStrike Falcon alerts.](../image/playbook-endpoint-detection-crowd.png "CrowdStrike Falcon alerts")

    4.  In Action 7, perform the following actions:

        1.  Navigate to **CrowdStrike Falcon** &gt; **Detections** tab.
        2.  Click on the CrowdStrike Falcon alert.
        3.  Under the Execution Details tab, click **Edit Hash** action in Hash Prevention Action.
        4.  Perform the required steps.

            **Note:** Choose the **Never Block** option carefully, as only certain hosts may be allowed to use the application with a valid business justification. However, additional alertings may need to be set up for other hosts.

    5.  In Action 8, if the application isn’t from a trusted source, then you need to choose whether you want to waive the file or application from the device locally.

        In Action 10, if you want to waive the file or application from the device locally, perform the following actions:

        1.  In Action 11, navigate to the **Quarantined Files** tab, and filter the endpoint by searching for the device name.
        2.  Select the file that needs to be waived locally, and click **Release**.

            **Note:**

            -   The file still runs on this specific endpoint. However, detection and quarantine continue to happen on all other hosts.
            -   To bulk release the quarantine file on multiple hosts, select the appropriate file name and status. Click on **Select**, and select **Release**.
        In Action 12, if you don't want to waive the file or application from the device locally, you can redirect the user to the IT Support for requesting installation of the approved applications.

4.  In Action 14, if the file or hash isn’t malicious, perform the following actions:

    1.  In Action 15, you need to determine if the file/hash is high risk or low risk based on the user's role \(department or position that handles sensitive information\), the type of application \(ransomware, rootkit, etc.\), and the impact of the application \(how many users were impacted\).

    2.  In Action 16, if the file is a high-risk file, then perform the following actions:

        1.  In Action 17, review the results with the Threat Intel Team.
        2.  In Action 18, run the Malware byte scan on the file.
        3.  In Action 19, initiate Forensic Analysis.
        4.  In Action 20, based on the result of the Forensic Analysis, perform host isolation and remove the malicious file/hash.
        5.  In Action 21, if the user credentials are compromised or the threat can’t be removed easily, raise an IT ticket to reset the user credentials or reimage the machine as required.
        6.  In Action 22, perform host unisolation.
        ![Response tasks to determine if it's a high-risk file.](../image/playbook-endpoint-detection-risk.png "High-risk file")

    3.  In Action 23, if the file isn’t a high-risk file, then perform the following actions:

        1.  Navigate to **CrowdStrike Falcon** &gt; **Configurations** tab.
        2.  From the Configurations tab, navigate to **Prevention Hashes** &gt; **** &gt; **Upload Hash** &gt; **Add the Hash**.
        3.  Choose the required OS, and select **Always Block**.
5.  In Action 24, a response task is created for the user to complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for Endpoint Detection](../concept/playbook-endpoint-detection.md)

