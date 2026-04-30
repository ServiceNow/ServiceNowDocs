---
title: Configuring an instance with ADAM
description: The first install copies the ADAM files to your computer, registers requires components, and creates the application shortcuts.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Configuring an instance with ADAM

The first install copies the ADAM files to your computer, registers requires components, and creates the application shortcuts.

## Before you begin

Role required: admin

## About this task

By default, all of the application files are installed to `%systemroot%\ADAM`.

-   Windows Server 2003 R2 - ADAM can be installed using the **Control Panel &gt; Add and Remove Programs &gt; Optional Component Manager**.
-   Windows Server 2000 &amp; Windows XP - Downloaded [http://www.microsoft.com/downloads](http://www.microsoft.com/downloads) from Microsoft.

Create the first instance service which functions as the first directory service hosted by ADAM. Do one of the following:

## Procedure

-   Run adaminstall.exe from the ADAM folder.

-   Use the **Create an ADAM instance** shortcut from the **Start Menu &gt; Programs &gt; ADAM** folder.

    1.  Select the **A unique instance** install option.

        **Note:** You can use this option to install an instance replica on a second server to provide a fault tolerant system.

    2.  Complete the fields.

        |Field|Description|
        |-----|-----------|
        |Instance Name|used primarily to identify the Windows Service name and display name|
        |Ports|sets the port numbers to be used for LDAP and LDAPS Listeners. The default LDAP port is 389, LDAPS is 636. If these ports are in use on the server, the setup wizard selects new ports. Work with your network administrator to determine the best ports to use|
        |Application Directory Partition|creates an application directory partition. Not needed at this step, we recommend creating the new partition now. A good practice is to use the same distinguished name as your forest or domain, but replace the highest level domain with adam instead of com or local. For example, if your forest partition is **dc=myCompany,dc=com**, you could create the ADAM partition as **dc=myCompany,dc=adam**|
        |File Locations|selects the location\(s\) for the ADAM partition data.|
        |Service Account Selection|selects a service account that the instance runs as. For stand-alone services, you can use the default network service account. If you plan on using replicas, you need to use an account that has access to all ADAM instances.|
        |ADAM Administrators|the delegation on the ADAM directory that leverages Windows integrated authentication. This is how the initial access is granted for administration. Once the initial account is granted rights, this user or group delegates rights to other Windows users or ADAM users. You can select the default to only grant admin access to the current user, or grant access to a different user or group based on your needs.|
        |Import LDIF Files|the files to import. MS-UserProxy is the most important file to import, but it’s worth adding all available files since there is little overhead to the schema and you won’t have to worry about extending it later if your needs expand. Confirm the details and the wizard complete the configuration.|


**Related topics**  


[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

