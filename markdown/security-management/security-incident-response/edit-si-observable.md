---
title: Edit a security incident observable list
description: You can edit which observables in the list associated with a security incident to display.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage observables, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Edit a security incident observable list

You can edit which observables in the list associated with a security incident to display.

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  Navigate to **Security Incident**.

2.  Choose an incident.

3.  Click **Security Incident Observables** related list tab.

4.  Click **Edit**.

5.  Add or remove observables from the list.

    Create a filter for long lists.

    ![Edit observables list example](../image/EditObservableList.png)

6.  Click **Save**.

    **Note:** When you add an observable to the security incident, the system checks for any other configuration items or users associated with it. The **Related Configuration Items** and **Related Users** related list tabs are updated accordingly. Also, if the Threat Intelligence plugin is activated, and you have at least one[Security Incident Response integrations](../concept/sir_integrations.md) integration implementation activated, the [Security Operations Integration - Threat Lookup capability](../../security-operations-common/concept/sec-ops-threat-lookups-capability.md) executes one or more workflows, and threat security lookups are performed on the observables you added. The results appear in the **Threat Lookup Results** tab.


**Related topics**  


[Add multiple security incident observables](add-multiple-si-observables.md)

[Create a security incident observable](create-si-observable.md)

