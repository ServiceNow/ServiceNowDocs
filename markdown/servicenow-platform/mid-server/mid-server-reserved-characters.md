---
title: MID Server protected records and reserved characters
description: Some MID Server records cannot be altered. Certain special characters are pre-defined in XML and cannot be used in passwords.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/mid-server-reserved-characters.html
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server protected records and reserved characters

Some MID Server records cannot be altered. Certain special characters are pre-defined in XML and cannot be used in passwords.

<table id="table_dlr_pv4_nhb"><tbody><tr><td>

![Links to each of the MID Server sections](../image/MIDRefIconBar.png)

</td></tr></tbody>
</table>## MID Server Records that cannot be altered

These records cannot be modified or deleted.

<table id="table_ktl_kbk_chb"><thead><tr><th>

Table

</th><th>

Record

</th></tr></thead><tbody><tr><td>

Public Page \[sys\_public\]

</td><td>

InstanceInfo

</td></tr><tr><td>

Scripted Web Service \[sys\_web\_service\]

</td><td>

-   InstanceInfo
-   GetMIDInfo
-   MIDAssignedPackages
-   MIDFieldForFileProvider
-   MIDFileSyncSnapshot
-   MIDServerCheck
-   MIDServerFileProvider

</td></tr></tbody>
</table>## Using special characters in an XML file

The XML specification defines five predefined entities that represent special characters, and requires that all XML processors honor them. If these characters are used in a password, you will experience unexpected results.

The following characters represent the five pre-defined entities:

-   "
-   &amp;
-   '
-   &lt;
-   &gt;

If you use the pre-defined entity characters in an XML file, such as the MID Server configuration file, you need to encode them. To encode pre-defined entities into an XML document:

-   replace **"** with **&amp;quot;**
-   replace **&amp;** with **&amp;amp;**
-   replace **'** with **&amp;apos;**
-   replace **&lt;** with **&amp;lt;**
-   replace **&gt;** with **&amp;gt;**

For example, to specify the password as `test&` in the MID Server config.xml file:

```
<parameter encrypt="true" name="mid.instance.password" value="test&amp;"/>
```

**Parent Topic:**[MID Server reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements]()

[MID Server upgrades]()

[Resolving MID Server issues]()

[MID Server dashboard]()

[MID Server properties]()

[MID Server parameters]()

[MID Server Configuration Parameter settings and priority]()

[MID Server File Cleaner]()

[MID Server privileged commands]()

[MIDSystem methods]()

[Manually start, stop, and restart a MID Server]()

[MID Server heartbeat]()

[Set the MID Server JVM memory size]()

[Pause the MID Server]()

