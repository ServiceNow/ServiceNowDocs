---
title: Restrict allowed Java packages \[Updated in Security Center 1.3\]
description: Configuring these properties protect from dangerous APIs being exposed to the scripting engine.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Restrict allowed Java packages \[Updated in Security Center 1.3\]

Configuring these properties protect from dangerous APIs being exposed to the scripting engine.

Configure the system tables and install the recommended plugin accordingly.

If the **sys\_whitelist\_member** and **sys\_whitelist\_package** table are not empty values, then dangerous APIs may be exposed to the scripting engine. Entries correspond to the Java namespace that have not been approved by ServiceNow security teams.

Install the Packages call removal tool. See [Packages call removal tool](sc-packages-call-removal-tool.md) for details.

Contact Customer Service and Support to edit these tables.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table, plugin name

</td><td>

Tables: -   **sys\_whitelist\_member**
-   **sys\_whitelist\_package**

Plugin: com.glide.script.packages\_call\_removal

</td></tr><tr><td>

Configuration type

</td><td>

Tabular Configuration, Plugins

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Purpose

</td><td>

Protect from dangerous APIs being exposed to the scripting engine.

</td></tr><tr><td>

Recommended value

</td><td>

Empty

</td></tr><tr><td>

Default value

</td><td>

None. This is a table configuration and not a Glide Property, so there is no default value.

</td></tr><tr><td>

Configuration type

</td><td>

table list, plugin

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Dangerous APIs may be exposed to the scripting engine. These supported APIs will likely introduce instability and insecurity within the instance.

</td></tr><tr><td>

Security risk rating

</td><td>

8.2

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

-   **[Packages call removal tool](sc-packages-call-removal-tool.md)**  
Activate and run the Packages Call Removal Tool \(**com.glide.script.packages\_call\_removal**\) plugin, and then consider whether each of the proposed changes should be completed or rejected.

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

