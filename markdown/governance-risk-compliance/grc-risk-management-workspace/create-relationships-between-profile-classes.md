---
title: Create relationships between entity classes using the GRC: Workbench
description: Managers create relationships between entity classes using the GRC: Workbench to build out the dependency map and better understand how entities relate to one another.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-risk-management-workspace/create-relationships-between-profile-classes.html
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use entity and risk dependencies using the GRC: Workbench, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create relationships between entity classes using the GRC: Workbench

Managers create relationships between entity classes using the GRC: Workbench to build out the dependency map and better understand how entities relate to one another.

## Before you begin

Role required: sn\_grc.manager

[Create profile classes using the GRC: Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-risk-management-workspace/create-profile-class-using-grc-workbench.md), before creating relationships between entity classes.

Entity classes can roll up to each other, leading to the development of the dependency model.

## Procedure

1.  Navigate to `https://myCompany.service-now.com/$grc_workbench.do`.

2.  Select the **Model Setup** tab at the top, and select the **Dependency Model** tab.

3.  If needed, create entity classes.

4.  Do one of the following actions.

<table id="choicetable_klb_sq3_4w"><tbody><tr><td id="d53734e98">

**If there are no relationships between entity classes**

</td><td>

Drag an entity class from the left to the center and drop it.

</td></tr><tr><td id="d53734e107">

**If there are relationships between entity classes**

</td><td>

Drag additional entity classes from the list on the left and drop them on the top or bottom of any entity class in the tree. **Note:** Dragging to the top of an entity class makes the target entity class roll up to the class that is dropped. Dragging to the bottom of an entity class makes the class that is being dropped roll up to the target class.

</td></tr></tbody>
</table>    **Note:** As long as you remain on the GRC: Workbench, click **Undo** after creating a relationship between entity classes to roll back the change. Leaving the GRC: Workbench causes the undo history to be lost.


## What to do next

After modeling out entities, define the risks in your organization:

-   [Generate a risk from a risk framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-risk-management-workspace/t_GenerateRiskFromStatement.md)
-   [Generate a risk from a risk statement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-risk-management-workspace/t_GenRiskFromRiskFrameProfile.md)
-   [Associate a risk framework or risk statement with an entity type to generate risks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-risk-management-workspace/t_GenerateRiskFromFramework.md)

After generating risks, [Relate risks to each other](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-risk-management-workspace/relate-risks-to-each-other.md).

**Parent Topic:**[Use entity and risk dependencies using the GRC: Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-risk-management-workspace/grc-workbench.md)

