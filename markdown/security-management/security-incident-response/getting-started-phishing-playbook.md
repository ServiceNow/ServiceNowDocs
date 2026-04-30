---
title: Activate a Security Incident Response flow
description: Security administrators and flow designers can use the Security Incident Response flows to automate the process of resolving security incidents in the organization.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Activate a Security Incident Response flow

Security administrators and flow designers can use the Security Incident Response flows to automate the process of resolving security incidents in the organization.

## Before you begin

Role required: sn\_si.admin, action\_designer, and flow\_designer

## About this task

The flows provided with the base system are in an inactive state. Activate these flows before you use them.

## Procedure

1.  [Download and install](../reference/download-app-first-time.md) the Security Operations Spoke application.

    This Spoke application provides security operations actions that you can use while defining Security Incident Response flows.

2.  Navigate to **Flow Designer** &gt; **Designer** and search for the Security Operations Spoke application to view the Security Incident related flows.

    ![Security Incident Management Spokes](../image/cj-sir-flow-phishing.png)Notice that the flows have a published status and are inactive.

3.  For example, if you want to activate the Automated Malware Playbook flow, click the **Security Incident - Automated Phishing Playbook - Template V1** link to view the flow.

    ![Automated Phishing Playbook Template](../image/cj-sir-flow-auto.png)

    **Note:** You cannot edit the flows provided with the base system as they are read-only flows. You can use these flows as they are or make a copy and modify them as required.

4.  Click **Activate** to activate the flow.


## Result

The Automated Phishing Playbook flow is active and ready to use.

