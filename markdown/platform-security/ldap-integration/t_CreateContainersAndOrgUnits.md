---
title: Create containers and organizational units for ADAM
description: Logically group objects stored in ADAM into containers and organizational units \(OU\) just as they would be in Active Directory.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Create containers and organizational units for ADAM

Logically group objects stored in ADAM into containers and organizational units \(OU\) just as they would be in Active Directory.

## Before you begin

Role required: admin

## Procedure

1.  Right-click the root partition and navigate to **New** &gt; **Object** &gt; **organizationalUnit**.

    **Note:** You can also view the list of other objects that are available. This list varies based on the schema extensions installed when you imported the LDF files.

2.  When prompted for a value, enter the name of the OU such as `Users`.

    The screen displays a **More Attributes** button.

3.  Use the button to assign values to additional attributes.

    For the OUs and containers, no additional values are needed.

    After creating the OUs, the new OUs are listed as a child of the root object.


**Related topics**  


[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

