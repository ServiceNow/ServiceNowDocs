---
title: Business stakeholder role for Agile Development 2.0
description: Use the business stakeholder role to read and retrieve data from any table of the Agile Development 2.0 and Scrum Programs applications to generate reports.
locale: en-US
release: zurich
product: Agile Development
classification: agile-development
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Agile Development 2.0, Strategic Portfolio Management]
---

# Business stakeholder role for Agile Development 2.0

Use the business stakeholder role to read and retrieve data from any table of the Agile Development 2.0 and Scrum Programs applications to generate reports.

When you activate the Business Stakeholder plugin \(com.snc.business\_stakeholder\) in your ServiceNow instance, the Read only roles for Agile 2.0 plugin \(com.snc.agile\_read\_roles\) is also activated. This plugin provides a business stakeholder role \(sn\_agile\_read\) with which you can access all the tables of Agile Development 2.0 and Scrum Programs applications. You can assign this role to any user in your organization who is a business stakeholder.

## Plugin availability

If you are a new customer, the Read only roles for the Agile 2.0 plugin \(com.snc.agile\_read\_roles\) is activated on zBoot. However, the business stakeholder role \(sn\_agile\_read\) is available only when you activate the Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\).

If you are an upgrade customer, you must manually activate the read-only roles for Agile 2.0 plugin \(com.snc.agile\_read\_roles\).

## Agile Development 2.0 tables accessible by users with the business stakeholder role

When both the Read only roles for Agile 2.0 plugin \(com.snc.agile\_read\_roles\) and the Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\) are active in your ServiceNow instance, the user with the business stakeholder role \(sn\_agile\_read\) has read access to the following tables.

<table id="table_AgileDev2.0"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product Assignment Group\[m2m\_product\_group\]

</td><td>

Stores relationship between products and groups.

</td></tr><tr><td>

Release Assignment Group\[m2m\_release\_group\]

</td><td>

Stores relationship between releases and groups.

</td></tr><tr><td>

Application Model \[cmdb\_application\_product\_model\]

</td><td>

Represents a whole product whose releases are being managed.

</td></tr><tr><td>

Release Product\[m2m\_product\_release\]

</td><td>

Represents all managed products.

</td></tr><tr><td>

Story Dependencies\[m2m\_story\_dependencies\]

</td><td>

Represents all related stories \(prerequisite and dependent\) to an existing story.

</td></tr><tr><td>

Scrum task\[rm\_scrum\_task\]

</td><td>

Represents a discrete amount of work for a story carried out during a sprint.

</td></tr><tr><td>

Sprint team member\[scrum\_pp\_sprint\_team\_member\]

</td><td>

Represents the list of users who are part of a sprint.

</td></tr><tr><td>

Team\[scrum\_pp\_team\]

</td><td>

Represents who completes scrum tasks and stories during releases and sprints.

</td></tr><tr><td>

Team name\[scrum\_pp\_team\_name\]

</td><td>

Represents the name of the scrum team.

</td></tr><tr><td>

Theme\[scrum\_theme\]

</td><td>

Represents either a tangible product \(such as a trading application\) or an abstract goal \(such as performance tuning\).

</td></tr><tr><td>

Scrum release \[rm\_release\_scrum\]

</td><td>

Represents individual versions \(releases\) of the product. Each release contains a list of sprints with a time range in which the stories in those sprints must be completed.

</td></tr><tr><td>

Sprint \[rm\_sprint\]

</td><td>

Stores sprints, which are the backlog items to be addressed together during a given time period.

</td></tr><tr><td>

Epic \[rm\_epic\]

</td><td>

Represents related stories or requirements that you have not yet transformed into stories.

</td></tr><tr><td>

Story \[rm\_story\]

</td><td>

Represents self-contained pieces of work that can be completed within a sprint.

</td></tr><tr><td>

Defect \[rm\_defect\]

</td><td>

Represents a deviation from the expected behavior of a product.

</td></tr><tr><td>

Enhancement \[rm\_enhancement\]

</td><td>

Represents an improvement to an existing product.

</td></tr></tbody>
</table>|Table|Description|
|-----|-----------|
|epic\_backlog\_definition|Stores the filter criteria that is used to create the epic backlogs.|
|scrum\_program\_m2m\_group|Stores the relationship between a scrum program and its teams.|

**Parent Topic:**[Agile Development 2.0 reference](agile-development-2-reference.md)

