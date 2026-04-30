---
title: Knowledge article version numbers
description: Knowledge article version numbers follow a specific pattern. Increments to the version number depend on the revision type.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge article version numbers

Knowledge article version numbers follow a specific pattern. Increments to the version number depend on the revision type.

Article version numbers follow this pattern: &lt;major release number.minor release number&gt;.

The type of revision being made to an article determines the increment. A minor revision increments the version number by 0.01. A major revision, such as publishing an article, increments the version to the next whole number, for example, from version 2.02 to 3.0.

The following example illustrates the life cycle of a versioned article and the changes to the version number.

<table id="table_trn_kgl_yy"><thead><tr><th>

User action

</th><th>

Article state

</th><th>

Version number

</th></tr></thead><tbody><tr><td>

Knowledge author creates a new article

</td><td>

Draft

</td><td>

0.01

</td></tr><tr><td>

Knowledge author makes a change and updates the article.

</td><td>

Draft

</td><td>

0.01

</td></tr><tr><td>

Knowledge author submits the article for review.

</td><td>

Review

</td><td>

0.02

</td></tr><tr><td>

Knowledge author recalls the article to make another change.

</td><td>

Draft

</td><td>

0.03

</td></tr><tr><td>

Knowledge article submits the article for review

</td><td>

Review

</td><td>

0.04

</td></tr><tr><td>

Approver rejects the article and requests a change.

</td><td>

Draft

</td><td>

0.05

</td></tr><tr><td>

Knowledge author makes the change and submits the article for review.

</td><td>

Review

</td><td>

0.06

</td></tr><tr><td>

Approver approves the article

</td><td>

Scheduled for publish

</td><td>

0.07

</td></tr><tr><td>

Article is published

</td><td>

Published

</td><td>

1.0

</td></tr><tr><td>

Knowledge author checks out the published article.

</td><td>

Draft

</td><td>

1.01

</td></tr><tr><td>

Knowledge author submits the article for review.

</td><td>

Review

</td><td>

1.02

</td></tr><tr><td>

Approver approves the article

</td><td>

Scheduled for publish

</td><td>

1.03

</td></tr><tr><td>

Article is publishedWhen the version 2.0 article is published, the state of the version 1.0 article changes to **Outdated**.

</td><td>

Published

</td><td>

2.0

</td></tr></tbody>
</table>Any change to the state of an article results in a version increment, except to and from the **Pending retirement**, **Retired**, and **Outdated** states.

**Note:** To know more about minor version edits, see [Article versioning changes](article-versioning-changes.md).

**Parent Topic:**[Knowledge Management reference](../../../knowledge-management-reference.md)

