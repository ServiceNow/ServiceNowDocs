---
title: Properties installed with Risk Management
description: Properties are added with activation of GRC: Risk Management.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Components installed with Risk Management, Reference, Risk Management, Governance, Risk, and Compliance]
---

# Properties installed with Risk Management

Properties are added with activation of GRC: Risk Management.

<table id="table_ycj_zqk_qjb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

States for which the risk is active \(the first state is the default active state\)sn\_risk.active\_states

</td><td>

-   Type: string
-   Default value: draft, assess, review, monitor
-   Location: **Risk** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

States for which risk is inactive \(the first state is the default inactive state\)sn\_risk.closed\_states

</td><td>

-   Type: string
-   Default value: retired
-   Location: **Risk** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Name of the assessment metric type that is used for risk assessmentsn\_risk.default\_assessment

</td><td>

-   Type: string
-   Default value: Risk Assessment
-   Location: **Risk** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Use qualitative impact scores as inputsn\_risk.qualitative\_impact

</td><td>

-   Type: true or false
-   Default value: false

**Note:** If upgrading from Geneva \(or earlier\) or Helsinki \(or later\) and the value was previously set to true, this value is set to true after upgrading.

-   Location: **Risk** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Use qualitative likelihood scores as inputsn\_risk.qualitative\_likelihood

</td><td>

-   Type: true or false
-   Default value: false
-   Location: **Risk** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Make risk statement mandatory in risksn\_risk.risk\_statement\_mandatory

</td><td>

-   Type: true or false
-   Default value: false.

**Note:** If false, allows risk creation with out any associated risk statement, if true risk statement is mandatory for risk creation


</td></tr><tr><td>

Compare risk tolerance based onsn\_risk\_advanced.risk\_tolerance

</td><td>

-   Type: choice list
-   Default value: Sum
-   Location: **Risk** &gt; **Administration** &gt; **Properties**

**Note:** This property is only available if you activate the Advanced Risk plugin.


</td></tr><tr><td>

Compare calculated risk score with sn\_risk\_advanced.risk\_rating\_config

</td><td>

-   Type: choice list
-   Default value: Average calculated ALE
-   Location: **Risk** &gt; **Administration** &gt; **Properties**

**Note:** This property is only available if you activate the Advanced Risk plugin.


</td></tr><tr><td>

Hide upstream and downstream riskssn\_risk.hide\_upstream\_downstream\_risks

</td><td>

-   Type: true or false
-   Default value: true.
-   Location: **Risk** &gt; **Administration** &gt; **Properties**

**Note:** This property is only available if you activate the Advanced Risk plugin.


</td></tr><tr><td>

Auto close issue created by indicatorsn\_grc.auto\_indicator\_issue\_closure

</td><td>

-   Type: yes or no
-   Default value: no.
-   Location: **Risk** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

A list of tables that are available in the 'Applies to' field on the Risk form.sn\_risk.risk\_applies\_to\_tables

</td><td>

-   Type: string
-   Default value: Risk Assessment
-   Location: **Risk** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Risk Management](r_InstallWRisk.md)

