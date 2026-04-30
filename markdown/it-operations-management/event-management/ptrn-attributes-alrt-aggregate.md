---
title: Specify and manage pattern identifier attributes for alert grouping
description: The Alert Aggregation Learner analyzes alerts and identifies patterns using a defined set of alert and configuration item \(CI\) attributes. By configuring these attributes as pattern identifiers, you can control which characteristics are used to group alerts. This customization creates meaningful alert groups, improving alert management and response times by reducing noise and enabling focus on critical issues.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Specify and manage pattern identifier attributes for alert grouping

The Alert Aggregation Learner analyzes alerts and identifies patterns using a defined set of alert and configuration item \(CI\) attributes. By configuring these attributes as pattern identifiers, you can control which characteristics are used to group alerts. This customization creates meaningful alert groups, improving alert management and response times by reducing noise and enabling focus on critical issues.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Event Management** &gt; **Administration** &gt; **Manage Pattern Identifier**.

2.  On the SA Alert Aggregation Pattern Attributes page, select **New** to create a new pattern identifier, or open an existing pattern identifier.

    The SA Alert Aggregation Pattern Attribute page opens.

3.  Select the Unlock Feature Identifier Attributes icon \(![Unlock Feature Identifier Attributes icon](../image/em-unlock-feature-identifier.png)\) and move attributes from the **Available** list to the **Selected** list.

    **Note:** Properties from CMDB CI via dot-walking are not populated.

    The **Configuration Item** attribute is automatically considered as an identifier and should not be added explicitly to the Feature Identifier Attributes section. The pattern is defined as a combination of the configuration item and your selected feature identifier attributes.

4.  Selecting the Lock Feature Identifier Attributes icon \(![Lock Feature Identifier Attributes icon](../image/em-lock-feature-identifier.png.png)\).

5.  Select **Submit** for a new pattern identifier or **Update** for an existing pattern identifier.

6.  Navigate back to the SA Alert Aggregation Pattern Attribute page by opening the pattern identifier.

7.  Activate the pattern identifier attributes by selecting **Deploy**.


## What to do next

-   Ensure a corresponding event rule exists: Verify that there is an event rule set up to assign or populate the newly defined pattern identifier attributes to the incoming alerts. Event rules define how attributes are assigned to alerts based on certain conditions.
-   Run the Service Analytics Attribute Populator for Historical Alerts job: After the new event rule is in place, this job is used to retroactively populate the pattern identifier attributes for existing alerts that were created before the new attributes were defined. It ensures that even past alerts \(historical alerts\) have the necessary attributes filled in for grouping them properly.

