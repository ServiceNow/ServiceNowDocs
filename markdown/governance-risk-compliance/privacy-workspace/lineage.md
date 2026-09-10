---
title: Manage data lineage
description: Data lineage is the visual representation of the relationships you define in a hierarchy. You can add new relationships directly from the lineage map in a processing map.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/privacy-workspace/lineage.html
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-08-19"
reading_time_minutes: 1
keywords: [data lineage, processing activity, hierarchy relationships]
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Manage data lineage

Data lineage is the visual representation of the relationships you define in a hierarchy. You can add new relationships directly from the lineage map in a processing map.

Every hierarchy relationship you create for a processing activity is rendered as a lineage map. An analyst can add relationships directly on the processing activity, and a business user can define relationships through a privacy impact assessment \(PIA\). The map lets you trace how data flows between vendors, applications, systems, and other processing activities from a source record. This helps you identify where privacy-related risks exist. For more on data lineages, see [View lineage map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/hierarchy-tab.md).

For a lineage map to be created, you must first create a hierarchy relationship. For steps, see [Add relationships to a hierarchy for a processing activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/create-a-data-lineage-for-a-processing-activity.md).

Use the following tasks to manage the lineage map for a processing activity:

-   [Edit a lineage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/editing-data-lineage.md)
-   [Delete a lineage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/delete-data-lineage.md)
-   [Update the maximum node level for the lineage map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/updating-node-level-for-lineage-map.md)

-   **[Edit a lineage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/editing-data-lineage.md)**  
Edit an existing lineage relationship to update the relationship type, description, or key relationship status of a connected node.
-   **[Delete a lineage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/delete-data-lineage.md)**  
Delete a lineage to remove a specific connection or node from the hierarchy of a processing activity.
-   **[Update the maximum node level for the lineage map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/updating-node-level-for-lineage-map.md)**  
Update the `sn_privacy.nodemap.maxLevel system` property to control how many node levels are visible on the lineage map.

**Parent Topic:**[Using Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/using-privacy-mgmt.md)

