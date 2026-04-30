---
title: Configuring confidential inheritance in your tables
description: You can set up confidentiality inheritance in the tables that are already configured in the confidentiality configuration module. In the GRC application, whenever a parent record is marked or unmarked as confidential, its related table records are also marked or unmarked as confidential.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Confidential records, Common GRC features, Governance, Risk, and Compliance]
---

# Configuring confidential inheritance in your tables

You can set up confidentiality inheritance in the tables that are already configured in the confidentiality configuration module. In the GRC application, whenever a parent record is marked or unmarked as confidential, its related table records are also marked or unmarked as confidential.

When you mark an issue as confidential, a related remediation task is automatically marked as confidential. For example, let's look at issue A. Issue A has the remediation tasks P, Q, and R. If issue A is marked as confidential, the remediation tasks P, Q, and R are also marked as confidential. The allowed users and groups are automatically appended based on the remediation task's confidentiality configuration record. Issue A's allowed users and groups are automatically appended to the inherited records P, Q, and R.

When an issue's confidentiality is unmarked, the corresponding confidentiality of a remediation task is also unmarked. Let's look at issue A again. Remember that issue A has the remediation tasks P, Q, and R. If the confidentiality is unmarked for issue A, then a dialog box appears with a question about whether it's okay to unmark the confidentiality for all the related tasks P, Q, and R or only for issue A. Based on what the selection is in the following example, the related records are unmarked as confidential.

![Unmark confidentiality.](../image/unmark-confidentiality.png "Unmark confidentiality")

As shown in the example dialog box, if **Include downstream records** was selected, then the confidentiality is unmarked for all the downstream records. If **Only this record** was selected, the confidentiality is unmarked for that single record only.

If you have access to the related confidential records and remove the confidentiality for a parent record, then the related records are also non-confidential.

**Note:** An inheritance configuration should exist between the parent and inherited tables.

## Examples of confidentiality inheritance

Inheritance works only at the point of marking a parent record as confidential. Let's look at the following two examples:

1.  When a parent record is marked as confidential, the related non-confidential records are also marked as confidential due to the inherited configuration. But, if a related record is added later, it isn’t automatically marked as confidential.
2.  Whenever confidentiality is marked on a parent record and the inheritance isn’t passed to the related records, the changes that are made later to the allowed users and groups of the parent record are not inherited in the related records.

For more information about the confidentiality inheritance configuration, see [KB1213404](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1213404) You must log in to the Now Support to view the Knowledge Base articles.

**Parent Topic:**[Confidential records](confidential-records.md)

