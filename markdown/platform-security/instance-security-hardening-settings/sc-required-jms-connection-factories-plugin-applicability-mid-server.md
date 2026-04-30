---
title: Required jms connection factories \[New in Security Center 1.3 and updated in 1.5 and 2.0\]
description: The mid.property.jms.command.allowed\_factory\_names property controls the Java Messaging Service \(JMS\) connection factories that the MID Server can use.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Required jms connection factories \[New in Security Center 1.3 and updated in 1.5 and 2.0\]

The **mid.property.jms.command.allowed\_factory\_names** property controls the Java Messaging Service \(JMS\) connection factories that the MID Server can use.

It is intended for a few select factories needed by plugins for JMS activity or action. Including additional factories could be a step in a chain of attack for vulnerabilities such as JDNI insertion that rely on capabilities an attacker can leverage in allowed factories. To prevent the possibility of any leveraged vulnerability, do not include factories beyond the necessary defaults.

To remediate this security risk review the list of names provided to the mid property, **mid.property.jms.command.allowed\_factory\_names**. Ensure any additional Java factory names beyond the default of connectionFactory, queueConnectionFactory, and topicConnectionFactory are necessary.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**mid.property.jms.command.allowed\_factory\_names**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Default value

</td><td>

**connectionFactory**, **queueConnectionFactory**, **topicConnectionFactory**

</td></tr><tr><td>

Recommended value

</td><td>

**connectionFactory**, **queueConnectionFactory**, **topicConnectionFactory**

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.1
-   CVSS score: Medium
-   Security risk details: If the MID Server \(**com.glideapp.agent**\) plugin is active, review the list of names provided to the mid property **mid.property.jms.command.allowed\_factory\_names**. Ensure any additional factory names beyond the default of connectionFactory, queueConnectionFactory, and topicConnectionFactory are necessary.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

