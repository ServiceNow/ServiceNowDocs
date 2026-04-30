---
title: Setting up VRM third-party hierarchies and engagements
description: Create third-party hierarchies by defining the parent-child relationships between the parent third party and all of their subsidiaries. You do this task because some organizations work with third parties that have subsidiaries \(or subsidiaries of subsidiaries\) that can pose a potential risk to your business. You can perform assessments at each subsidiary organization and roll up the results to calculate an overall risk score for the parent third party.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Work in the VRM classic UI, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Setting up VRM third-party hierarchies and engagements

Create third-party hierarchies by defining the parent-child relationships between the parent third party and all of their subsidiaries. You do this task because some organizations work with third parties that have subsidiaries \(or subsidiaries of subsidiaries\) that can pose a potential risk to your business. You can perform assessments at each subsidiary organization and roll up the results to calculate an overall risk score for the parent third party.

## Third-party hierarchy

In this example, parent organization Acme has two subsidiaries and Acme NA has two subsidiaries. In this hierarchy, you perform risk assessments for the parent third party and all subsidiaries and calculate risk scores for each entity. You can then aggregate \(roll up\) the risk scores to calculate the risk score for Acme.

![Third-party hierarchy.](../image/vendor-hierarchy.png)

## Third-party hierarchy with subsidiaries and engagements

Engagements represent products or services provided to the parent organization—either directly or from subsidiaries—that you can assess for risk. In the case where a subsidiary provides engagements, the risk scores assigned to the engagements are rolled up to calculate the risk score of the subsidiary, which in turn roll up to the parent organization.

In this example, subsidiary Acme US has three engagements. As in the previous example, risk is assessed for the parent, all of its subsidiaries, and all of their engagements. The risk scores are then rolled up to calculate the risk score for the parent.

![A third-party hierarchy with subsidiaries and engagements.](../image/vendor-hierarchy-engagement.png)

See [Define a VRM engagement](../task/tprm-ws-engagement-request.md).

## Overview: Setting up a third-party hierarchy

**Note:** The setup procedures in this section apply only if you work with multi-layered third parties; that is, third parties that operate subsidiaries. They also guide you through the setup of engagements offered by subsidiaries. If these are not the types of third parties you do business with, and you do not want to set up third-party hierarchies, these procedures are optional.

<table id="table_nsl_crc_jlb"><thead><tr><th>

Setup procedure

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Define third-party risk areas.

</td><td>

A risk domain defines the type of risk to assess for a third party. For example, you might want to assess a data-management third party in terms of security risk and a bank in terms of financial risk. Security risk and financial risk are risk domains. Some platform applications refer to risk domains as "risk areas."

 See [Define a third-party risk domain](../task/tprm-risk-domain-define.md).

</td></tr><tr><td>

Define third-party risk area criteria.

</td><td>

A third-party risk area criteria is a group of risk domains \(sometimes called risk areas in other platform features\) that applies to a particular type of third party.

 See [Define third-party risk area criteria](../task/tprm-risk-domain-criteria-df.md).

</td></tr><tr><td>

Define component criteria.

</td><td>

Components are the entities for which you can assess risk. The base system includes the engagements, external monitoring, subsidiaries, and third-party risk assessments components. Risk is calculated for each component and then the risk is aggregated and rolled up to calculate a third-party risk rating.

 See [Define component criteria](../task/tprm-component-criteria-define.md).

</td></tr><tr><td>

Define engagements for a third party

</td><td>

Define an engagement so that you can assess the risks that are associated with the services or products offered by a third party. Engagements can also represent the products or services that are provided to the parent third party, either directly or from departments, partners, or subsidiaries that you can also assess for risk. As engagements are defined, you can define primary and secondary contacts for both third parties and engagements. Each type of contact can perform specific activities in the Third-party portal.

See [Define a VRM engagement](../task/tprm-ws-engagement-request.md).

</td></tr><tr><td>

Define engagement risk scoring rules.

</td><td>

An engagement risk-scoring rule specifies component criteria that determine which engagements are selected for assessment. For example, a rule could enable assessments for engagements that involve more than $40,000 annual business. Engagement scoring rules apply only to engagements.

 See [Define engagement risk scoring rules](../task/tprm-engagement-scoring-rules-df.md).

</td></tr><tr><td>

Define third-party risk scoring rules.

</td><td>

Define criteria, based on risk scores, that determine which third parties require assessments. Third-party risk scoring rules apply to subsidiaries and engagements and to third-party risk areas.

 See [Define third-party risk scoring rules](../task/tprm-tp-risk-scoring-rules-define.md).

</td></tr></tbody>
</table>