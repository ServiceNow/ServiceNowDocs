---
title: Configuring Pattern Designer and related applications
description: Install the latest available versions of the ServiceNow applications to use the latest discovery patterns.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Configuring Pattern Designer and related applications

Install the latest available versions of the ServiceNow applications to use the latest discovery patterns.

The Pattern Designer \(com.snc.pattern.designer\) application provides the UI for creating or customizing discovery patterns. Pattern Designer is automatically installed with Discovery or Service Mapping. The patterns themselves are released using dedicated pattern applications.

The following user roles have access to Pattern Designer and can perform various actions. Note that customizing patterns requires basic knowledge of programming.

<table id="table_m5h_h4v_2hc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PD user

</td><td>

Has read-only access to **Discovery Pattern Log**.

</td></tr><tr><td>

PD admin

</td><td>

Can view, create, edit, and publish patterns.

</td></tr><tr><td>

PDE viewer

</td><td>

Starting with Pattern Designer Enhancements version 3.9.0, users can view **Command Validation Tasks**, **Command Validation Tasks Results**, and **Command List**. The pde\_viewer can view the **Command Validation Tool** modules and related tables, but doesn't have permissions to modify or edit them.

The pde\_viewer role can view the following tables only:

-   Command List \[pd\_command\_list\]
-   Command Validation Task \[pd\_command\_validation\]
-   Command Validation Task Results \[pd\_command\_validation\_results\]
-   Pattern Shared Library Mapping \[pd\_pattern\_to\_shared\_library\_mapping\]
-   Temporary Variable Mappings \[pd\_temp\_variable\_value\_mapping\]

</td></tr><tr><td>

PD MID

</td><td>

Not assigned to a user directly but to the MID Server record or the user under which the MID Server runs. The role enables the MID Server to interpret and run pattern-based probes.

</td></tr></tbody>
</table>ServiceNow releases all discovery patterns using the following applications:

-   **Discovery and Service Mapping Patterns \(sn\_itom\_pattern\)**

    This application provides the latest versions of discovery patterns the original version of which ServiceNow released on ServiceNow Store.

-   **Visibility Content \(sn\_pattern\_design\)**

    This application supplies the updated version of the patterns that were part of the family releases up until Tokyo.


You can install the latest available versions of the pattern applications from the ServiceNow Store. Alternatively, you can install these applications as plugins on your ServiceNow instance.

-   **[Check which plugin contains a required pattern](../task/check-pattern-availability.md)**  
Since ServiceNow releases discovery patterns using two different plugins, you may need to check which plugin to install or upgrade.
-   **[Install Discovery and Service Mapping Patterns](../task/install-discovery-service-mapping-patterns.md)**  
You can install the Discovery and Service Mapping Patterns application \(sn\_itom\_pattern\) if you have the admin role.
-   **[Install Visibility Content](../task/install-itom-visibility-global-content.md)**  
You can install the Visibility Content application \(sn\_pattern\_design\) if you have the admin role.
-   **[Password2 encryption for patterns](../concept/password2-encryption-patterns.md)**  
The Password \(two-way encrypted\) field type is used to encrypt and decrypt data. The field type works in accordance with NIST 800-57 guidelines and provides FIPS 140-2-L3 protection.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

**Previous topic:**[OpenStack resource discovery](openstack-discovery.md)

**Next topic:**[Check which plugin contains a required pattern](../task/check-pattern-availability.md)

