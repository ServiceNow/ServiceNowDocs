---
title: Configuring the auto-generation of documents for healthcare cases
description: You can define the conditions for auto-generating documents for a healthcare case.
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configuring the auto-generation of documents for healthcare cases

You can define the conditions for auto-generating documents for a healthcare case.

As a user with the admin role, you can configure decision tables to automatically generate a healthcare document when the decision condition is satisfied for a healthcare case. For example, as part of the procedure scheduling process, you can define conditions to send privacy consent and procedure consent documents to patients for reviewing and signing them digitally.

Note the following points when configuring decision tables for healthcare cases:

-   Associate the document template for the healthcare document as the answer for the decision.
-   Associate the column in a healthcare case table as a decision input.

You configure decision tables for healthcare cases in the Healthcare and Life Sciences Service Management Core application by navigating to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Document decisions**. The **Trigger document flow for HC case** business rule runs on insert and update of every healthcare case and evaluates all document decisions that have the case reference configured as an input. When the decision conditions are satisfied, the business rule initiates the document workflow for the associated document template.

For more information, see [Decision Tables](https://www.servicenow.com/docs/access?context=decision-table&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

