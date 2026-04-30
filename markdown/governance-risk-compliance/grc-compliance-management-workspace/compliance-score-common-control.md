---
title: Impact of common control on compliance score calculation
description: Whenever an entity is associated to a common control and termed as a reliant entity, there is an impact on the compliance score of the entity on account of the common control test results.
locale: en-US
release: zurich
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Test common control and implement results, Manage controls, Use, GRC Compliance Workspace, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Impact of common control on compliance score calculation

Whenever an entity is associated to a common control and termed as a reliant entity, there is an impact on the compliance score of the entity on account of the common control test results.

All active, associated common controls contribute to the compliance score as any other control that exists.

Whenever a control changes its compliance status or weightage, the compliance score for the entities is recalculated. Similarly, in the case of a common control, the compliance score for reliant entities is recalculated as well.

All primary actions trigger recalculation of compliance score. When reliant entities are added or removed using the Add or Remove UI action in the Reliant entities related list as an upstream action, the compliance score for that particular reliant entity is recalculated. It is also recalculated when you retire a common control or convert a common control to standard control. Controls that are either compliant or non-compliant contribute to the compliance score calculation of an entity.

For more information, see the [Compliance score calculations in GRC \[KB1222566\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1222566) article in the Now Support Knowledge Base.

**Note:** You must log in to Now Support to view the articles.

