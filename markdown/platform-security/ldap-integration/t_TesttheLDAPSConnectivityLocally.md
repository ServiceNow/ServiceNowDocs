---
title: Test the LDAPS connectivity locally
description: Test the LDAPS connectivity after installing the internal and third party certificates when you configure Microsoft Active Directory for SSL access.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Active Directory for secure LDAPS communication, LDAP integration, Authentication, Access Management]
---

# Test the LDAPS connectivity locally

Test the LDAPS connectivity after installing the internal and third party certificates when you configure Microsoft Active Directory for SSL access.

## Before you begin

Role required: admin

## Procedure

1.  Ensure that Windows Support Tools are installed on the domain controller \(DC\).

    The Support Tools setup \(suptools.msi\) can be found in the `\Support\Tools` directory on your Windows Server CD.

2.  Navigate to **Start** &gt; **All Programs** &gt; **Windows Support Tools** &gt; **Command Prompt**.

    On the command line, enter `ldp` to start the tool.

3.  From the ldp window, select **Connection** &gt; **Connect** and supply the local FQDN and port number \(636\).

    Also select the SSL.

    If successful, a window displays and lists information related to the Active Directory SSL connection. If the connection is unsuccessful, try restarting your system and repeat this procedure.


