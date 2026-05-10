---
title: Defining Expiration Rules
description: Define expiration rules for various observables or a combination of various source objects or indicators source that are created in TISC.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [About Rules Engine in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# Defining Expiration Rules

Define expiration rules for various observables or a combination of various source objects or indicators source that are created in TISC.

## Before you begin

Every source that is created in the application has an expiry period. The data feeds use the techniques such as time-based expiration period to boost the data ingestion. In TISC, the expiration rules defines the expiration time for a particular set of data sources or set of types of objects or types of observables.

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Expiration Rules**.

    The Expiration Rules page displays.

3.  Click **New**.

<table id="choicetable_vcd_cj4_zbc"><thead><tr><th align="left" id="d395820e97">

Field

</th><th align="left" id="d395820e100">

Description

</th></tr></thead><tbody><tr><td id="d395820e106">

**Name**

</td><td>

Enter a name for the expiration rule.

</td></tr><tr><td id="d395820e115">

**Description**

</td><td>

Enter a description for the expiration rule.

</td></tr><tr><td id="d395820e124">

**Expiry period \(days\)**

</td><td>

Specify the time duration after which the data ingested should expire or considered outdated.Enter the expiry period for the observable in days. For example, 100 days.

**Note:** Whatever the data that is ingested from the source will be expired 100 days after the ingestion.

</td></tr><tr><td id="d395820e137">

**Data Sources**

</td><td>

Indicates the expiration rule for the current data source. Select the list of data sources from the lookup.**Note:** Do not select this field and make sure to leave it blank if you want to select all the data sources.

If you want to select indicator as an object you must select the object and then select the **Type of records** value as **Indicator**.

**Note:** By default, a sample expiration rule sn\_sec\_tisc\_m2m\_entity\_rules is provisioned for the users within the base system. For Observables, this sample expiration rule will be in disabled state. You must enable and activate the rule. To apply the rule on the source records, you must enable the rule.

</td></tr><tr><td id="d395820e159">

**Category**

</td><td>

Indicates the expiration rule category type for the current data source. Select the category type from the drop-down list such as observable or object.

</td></tr><tr><td id="d395820e168">

**Type of Records**

</td><td>

Select the type of records.

</td></tr></tbody>
</table>4.  Click **Enable** to enable the expiration rule after you create a new rule.

    If you don't enable the expiration rule then the rule will not be applied to the source record.

    **Note:**

    -   Whenever you enable an expiration rule, then a duplication check happens in the background to verify if there is any duplicate rule in the system with the same combination of data sources and Type of records. If so, then the application prompts an information message that the rule already contains the same combination of data source and object category and you must modify the existing combination to enable the rule.
    -   A sample expiration rule is provisioned for the users in the base system and this **Sample Expiration Rule** for observable will be in disabled state by default and you must enable and activate the rule.
5.  Click **Save**.

6.  Click **Delete** if you wish to delete any expiration rule.


-   **[Expiration rules for source records](../concept/tisc-expiration-source.md)**  
Expiration rules are basically helpful to set the expiration time for the source records. The aggregate record inherits the highest expiration time from its corresponding sources records.

