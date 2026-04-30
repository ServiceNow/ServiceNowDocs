---
title: Set up the ADAM console
description: Set up the ADAM console. Even though there are many similarities between ADAM and Active Directory, the administration can be very different since there is no Users and Computers management console.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Set up the ADAM console

Set up the ADAM console. Even though there are many similarities between ADAM and Active Directory, the administration can be very different since there is no **Users and Computers** management console.

## Before you begin

Role required: admin

## About this task

Most of the general administration is performed using the ADAM ADSI MMC console available from the **ADAM** start menu. The first time you run the ADAM ADSI console, you must connect to the partition you created.

## Procedure

1.  Right-click the **ADAM ADSI Edit** item in the left frame.

2.  Give the new connection a name and update the server name and port fields with the information used when you created the instance.

3.  Select **distinguished name** or **naming context** and specify the distinguished name of the application partition you created earlier.

    You can connect to the Configuration and Schema partitions for advanced configuration options.

    You should now be able to see into the partition and the default containers for LostAndFound, NTDS Quotas, and Roles. The Roles container has not been configured yet.


**Related topics**  


[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

