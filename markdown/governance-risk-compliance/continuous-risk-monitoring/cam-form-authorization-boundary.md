---
title: Fields on the Authorization Boundary form
description: An authorization boundary defines the scope of a particular system that can be continuously managed and monitored using the CAM application.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Fields on the Authorization Boundary form

An authorization boundary defines the scope of a particular system that can be continuously managed and monitored using the CAM application.

<table id="table_epy_qrq_f5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique and descriptive name for this boundary.

</td></tr><tr><td>

Description

</td><td>

A description for this boundary.

</td></tr><tr><td>

Operational status

</td><td>

Option to set the status of the boundary manually or auto-populate. The operational status:-   Under development
-   Reauthorize

The system automatically updates the operational status from **Operational** to **Reauthorize** based on:

    -   When the **Next Authorization Date** selected in the authorization package is within the number of days given in the CAM system property.
    -   **sn\_irm\_cont\_auth.days\_before\_boundary\_reauthorizes** configured in the system properties. The default value is 180 days. To update the value navigate to **All** &gt; **sys\_properties.LIST**. Enter **sn\_irm\_cont\_auth.days\_before\_boundary\_reauthorizes** in the filter search bar. Open the record and update the **Value**.
-   Operational

Auto-populated when the active Authorization Packages get authorized and moves from **Authorize** to **Monitor** state.

-   Decommissioned

</td></tr><tr><td>

Mission critical

</td><td>

Option to set the boundary as mission-critical.

</td></tr><tr><td>

System owner

</td><td>

The individual responsible for procuring, developing, integrating, modifying, operating, and maintaining an information system.

</td></tr><tr><td>

Information owners

</td><td>

The individuals responsible for statutory, management, and operational authority.

</td></tr><tr><td>

System users

</td><td>

Responsible for performing the actual work on the system.

</td></tr><tr><td>

Diagrams

</td><td>

If needed, or if you don’t have a Configuration Management Database \(CMDB\), add data flow, network, and boundary diagrams.

</td></tr><tr><td>

Boundary type

</td><td>

Option to set the type of the boundary. The types are as follows.-   **GSS**: General Support System \(GSS\) is a collection of connected IT resources managed together, including hardware, software, data, applications, and people.
-   **Major app**: An application that handles sensitive information and requires special security oversight due to the high risk if the data is lost, misused, or accessed without authorization.
-   **Minor app**: An application that needs security protection but has lower risk than a major application. Minor applications are typically included as part of a general support system.
-   **Sub system**: A major component of a larger information system that performs specific functions.
-   **Closed system**: A self-contained system that operates only within your organization and doesn’t connect to external systems.

</td></tr><tr><td>

Classification

</td><td>

Option to set the classification of the boundary. The types are as follows.-   **Confidential**: Lowest level of classified information that requires protection from unauthorized disclosure.
-   **Secret**: Mid-level classified information that requires substantial protection and restricted access.
-   **Top secret**: Highest level of classified information that requires maximum protection and stringent access controls.
-   **Sensitive but unclassified**: Non-classified information that requires protection due to its sensitive nature such as personal, proprietary, or business-sensitive data\).
-   **CUI**: Controlled unclassified information \(CUI\) requires specific safeguarding and handling per federal regulations or policies.

</td></tr></tbody>
</table>**Parent Topic:**[CAM reference](../concept/reference-grc-cam.md)

