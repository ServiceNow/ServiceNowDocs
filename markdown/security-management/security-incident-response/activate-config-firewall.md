---
title: Activate and configure the Palo Alto Networks Firewall Integration
description: The Integration Configuration feature allows you to quickly activate and set up third-party security integrations, including Palo Alto Networks - Firewall. Before you can use the Palo Alto Networks - Firewall, you must download it from the ServiceNow Store.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Palo Alto Networks - Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Activate and configure the Palo Alto Networks Firewall Integration

The Integration Configuration feature allows you to quickly activate and set up third-party security integrations, including Palo Alto Networks - Firewall. Before you can use the Palo Alto Networks - Firewall, you must download it from the ServiceNow Store.

## Before you begin

Role required: sn\_si\_admin

## Procedure

1.  Before activating and configuring the integration, access the Palo Alto Networks Firewall dashboard.

    Take note of the names of the IP Dynamic List, URL Dynamic List, or Domain Dynamic List you are using for firewall blocking.

2.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

3.  When the installation is complete, navigate to **Security Operations** &gt; **Integration Configuration**.

    The available security integrations appear as a series of cards.

4.  In the Palo Alto Networks Firewall card, click **Configure**.

    ![Palo Alto Networks Firewall configuration](../image/config-screen.png)

5.  Click **Configure firewalls**.

6.  In the Firewall Configurations screen, click **New**.

7.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Firewalls|Click the lock icon and select the firewall to be configured.|
    |Firewall Version|Select the Palo Alto Networks Firewall version.**PAN-OS-7.1** is the recommended version. Selecting earlier versions may return inconsistent results.|
    |Username|Enter the username to use when connecting to the firewall via REST endpoints.|
    |Password|Enter the password for the connecting user.|
    |IP Dynamic List|Enter the name of the External Dynamic List or Dynamic Block List you use for IP addresses.|
    |URL Dynamic List|Enter the name of the External Dynamic List or Dynamic Block List you use for URLs.|
    |Domain Dynamic List|Enter the name of the External Dynamic List or Dynamic Block List you use for domains.|

8.  Click **Submit**.


