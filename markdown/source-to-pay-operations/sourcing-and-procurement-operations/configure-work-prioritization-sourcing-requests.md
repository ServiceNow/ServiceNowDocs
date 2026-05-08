---
title: Configure work prioritization for sourcing requests
description: Configure the Priority defaulting for sourcing requests decision table to automatically assign priority levels to sourcing requests based on the organizational seniority of the business owner or other administrator-defined conditions.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 4
keywords: [configure sourcing request priority, priority defaulting for sourcing requests, decision table, business owner, job code, organizational hierarchy, procurement administrator, demo rules, work prioritization, SPO]
breadcrumb: [Configuring work prioritization, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure work prioritization for sourcing requests

Configure the **Priority defaulting for sourcing requests** decision table to automatically assign priority levels to sourcing requests based on the organizational seniority of the business owner or other administrator-defined conditions.

## Before you begin

Before configuring work prioritization for sourcing requests, confirm the following:

-   The Shopping Hub application \(`sn_shop`\) is installed and active on the instance.
-   The following priority levels exist and are active in the instance's priority choice list: Critical, High, Moderate, Low, and Planning.
-   Job code records exist in the instance and are associated with user profiles in the expected way.
-   The **Business owner** field is populated on sourcing request records. If it is empty, no job code can be evaluated and no rule will match.

Role required: sn\_spend\_psd.psd\_admin or admin

## About this task

The **Priority defaulting for sourcing requests** decision table contains the rules that determine how priority is assigned to sourcing requests. The default example rules evaluate the **Business owner** field on the sourcing request and assign priority based on the business owner's job code.

The example rules ship as demo data and are likely not loaded in your production instance. Even if they are present, they reference job code records by internal identifiers specific to the demo dataset. These identifiers will not match your organization's job code records and the rules will not produce results until they are reconfigured with the correct values from your instance.

The **Business owner is CFO or CEO** demo rule is an exception — it evaluates the text value of the job code field directly, making it more portable. However, it only produces results if your organization's job codes use exactly those text values.

If your organization does not use job code hierarchy as the basis for sourcing priority, the conditions can be replaced entirely. Any field on the sourcing request or purchase line record is available as a condition input.

## Procedure

1.  Navigate to **All** &gt; **Sourcing and Purchasing Automation** &gt; **Decision Tables**.

2.  In the decision tables list, select **Priority defaulting for sourcing requests**.

    The decision table opens showing the table header, two input columns \(**Sourcing request** and **Purchase line**\), and the rules grid.

3.  If demo rules are present, review each rule and decide whether to keep, modify, or delete it.

    The default demo rules match job code records by internal identifier. Before these rules will produce results in your instance, you must replace the demo identifiers with the correct identifiers for your organization's job code records. Use the reference field lookup to select the correct job code records rather than entering values manually.

    If the demo rules do not reflect your organization's prioritization criteria, delete or deactivate them and add rules from scratch.

4.  Identify the job code records in your instance that correspond to the organizational tiers you want to prioritize.

    Navigate to the job codes list in your instance and note the records that represent each organizational tier — for example, executive, senior individual contributor, manager, and individual contributor levels. You will select these records when configuring rule conditions.

5.  Add a rule row to the rules grid.

6.  Configure the rule row by selecting each cell and providing the required values.

    -   To set a condition, select the operator cell and choose an operator, then select the condition value cell and enter a value. To match on business owner job code, use the dot-walked field `business_owner.job_code`. Use the reference field lookup to select the correct job code records rather than entering values manually.
    -   To set the result, select the result value cell and choose the priority level to assign when the rule matches.
    For detailed information about working with decision table cells, conditions, and results in Workflow Studio, see Modify decision table rules in Workflow Studio.

7.  In the **Rank** column, set the evaluation sequence for each rule.

    To change a rank value, double-click the number to edit it, enter a new value, and press **Enter**. Place rules for higher-urgency tiers at a lower rank number so they are evaluated first.

8.  Select **Save** to save the rule.

    Repeat steps 5 through 8 for each additional rule.

    Next, verify that the priority recalculation business rules are active for the sourcing request and purchase line tables.

9.  Navigate to **System Definition** &gt; **Business Rules** and search for **Recalculate priority on update** filtered by the sourcing request table and the purchase line table.

    Confirm both rules show as active.

10. Test the configuration by creating or updating a sourcing request where the business owner has a job code that matches one of your configured rules.

    After the background rule runs, verify that the **Priority** field on the sourcing request reflects the expected value. Also test a sourcing request whose business owner job code does not match any rule and confirm that its priority remains at **Planning**.

    If a sourcing request has no business owner, no job code can be evaluated and the record receives Planning priority.


## Result

Sourcing requests are automatically assigned a priority level when they are created or updated. Procurement specialists can sort and filter their work queue by priority to work the most urgent sourcing requests first.

**Parent Topic:**[Configuring work prioritization](../concept/configuring-work-prioritization.md)

