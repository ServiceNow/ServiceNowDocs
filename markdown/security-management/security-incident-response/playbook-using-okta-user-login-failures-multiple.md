---
title: Use the Okta User Login Failures from Multiple IPs playbook
description: Use this playbook to investigate security incidents for user login failures on Okta. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Okta User Login Failures from Multiple IPs playbook.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Playbook for Okta User Login Failures from Multiple IPs, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Okta User Login Failures from Multiple IPs playbook

Use this playbook to investigate security incidents for user login failures on Okta. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Okta User Login Failures from Multiple IPs playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, perform the following tasks:

    -   Identify the user account that is being targeted.
    -   Verify the IP subnet and check if they all belong to the same Autonomous System Number \(ASN\) owner.
2.  In Action 2, check whether there were any successful logins before or after the activity from the different IPs/ASNs.

3.  In Action 3, if there were no successful logins before or after the activity from the different IPs/ASNs, then in Action 4, verify whether the devices in which the authentication is being performed are known user agents.

    If the devices are authenticated by known user agents, then the flow ends.

    ![Response tasks if there were no successful logins before or after the activity from the different IPs/ASNs.](../image/playbook-okta-login-failures-ips-overview.png "Okta User Login Failures from Multiple IPs playbook")

4.  In Action 5, based on the investigation, reach out to the user through out-of-band communication \(For example, phone call or email\) to check if the activity is due to account lockout or a wrong password provided by the user.

5.  In Action 6, check whether the user provided a valid business justification.

6.  In Action 7, if the user provided a valid business justification, perform the following tasks.

    1.  In Action 8, create a response task to document the findings so far.

    2.  In Action 9, create a response to initiate a post incident review.

        In Action 10, the flow ends.

7.  In Action 11, verify the IP address and client user agent from where the authentication request is made and try to identify if it is part of a brute force activity by pivoting on the IP address.

8.  In Action 12, inform the affected user that account will be locked for investigation purposes.

    You can use the provided email template to inform the affected user.

    ![Response tasks if there were successful logins before or after the activity from the different IPs/ASNs.](../image/playbook-okta-login-failures-ips-investigate.png "Using the Okta User Login Failures from Multiple IPs playbook")

9.  In Action 13, work with the IT Support team to lock the account out and start investigating the scope of the compromise.

10. In Action 14, reset the user password and send an email to the user with the default password.

11. In Action 15, block the malicious Source IPs.

12. In Action 16, get help from the IT Support Team to the release the account and bring it back to operational standards.

13. In Action 17, document the findings so far.

14. In Action 18, complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for Okta User Login Failures from Multiple IPs](../concept/playbook-okta-user-login-failures-ips.md)

