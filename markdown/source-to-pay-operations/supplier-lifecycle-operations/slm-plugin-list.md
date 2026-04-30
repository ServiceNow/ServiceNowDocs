---
title: Supplier Lifecycle Operations plugin installation sequence
description: The following table provides the list of plugins for Supplier Lifecycle Operations, a high-level description of each plugin, and the dependencies that are required before installing each plugin.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Supplier Lifecycle Operations plugin installation sequence

The following table provides the list of plugins for Supplier Lifecycle Operations, a high-level description of each plugin, and the dependencies that are required before installing each plugin.

<table id="table_b5p_bs1_rwb"><thead><tr><th>

Plugin

</th><th>

Description

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

Supplier Common Architecture\[com.snc.sn\_slm\]

</td><td>

Provides a common architecture to track data objects related to a supplier used in both Supplier Lifecycle Operations and Supplier Collaboration Portal.

</td><td>

-   Finance Common Architecture \(com.sn\_fin\)
-   Service Delivery Common \(com.sn\_spend\_sdc\)
-   Document Management \(com.snc.platform\_document\_management\)
-   External User Registration \(com.snc.external\_user\_self\_registration\)
-   Common Vendor Core \(com.snc.sn\_vendor\_core\) and \(com.snc.vendor\_core\)

</td></tr><tr><td>

Supplier Lifecycle Operations\[com.snc.sn\_supplier\_mgmt\]

</td><td>

Onboard suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle.

</td><td>

-   Supplier Common Architecture \(com.snc.sn\_slm\)
-   Playbook Experience \(com.playbook\_experience\)
-   Employee Experience Foundation \(com.snc.sn\_ex\_emp\_fd\)
-   News Integration for Supplier Lifecycle Operations \(com.snc.sn\_supplier\_news\)
-   Map UI Component for threat and alert data feeds \(com.sn\_fam\_map\)

</td></tr><tr><td>

Supplier Collaboration Portal\[com.snc.sn\_supplier\_sp\]

</td><td>

Provides a single, one-stop experience for suppliers to get self-service, complete tasks and make requests into an organization.

</td><td>

-   Supplier Common Architecture \(com.snc.sn\_slm\)
-   Service Portal \(com.glide.service-portal\)
-   E-signature \(com.snc.esign\)
-   Employee Center \(com.snc.employee\_center\)

</td></tr><tr><td>

Craft.co Integration for Supplier Lifecycle Operations\[com.snc.sn\_supplier\_craft\]

</td><td>

Provides a pre-configured integration with Craft.co. Craft.co is a supplier intelligence platform that offers validated and comprehensive information about suppliers with which a company engages.

</td><td>

Supplier Lifecycle Operations \(com.snc.sn\_supplier\_mgmt\)

</td></tr><tr><td>

News Integration for Supplier Lifecycle Operations\[com.snc.sn\_supplier\_news\]

</td><td>

Retrieve recent news and other articles from preferred news channels. There is a pre-configured integration with Microsoft Bing available with this application.

</td><td>

None

</td></tr><tr><td>

Advanced Work Assignment for Supplier Lifecycle Operations\[com.snc.sn\_slm\_awa\]

</td><td>

Automatically assign supplier cases to agents based on availability and capacity.

</td><td>

-   Advanced Work Assignment \(com.glide.awa\)
-   Agent Chat \(com.glide.interaction.awa\)
-   Glide Virtual Agent \(com.glide.cs.chatbot\)
-   Supplier Lifecycle Operations \(com.snc.sn\_supplier\_mgmt\)

</td></tr></tbody>
</table>## Supplier Lifecycle Operations plugin installation sequence

To avoid incomplete demo data and other installation issues, you should install the plugins in the following sequence:

1.  Supplier Common Architecture \(com.snc.sn\_slm\)
2.  News Integration for Supplier Lifecycle Operations \(com.snc.sn\_supplier\_news\)
3.  Supplier Lifecycle Operations \(com.snc.sn\_supplier\_mgmt\)
4.  \(Optional\) Craft.co Integration for Supplier Lifecycle Operations \(com.snc.sn\_supplier\_craft\)
5.  \(Optional\) Advanced Work Assignment for Supplier Lifecycle Operations \(com.snc.sn\_slm\_awa\)

## Supplier Collaboration Portal plugin installation sequence

To avoid incomplete demo data and other installation issues, you should install the plugins in the following sequence:

1.  Supplier Common Architecture \(com.snc.sn\_slm\)
2.  Supplier Collaboration Portal \(com.snc.sn\_supplier\_sp\)

**Parent Topic:**[Install Supplier Lifecycle Operations](../task/install-supp-mgmt.md)

