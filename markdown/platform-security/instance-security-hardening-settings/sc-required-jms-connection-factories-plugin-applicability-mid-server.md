---
title: Required JMS connection factories
description: The mid.property.jms.command.allowed\_factory\_names property controls the Java Messaging Service \(JMS\) connection factories that the MID Server can use.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Required JMS connection factories

The **mid.property.jms.command.allowed\_factory\_names** property controls the Java Messaging Service \(JMS\) connection factories that the MID Server can use.

This property controls the Java Messaging Service \(JMS\) connection factories that the MID Server can use. It is intended for a few select factories needed by plugins for JMS activity or action. Including additional factories could be a step in a chain of attack for vulnerabilities such as JNDI insertion that rely on capabilities an attacker can leverage in allowed factories. To prevent the possibility of any leveraged vulnerability, do not include factories beyond the necessary defaults.

Review the list of names provided to the mid property **mid.property.jms.command.allowed\_factory\_names**. Ensure any additional factory names beyond the default of `connectionFactory, queueConnectionFactory, topicConnectionFactory` are necessary.

See the following documentation for updating this and other mid server properties: [MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

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
-   Security risk details: Expanding the set of Java Messaging Service \(JMS\) connection factories beyond the necessary defaults introduces a significant risk because it increases the attack surface for exploitation techniques such as JNDI injection. Allowing additional factories can enable attackers to leverage insecure configurations or vulnerabilities in messaging components as part of a broader attack chain, potentially leading to remote code execution or system compromise. Restricting factories to only those required by core functionality is essential to maintain a secure posture.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

