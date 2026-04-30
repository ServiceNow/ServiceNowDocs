---
title: Run IP-Based Certificate Discovery
description: Enable the Transfer Layer Security \(TLS\) port probe \[tls\_ssl\_certs\] and scan for certificates on an IP address or multiple IP addresses.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, Discovery, ITOM Visibility, IT Operations Management]
---

# Run IP-Based Certificate Discovery

Enable the Transfer Layer Security \(TLS\) port probe \[tls\_ssl\_certs\] and scan for certificates on an IP address or multiple IP addresses.

## Before you begin

Know the IP address, range of IP addresses, or list of IP addresses you want to perform Certificate Discovery on.

Role required: Certificate administrator, discovery\_admin, or admin

## Procedure

1.  Activate the TLS port probe \[tls\_ssl\_certs\].

    1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Port Probes**.

    2.  Open **tls\_ssl\_certs**.

    3.  To enable the probe, select the **Active** check box.

        By default, the check box for any new installation is cleared.

    4.  Confirm the **Triggered by services** has the services you need.

        By default, the following services trigger the tls\_ssl\_certs probe: HTTPS, tomcat-ssl, IBM Websphere SSL, Idaps, IMAPS, pop3s, ftps-data, ftps, smtp, pop3, imap, Idap, ftp, submission.

    5.  Select **Update**.

2.  Create an IP-Based Certificate Discovery Schedule.

    1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

    2.  Select **New**.

    3.  Fill out each text field with its corresponding value.

        For more information on the fields and values, see [IP-Based Discovery Schedule Form Table](../reference/ip-based-cert-discovery-schedule-table.md).

    4.  Select and hold \(or right-click\) above **Discovery Schedule** and select **Save**.

        By selecting **Save**, additional configuration options are available.

    5.  Select the **Use SNMP** text field.

    6.  In the new tabs that appear, select **Discovery IP Ranges**.

    7.  Select **New**.

    8.  Fill each field with its corresponding value.

        For more information on the fields and values, see [Setting Your IP Addresses Form and Fields Table](../reference/setting-up-your-ip-addresses.md).

    9.  Select **Submit**.

        The port **tls\_ssl\_certs** will look for Certificates available inside your selected IPs at the next time interval \(daily, weekly, monthly, etc.\).

3.  Create an IP-Based Certificate **Quick Discovery** for immediate discovery \(optional\).

    1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

    2.  Select **Quick Discovery**.

    3.  Enter your Target IP into the **Target IP** field.

        **Warning:** Make sure that your IP address is accessible to the MID Server you’re using. If it doesn’t, you have to set [Credential aliases for Discovery](https://www.servicenow.com/docs/access?context=discovery-credential-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

    4.  Select **OK**.


## Result

The probe tls\_ssl\_certs searches for Certificates inside your selected IP immediately, and reports the certificates it finds.

