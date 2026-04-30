---
title: Playbook for Child Security Incident Automation
description: Duplicate security incidents are categorized as child security incidents and are rolled up to the parent security incidents.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for Child Security Incident Automation

Duplicate security incidents are categorized as child security incidents and are rolled up to the parent security incidents.

The Child Security Incident Automation playbook helps reduce the time required to investigate and close duplicate security incidents. This playbook automatically rolls up specific unique artifacts of the child security incident \(observables, affected users, CIs\) to the parent security incident.

## Prerequisites

Role required:

-   sn\_si.admin
-   flow\_designer

Spoke: Install Security Operations Spoke \(sn\_sec\_spoke\)

## Key capabilities

The Child Automation playbook covers the following capabilities:

1.  Moves the security incident to the **Analysis** stage.
2.  Eliminates duplicates and adds \(rolls up\) the affected users and CIs to the parent security incident.
3.  Adds observables from the child incident to the parent security incident.
4.  Closes or cancels the child security incident when the parent security incident is closed.

## Capabilities required

For more information, see the [ServiceNow store](https://store.servicenow.com/).

## Security analyst experience

To understand how to resolve security threats in a step-by-step manner, see [Resolve security threats with the playbook](../task/use-the-playbook.md#).

## Deeper understanding of the Child Security Incident Automation playbook with Flow Designer capabilities

**Getting Started**

1.  Login as a user with sn\_si.user and flow\_designer roles.
2.  Navigate to **Flow Designer** &gt; **Designer** and click on the Failed Login playbook.
3.  Make a copy of the Child Security Incident Automation playbook and make the necessary modifications. \(This is an optional step. Follow this step only if you plan to customize or make specific changes to the flow\).
4.  Make the necessary modifications according to your requirement. \(This is an optional step. Follow this step only if you plan to customize or make specific changes to the flow\).
5.  Activate the playbook.
    -   Activate the main flow to use the playbook available with the base system.
    -   Activate the copied flow after making any modifications according to your requirements.

The following image shows a copy of the Child Security Incident Automation playbook. Review the steps below to get an understanding of the various actions in the playbook.

![Child Automation Flow:Overview](../image/cj-sir-child-automation-1.png)

This playbook is triggered when:

-   The parent security incident field isn’t empty.
-   The parent security incident is in Draft, Analysis, Contain, or Eradicate state.

![Child Automation playbook: Trigger](../image/cj-sir-child-automation-trigger.png)

The following steps walk you through the actions and tasks that are available in the Child Security Incident Automation playbook.

1.  When the playbook starts executing, in Step 1, if the security incident is in a Draft state, it’s updated and set to the Analysis state.

    ![Child Automation playbook: step 1](../image/cj-sir-child-automation-step1.png)

2.  In steps 2 and 3, affected users for the security incident are retrieved and rolled up to the parent security incident. Any duplicate users are eliminated.
3.  In steps 4 and 5, configuration items associated with the child security incident are retrieved and unique CIs are rolled up to the parent security incident.

    ![Child automation playbook: step 5](../image/cj-sir-child-automation-step4-5.png)

4.  In steps 6 and 7, observables associated with the child security incident are retrieved and unique observables are rolled up to the parent security incident.

    ![Child automation playbook: step 7](../image/cj-sir-child-automation-step6-7.png)

5.  In steps 8 and 9, automated worknotes are posted to the parent and child security incidents indicating that the affected users, configuration items, and observables have been rolled up from the child to the parent security incident.

**Parent Topic:**[Flow-based Playbooks](playbook-flow-based.md)

