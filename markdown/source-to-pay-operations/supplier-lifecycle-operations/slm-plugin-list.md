---
title: Application plugin installation sequence in Supplier Case Management
description: The following table provides the list of plugins for Supplier Case Management, a high-level description of each plugin, and the dependencies that are required before installing each plugin.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Application plugin installation sequence in Supplier Case Management

The following table provides the list of plugins for Supplier Case Management, a high-level description of each plugin, and the dependencies that are required before installing each plugin.

**Important:** Before installing a plugin listed in the Plugin name column, ensure that you install all corresponding dependencies listed in the Plugin dependencies column from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

<table id="table_b5p_bs1_rwb"><thead><tr><th>

Sequence

</th><th>

Plugin name

</th><th>

Description

</th><th>

Plugin dependencies

</th></tr></thead><tbody><tr><td>

1

</td><td>

Supplier Common Architecture\[com.snc.sn\_slm\]

</td><td>

Provides a common architecture to track data objects related to a supplier used in both Supplier Case Management and Supplier Collaboration Portal.

</td><td>

-   Finance Common Architecture \(com.sn\_fin\)
-   Service Delivery Common \(com.sn\_spend\_sdc\)
-   External User Registration \(com.snc.external\_user\_self\_registration\)
-   Common Vendor Core \(com.snc.sn\_vendor\_core\) and \(com.snc.vendor\_core\)

</td></tr><tr><td>

2

</td><td>

Supplier Case Management\[com.snc.sn\_supplier\_mgmt\]

Plugin scope name: sn\_supplier

</td><td>

Onboard suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle.

</td><td>

-   Supplier Common Architecture \(com.snc.sn\_slm\)
-   Source-to-Pay Workspace \(com.sn\_spend\_workspace\)

</td></tr><tr><td>

3

</td><td>

Supplier Collaboration Portal\[com.snc.sn\_supplier\_sp\]

</td><td>

Provides a single, one-stop experience for suppliers to get self-service, complete tasks and make requests into an organization.

</td><td>

-   Supplier Common Architecture \(com.snc.sn\_slm\)
-   Service Portal \(com.glide.service-portal\)
-   E-signature \(com.snc.esign\)
-   Employee Center \(com.snc.employee\_center\)

</td></tr><tr><td>

4

</td><td>

Supplier Operations\[com.snc.sn\_so\]

</td><td>

Provides advanced case management capabilities to handle key supplier lifecycle events such as onboarding, offboarding, and ongoing operations.

</td><td>

Document Management \(com.snc.platform\_document\_management\)

</td></tr><tr><td>

5

</td><td>

Craft.co Integration for Supplier Lifecycle Operations\[com.snc.sn\_supplier\_craft\]

</td><td>

Provides pre-configured integration with Craft.co. Craft.co is a supplier intelligence platform that offers validated and comprehensive information about suppliers with which a company engages.

</td><td>

Supplier Operations\(com.snc.sn\_so\)

</td></tr><tr><td>

6

</td><td>

News Integration for Supplier Lifecycle Operations\[com.snc.sn\_supplier\_news\]

</td><td>

Retrieve recent news and other articles from preferred news channels. There is a pre-configured integration with Microsoft Bing available with this application.

</td><td>

Supplier Operations\(com.snc.sn\_so\)

</td></tr><tr><td>

7

</td><td>

SLO Connector for Relish Data Assure\[x\_reliq\_slo\_connec\]

</td><td>

Provides pre-configured integration with Relish. Relish is a supplier intelligence platform that helps in validating supplier data with confidence.

</td><td>

-   Source-to-pay integration framework \(sn\_spend\_intg\)
-   Relish Data Assure \(x\_reliq\_relish\_dat\)

</td></tr><tr><td>

8

</td><td>

Advanced Work Assignment for Supplier Lifecycle Operations\[com.snc.sn\_slm\_awa\]

</td><td>

Automatically assign supplier cases to agents based on availability and capacity.

</td><td>

-   Advanced Work Assignment \(com.glide.awa\)
-   Agent Chat \(com.glide.interaction.awa\)
-   Glide Virtual Agent \(com.glide.cs.chatbot\)
-   Supplier Case Management \(com.snc.sn\_supplier\_mgmt\)

</td></tr></tbody>
</table>## Supplier Case Management plugin installation sequence

To avoid incomplete demo data and other installation issues, you should install the plugins in the following sequence:

1.  Supplier Common Architecture \(com.snc.sn\_slm\)
2.  News Integration for Supplier Lifecycle Operations \(com.snc.sn\_supplier\_news\)
3.  Supplier Case Management \(com.snc.sn\_supplier\_mgmt\)
4.  \(Optional\) Craft.co Integration for Supplier Lifecycle Operations \(com.snc.sn\_supplier\_craft\)
5.  \(Optional\) SLO Connector for Relish Data Assure \(x\_reliq\_slo\_connec\)
6.  \(Optional\) Advanced Work Assignment for Supplier Lifecycle Operations \(com.snc.sn\_slm\_awa\)

**Parent Topic:**[Install Supplier Case Management](../task/install-supp-mgmt.md)

**Related topics**  


[Components installed with Supplier Case Management](installed-with-supp-mgmt.md)

[Explicit Roles in Supplier Case Management](../concept/slo-explicit-roles-plugin.md)

