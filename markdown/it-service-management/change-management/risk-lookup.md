---
title: Calculated Risk Score
description: Risk lookup table is to get the risk value corresponding to the success probability value and impact value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/risk-lookup.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Reference, Change Management, IT Service Management]
---

# Calculated Risk Score

Risk lookup table is to get the risk value corresponding to the success probability value and impact value.

The sn\_chg\_probability\_risk\_lookup table provides the data that's used to calculate the risk value of a change request.

**Note:** The `sn_chg_probability_risk_lookup` table and the **Calculated Risk Score** menu item are available only after the change risk calculator feature is activated. If you don't see the table or the menu, activate the feature first. For more information, see [Activate Change Management - Risk Calculator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/activate-change-risk-calculator.md).

## Defining probability ranges

The **Calculated Risk Score** lookup does not define probability ranges. It consumes a success probability band that is calculated from the success probability definitions that produce each band. For more information, see [Success Probability definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/success-probability-definition.md). Also see [Success score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-score-calculation.md) for information on how the resulting band combines with impact to produce the risk value.

By default, the table contains nine records with all the possible mappings for Impact and Success Probability along with their corresponding risk values.

The lookup maps banded success probability values \(High, Medium, and Low\) against Impact values rather than raw percentages. The probability ranges that determine these bands are configured in the success probability definitions. For more information, see [Success Probability definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/success-probability-definition.md).

## Managing risk lookup records

You can add and delete records in the table. The **Check impact and probability combination** business rule validates duplicate mapping entries.

Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Calculated Risk Score**.

All risk calculating engines calculate their corresponding risk value. The system picks the highest risk and defines the risk for the change. You can modify the risk values regardless of the values defined for Impact and success probability.

You can view the success probability definition that set the success probability on the change request by accessing the sn\_chg\_probability\_details table. Users with read access to change requests can access this table.

On the change request form, in the **Related Links** section, select **Calculate risk**. The risk engines calculate the risk for the change. Select the icon next to the **Risk** field to view the risk set for the change.

Select the icon next to **Calculated Risk Score** to find which type of success probability definition sets the risk for the change. The Calculated Risk Score field can have the following values:

-   Calculated \(Impact + Success Probability\)
-   Calculated \(Impact + Change Success Score\)
-   Calculated \(Impact + Change Model Success\)
-   Not set: When the risk is not evaluated

**Note:** Risk lookup supports domain separation. The sn\_chg\_probability\_risk\_lookup table is process-separated when you install the domain separation plugin.

**Parent Topic:**[Reference section for Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/reference-change-management.md)

