---
title: Playbook for Failed Login Manual
description: When a user makes certain unsuccessful login attempts \(according to the SIM configuration\), a security incident is created.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for Failed Login Manual

When a user makes certain unsuccessful login attempts \(according to the SIM configuration\), a security incident is created.

These unsuccessful login attempts may either be false positives or attempts made by attackers to obtain access to user email accounts. In such scenarios, the Failed Login Manual playbook can provide guidance and help optimize the investigation of failed login security incidents.

## Prerequisites

Role required:

-   sn\_si.admin
-   flow\_designer

Spoke: Install Security Operations Spoke \(sn\_sec\_spoke\)

## Key capabilities

The Failed login playbook covers the following capabilities to investigate security incidents:

1.  Checks if the affected user is an active/inactive user
2.  Filters allowed list observables
3.  Enriches the observables
4.  Performs automated threat lookup.
5.  Sends automated email to the user to confirm the failed login attempt.
6.  Assigns tasks to analyst to investigate user access
7.  Identifies malicious observables and block IPs and URLs.
8.  Resets user password.
9.  Updates security incident status
10. Assigns tasks to a security analyst to handle post-incident review.

## Capabilities required

-   Threat Lookup \(Virus Total, Hybrid Analysis\)
-   Observable Enrichment \(Whois, ReverseWhois\)
-   Sighting Search \(Splunk, QRadar\)
-   Observable Blocking \(CheckPoint, Palo Alto\)

For more information, see the [ServiceNow store](https://store.servicenow.com/).

## Security analyst experience

To understand how to resolve security threats in a step-by-step manner, see [Resolve security threats with the playbook](../task/use-the-playbook.md#).

## Using Failed Login playbook with Flow Designer capabilities

**Getting Started**

1.  Login as a user with sn\_si.user and flow\_designer roles.
2.  Navigate to **Flow Designer** &gt; **Designer** and click on the **Failed Login** playbook.
3.  Make a copy of the following flows to copy the Failed Login Playbook and make the necessary modifications. \(This is an optional step. Follow this step only if you plan to customize or make specific changes to the flow\).
    -   Failed Login Manual Playbook V1
    -   Failed Login - Parse User's reply and Update Response Task V1
4.  Make the necessary modifications according to your requirement. \(This is an optional step. Follow this step only if you plan to customize or make specific changes to the flow\).
5.  Activate the playbooks.
    -   Activate the main flow to use the playbook available with the base system.
    -   Activate the copied flows after making any modifications according to your requirements.

The following image shows a copy of the Failed Login Manual playbook. Review the steps below to get an understanding of the various actions in the playbook.

![Copy of failed login manual playbook](../image/cj-sir-failed-login-1.png)

This playbook is triggered and associated with the security incident when the following conditions are met:

-   Category is Failed Login
-   Has one or more affected users
-   Security incident isn’t closed or canceled

![Failed login playbook: trigger](../image/cj-sir-failed-login-trigger.png)

The following steps walks you through the actions, tasks, and subflows that are available in the Failed Login Manual playbook.

1.  When the playbook starts executing, in Step 1, the playbook is automatically updated with a worknote showing the security incident with the failed login category has been assigned.

    ![Failed login playbook: step 1](../image/cj-sir-failed-login-2.png)

2.  In Step 2, the playbook is updated and moved to the Analysis state.
3.  In Step 3, the playbook checks if the Affected User is an active or inactive user. If the user is inactive, a worknote is added to the security incident that the user account is inactive.

    ![Failed login playbook: step 3](../image/cj-sir-failed-login-3.png)

    **Note:** In step 3 of the flow, the flow checks inactive users in the `sn_si_incident` table available in ServiceNow. This step is provided as a guideline and must be modified for your specific environment. If you want to use this functionality, we recommend that you have an Active Directory integration set up in your environment. You can check with your Active Directory integration to find the user status and depending on the response, you can design the next steps for your playbook.

    If you don’t have an Active Directory integration, replace this step with a manual task for the security analyst to work with the IT team to block the user and move forward with the rest of the steps in the playbook.

4.  In Step 4, the observables for the security incident are retrieved.
5.  In Step 5, the observables are identified.
6.  If no observables are found, a manual response task is created in Step 6 and the flow ends.

    ![Failed login playbook: step 6](../image/cj-sir-failed-login-4.png)

7.  If observables are found in Step 7, observables that aren’t allowed list are identified.
8.  If at least one of the observables is not allowed list, the following steps are performed:
    1.  Steps 8.1 and 8.2 are executed. Observables are retrieved and an automated response task is initiated.

        ![Failed login playbook: steps 8.1 and 8.2](../image/cj-sir-failed-login-5.png)

    2.  After the automated task has been created, Step 8.3 \(8.3.1.1 and 8.3.2.1\) is run and the Enrich Observables and Threat Lookup integrations are executed. Note that these are subflows that have been included in the playbook.

        ![Failed playbook flow: steps 8.3.1.1 and 8.3.1.2](../image/cj-sir-failed-login-6.png)

    3.  In Step 8.4, after the integrations have been completed, the security incident record is updated.
    4.  In Step 8.5, a new response task is created to indicate the next automated task that will take place.
    5.  In Step 8.6, the Sighting Search integration will be run on the observables.

        ![Failed login playbook: step 8.6](../image/cj-sir-failed-login-7.png)

    6.  After the Sighting Search subflow has been completed, in Step 8.7, the security incident is updated.
    7.  In Step 8.8, the observables are checked to see if they are malicious.
    8.  If the observables are not malicious, and if the user account is active, an automated email is sent to the user to reconfirm the unsuccessful login attempts. A manual response task is created to identify the observables and add them to the security incident. The playbook then ends at this stage.
    9.  If the observables are malicious, three response tasks are created:

        1.  An automated email is sent to the user to confirm **\(Yes or No\)** the unsuccessful login attempts. If the user responds Yes:

            1.  The security incident status is updated to **Contain**.
            2.  An automated email is sent to the user to reset the password.
            3.  The Reset Password subflow is initiated and an email is sent to the user when the task has been completed.
            **Note:** The Reset Password step is provided as a guideline. The steps in the flow reset the password for the user's account in the ServiceNow System. But the process to reset the password may be different depending on your environment. You can check with your Active Directory integration to reset the password of users automatically. If you don’t have an Active Directory integration, replace this step with a manual task for the security analyst to work with the respective IT team to reset users password and move forward with the rest of the steps in the playbook, upon completing the respective task.

        2.  If the user responds No, an automated email is sent to the user to reconfirm the response. The security analyst has to manually take appropriate actions.
        3.  If the user doesn’t respond to the automated email, the security analyst must update the security incident manually and provide a response. A manual task is created to validate if the user account has been compromised.
        ![Failed login playbook: step 8.10.2](../image/cj-sir-failed-login-8.png)

9.  In Step 8.10.3, the security incident is state is updated.
10. In Step 8.10.4, an automated task is created to verify if the Create Block Requests for Malicious IPs and URLs capability implementation is available. If the capability implementation is available, the Create Block Requests subflow is executed. If this isn’t available, the security incident is updated and a worknote is posted to indicate that the capability implementation isn’t available.
11. In Step 9, the security incident is updated and the state is set to **Review**.
12. In Step 10, a response task is created for the user to complete the post-incident review before closing the task.

**Parent Topic:**[Flow-based Playbooks](playbook-flow-based.md)

