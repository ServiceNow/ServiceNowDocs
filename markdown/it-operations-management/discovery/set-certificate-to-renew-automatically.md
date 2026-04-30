---
title: Set a certificate to renew automatically
description: Configure automatic certificate renewal to avoid service interruptions from expired certificates. Set the number of days before expiration when the system should automatically renew certificates.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-09-02"
reading_time_minutes: 1
breadcrumb: [Automated Certificate Renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Set a certificate to renew automatically

Configure automatic certificate renewal to avoid service interruptions from expired certificates. Set the number of days before expiration when the system should automatically renew certificates.

## Before you begin

Complete the following tasks to configure your system to renew your certificates automatically:

1.  [Configure your MID Server for automatic certificate renewal](configure-mid-server-automatic-cert-renewal.md)
2.  [Add the required applications and capabilities to your MID Server](add-req-apps-capabilities-to-mid-server.md)
3.  [Configure System Properties for automatic certificate renewal](config-sys-props-for-auto-cert-renewal.md)

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **Service Catalog** &gt; **Certificate Management** &gt; **Automated Flow** &gt; **Renew Certificate \(Automated\)**.

2.  Select the **Issued Certificate** that you would like to renew by selecting the search icon ![search icon](../../health-log-analytics-operator/image/icon-search-sow.png).

3.  Set the **Renew Automatically** field to **Yes**.

    **Note:** By selecting **Yes**, a new field appears called **How many days before expiry does this certificate need to be renewed?**.

4.  Select the number of days in the **How many days before expiry does this certificate need to be renewed?** field.

5.  Select **Submit**.


## Result

The certificate you chose is set to auto-renew the number of days before expiration that you request.

