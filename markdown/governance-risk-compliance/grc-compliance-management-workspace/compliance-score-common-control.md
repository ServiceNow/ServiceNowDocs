---
title: Impact of common control on compliance score calculation
description: Whenever an entity is associated to a common control and termed as a reliant entity, there is an impact on the compliance score of the entity on account of the common control test results.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Testing common control and implementing results on multiple reliant entities, Manage controls using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Impact of common control on compliance score calculation

Whenever an entity is associated to a common control and termed as a reliant entity, there is an impact on the compliance score of the entity on account of the common control test results.

All active, associated common controls contribute to the compliance score as any other control that exists.

Whenever a control changes its compliance status or weightage, the compliance score for the entities is recalculated. Similarly, in the case of a common control, the compliance score for reliant entities is recalculated as well.

All primary actions trigger recalculation of compliance score. When reliant entities are added or removed using the Add or Remove UI action in the Reliant entities related list as an upstream action, the compliance score for that particular reliant entity is recalculated. It is also recalculated when you retire a common control or convert a common control to standard control. Controls that are either compliant or non-compliant contribute to the compliance score calculation of an entity.

For more information, see the [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0716583](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0716583) article in the Now Support Knowledge Base.

**Note:** You must log in to Now Support to view the articles.

